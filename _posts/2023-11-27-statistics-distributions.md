---
layout: post
title:  "Statistical Distributions"
date:   2023-11-27 14:11:00 +0900
categories: Statistics
tags: distribution
use_math: true
---
다양한 discrete disributions와 continuous distributions의 이름과 Notation, pmf 혹은 cdf, pdf, 사용 예시를 정리해보았다. <br>
<br>  
<br>  
  
{% raw %}
#### Discrete Distribution (이산형 분포)  
  
| 이름 | Name | pmf | Notation | 사용예시 |
|---------------|-----|--------------------------------------------------------|---|
|베르누이 분포 |Bernoulli Dist | $${p^x} q^{1-x}$$ where $$q=1-p$$ | Bernoulli($$p$$) | 동전을 한 번 던진다. |
|이항 분포 |Binomial Dist | $$\binom{n}{k}$$ $${p^k} q^{n-k}$$  | Bin($$n, p$$) | 같은 동전을 순차적으로 n번 던진다. |
|다항 분포 | Multinomial Dist | $$\frac{n!}{x_1!,...,x_k!}{{p_1}^{x_1},...,{p_k}^{x_k}}$$  | Multinomial($$n$$, $$(p_1,...,p_k)$$) | 주사위를 n번 던진다. |
|포아송 분포 | Poisson Dist | $$\frac{{\lambda}^{k}}{k!}e^{-\lambda}$$  | Pois($$\lambda$$)| 단위 시간 동안 발생하는 사건의 수 |
|기하 분포 $$k$$번 실패 | Geometric Dist with $$k$$ Failures| $${(1-p)^k}p$$ | - | k번 시도에서 처음 성공할 확률 |
|기하 분포 $$k$$번 시도 | Geometric Dist with $$k$$ Trials| $$(1-p)^{k-1} p$$  | - | 첫 성공까지 k번 실패할 확률 |
|음이항 분포 | Negative Binomial Dist | $$\binom{k+r-1}{k}$$ $$(1-p)^k p^r$$   | NB($$r, p$$) | r번째 성공까지 k번 실패할 확률 |
|초기하 분포 | Hypergeometric Dist | $$\frac{\binom{K}{k}\binom{N-K}{n-k}}{\binom{N}{n}}$$  | - | 비복원추출에서 N개 중에 n번 추출했을 때 원하는 것 k개가 뽑힐 확률의 분포 |
|유니폼 분포 | Uniform Dist | $$\frac{1}{b-a+1}$$ | Unif($$a,b$$) | 동전 던지기나 주사위 던지기 |  
  
<br>  
<br>  
<br>  
  
#### Continuous Distribution (연속형 분포)  
  
| 이름 | Name | cdf | pdf | Notation |
|---------------|-----|--------------------------------------------------------|---|
| 정규(가우시안) 분포 | Normal (Gaussian) Dist | $$\Phi(\frac{x - \mu}{\sigma})$$ | $$\frac{1}{\sigma \sqrt{2\pi}}\exp^{-\frac{1}{2}{(\frac{x - \mu}{\sigma})}^2}$$ | N($$\mu, \sigma^2$$) |
| 표준 정규 분포 |Standard Normal Dist | $$\Phi(x)$$ | $$\frac{1}{\sqrt{2\pi}}\exp^{-\frac{1}{2} x^2}$$ | N(0, 1) |
| 티 분포 | t-Dist | $$equation$$  | $$equation$$ | t($$\nu$$) |
| 카이제곱 분포 | Chi-squared ($$\chi^{2}$$) Dist | $$equation$$  | $$equation$$ | $$\chi^{2}(k)$$ |
| 에프 분포 | F-Dist | $$equation$$  | $$equation$$ | F($$d_1, d_2$$) |
| 지수 분포와 레이트 모수 | Exponential Dist with Rate Parameter | $$1 - e^{-\lambda x}$$  | $$\lambda e^{-\lambda x}$$ | Exp($$\lambda$$) |
| 지수 분포와 스케일 모수 | Exponential Dist with Scale Parameter | $$1 - e^{-\frac{x}{\theta}}$$  | $$\frac{1}{\theta} e^{-\frac{x}{\theta}}$$ | Exp($$\theta$$) |
| 감마 분포와 쉐이프, 스케일 모수 | Gamma Dist with Shape and Scale Parms| $$\frac{1}{\Gamma(\alpha)} \gamma(\alpha, \frac{x}{\theta})$$ | $$\frac{\beta ^ \alpha}{\Gamma(\alpha)}x^{\alpha - 1}e^{-x/\theta}$$ | Gamma($$k, \theta$$)|
| 감마 분포와 쉐이프, 레이트 모수 | Gamma Dist with Shape and Rate Parms | $$\frac{1}{\Gamma(\alpha)} \gamma(\alpha, \beta x)$$ | $$\frac{\beta ^ \alpha}{\Gamma(\alpha)}x^{\alpha - 1}e^{-\beta x}$$ | Gamma($$\alpha, \beta$$)|
| 베타 분포 | Beta Dist | $$equation$$  | $$equation$$ | Beta($$\alpha, \beta$$) |
| 와이블 분포 | Weibull Dist | $$equation$$  | $$equation$$  | Weib($$\lambda, k$$) |
| 랭 분포 | Erlang Dist | $$equation$$  | $$equation$$  | - |
| 디리클레 분포 | Dirichlet Dist | $$equation$$  | $$equation$$  |Dir($$\vec{\alpha}$$) where $$\vec{\alpha}$$ = ($$\alpha_1,...,\alpha_K$$)|
| 파레토 분포 | Pareto Dist | $$equation$$  | $$equation$$ | - |
| 제타 분포 | Zeta Dist | $$equation$$  | $$equation$$ | - |
| 라플라시안 분포 | Laplacian Dist | $$equation$$  | $$equation$$ | - |
| 코시 분포 | Cauchy Dist | $$equation$$  | $$equation$$ | - |
| 유니폼 분포 | Uniform Dist | $$\begin{cases} 0 for x < a\\ \frac{x-a}{b-a} for x \in [a, b]\\ 1 for x > b   \end{cases}$$  | $$\frac{1}{b-a}$$ for $$x \in \[a,b\]$$ | Unif($$a,b$$) |   
  
{% endraw %}  

<br>  

##### Notations  

$$\Gamma(\alpha)$$ if gamma function. For all positive integers, $$\Gamma(\alpha)=(\alpha-1)!$$.  
For real number $$z$$, $$\Gamma(z) = \int_{0}^{\infty} t^{z-1} e^{-t} dt$$.  
<br>

Incomplete gamma function:  
The upper incomplete gamma function is defined as:  
$$\Gamma(s, x)=\int_{x}^{\infty} t^{s-1} e^{-t} dt$$  
The lower incomplete gamma function is defined as:  
$$\gamma(s, x)=\int_{0}^{x} t^{s-1} e^{-t} dt$$  

<br>

