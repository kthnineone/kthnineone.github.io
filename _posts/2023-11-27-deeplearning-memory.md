---
layout: post
title:  "Deep Learning 메모리 요구량"
date:   2023-11-27 15:31:00 +0900
categories: DeepLearning
tags: memory
use_math: true
---

최근 AI 모델, 특히 딥러닝 모델의 크기는 점점 커지고 있으며  
GPU 메모리는 유한하기 때문에 모델의 메모리 요구량을 계산해봐야 한다.



![Image Alt 텍스트]({{site.url}}/assets/images/Memory_requirements_0.PNG )

fp32는 32bit floating point로 Exponent 8 bits와 Mantissa 23 bits가 있다.  
나머지 1 bit는 sign으로 양수와 음수를 나타낸다.  
fp16은 16bit로 Exponent가 5 bits, Mantissa가 10 bits, 1 bit가 sign이다.  
Input, Activation, Parameter, Gradient, Optimize State (Adam의 경우 Parameter, Gradient, Momentum, Variance)를 모두 fp32로 나타낼 수도 있고,  
Optimizer가 아닌 파트는 fp16으로 나타내는 mixed precision을 사용할 수도 있다.  

![Image Alt 텍스트]({{site.url}}/assets/images/Memory_requirements_1.PNG )

Conv-1의 경우 11x11x3x96 = 34,848, 
그리고 새로이 변환된 Channel의 개수만큼인 96개의  biases가 추가되어 34,944개의 Parameters를 가진다.  
계산해보면 1.25 GB + $$\alpha$$만큼의 용량이 필요하다.  

총 메모리 할당 크기 = Parameter의 메모리 크기 + Gradient의 메모리 크기 + Activation의 메모리 크기 + Optimize State의 메모리 크기 + $$\alpha$$.<br>
이때, Parameter의 크기 = Gradient의 크기 = Optimize State의 Parameter의 크기 = Optimize State의 Gradient의 크기 <br> 
= Momentum의 크기 = Variance의 크기이므로, Optimize State의 크기 = 4 x Parameter의 크기다. <br>  
따라서, Parameter의 크기 x 2 bytes + Gradient의 크기 x 2 bytes + Optimize State의 크기 x 4 bytes + Activation의 크기 x 4 bytes <br>
= Parameter의 크기 x 4 bytes + Activation의 크기 x 4 bytes.

![Image Alt 텍스트]({{site.url}}/assets/images/Memory_requirements_2.PNG )

AlexNet 같은 비교적 예전 모델의 경우 4 GB도 안되는 작은 용량이지만,  
CoAtNet-7 같은 경우 약 45 GB가 넘어서 RTX 3090이나 4090으로도 돌리기 힘들다.  
GPT3 같은 거대한 모델의 경우 TB 단위라서 개인이 모델을 학습시키기 어렵다.  
심지어 개인 워크스테이션으로 RTX A6000 D6 48 GB를 4개를 써도 불가능하다.  

리소스가 충분한 개인이나 집단이 아니라면 거대 모델의 Pre-trained Model을 가져와서  Fine-Tuning하거나 Transfer Learning하는 작업이 필수적이다.
<br>
<br>

##### 출처  
패스트 캠퍼스의 [실무 사례로 배우는 컴퓨터 비전 논문 구현과 알고리즘 성능 최적화 With SOTA 모델](https://fastcampus.co.kr/data_online_sota) 강의를 듣고 정리한 내용입니다.
<br>

