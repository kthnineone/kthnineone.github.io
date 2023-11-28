---
layout: post
title:  "Probability Space and Random Variables"
date:   2023-11-27 15:08:00 +0900
categories: Statistics
tags: random-variable
use_math: true
---
#### Outcome, Event, Experiment, Trial  

<b>Outcome</b>은 가능한 사건이다.<br>
<b>Event</b>는 일어난 사건이다.<br>
<b>Experiment or Trial</b>은 outcome을 반복해서 뽑는 행위다.<br>  
<br>


#### Sample Space  
$$\Omega$$는 Sample Space로 정의한다. 이는 가능한 모든 Outcome의 집합이다. <br>  
$$\sigma-algebra$$ $$F$$는 다음 세가지를 만족하는 a collection of sets in $$\Omega$$다.<br>  
1. If $$S$$ $$\in$$ $$F$$, then complement of $$S$$ also $$\in$$ $$F$$. 
2. If $$S_1$$ and $$S_2$$ $$\in$$ $$F$$, then ($$S_1$$ $$\cup$$ $$S_2$$) also $$\in$$ $$F$$. 
3. $$\Omega$$ $$\in$$ $$F$$.  
<br>
<br>



#### Probability Measure  
<b>Probability Measure</b> $$P$$는 다음의 공리를 만족해야 한다.  
$$P: F \rightarrow R$$이고 이때 $$R$$은 실수 집합이다.  
1. Non-negative. P($$S$$) $$\geq$$ 0 for any event $$S \in F$$. 
2. $$\sigma-additive$$. If the sets $$S_1, ...,... S_n, \in F$$ are disjoint to each other, then $$P(\cup S_i$$)=$$\Sigma P(S_i)$$.
3. Normalization. P($$\Omega$$)=1.  
<br>
<br>



#### Probability Space  
<b>Probability Space</b>는 Sample Space $$\Omega$$, a set of events인 $$\sigma-algebra$$, <br>
events에 확률을 부과하는 Proability Measure인 $$P$$로 이루어진 triple ($$\Omega$$, $$\sigma-algebra$$, $$P$$)다.  
&nbsp;
<br>



#### Random Variable  
<b>확률 변수 Random Variable</b>은 Sample Space를 실수로 보내는 함수다. <br>
$$X: \Omega \rightarrow R$$. <br>
같은 Sample Space에 대해서 여러가지 함수를 취할 수 있다.<br>
동전을 던지는 경우 Sample Space는 {Head, Tail}이다. <br>
1. X(Head) = 1, X(Tail) = 0 으로 정의할 수 있다.
2. X(Head) = -1, X(Tail) = 1 으로 정의할 수 있다.  
<br>
<br>
