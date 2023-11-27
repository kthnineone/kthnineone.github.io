---
layout: post
title:  "Random Variables"
date:   2023-11-27 15:08:00 +0900
categories: statistics
tags: random-variable
use_math: true
---

Outcome은 가능한 사건이다.<br>
Event는 일어난 사건이다.<br>
Experiment or Trial은 outcome을 반복해서 뽑는 행위다.<br>  
&nbsp;
$$\Omega$$는 Sample Space로 정의한다. 이는 가능한 모든 Outcome의 집합이다. <br>  
$$\delta-algebra, F$$는 다음 세가지를 만족하는 a collection of sets in $$\Omega$$다.<br>  
1. If $$S$$ $$\in$$ $$F$$, then complement of $$S$$ also $$\in$$ $$F$$. 
2. If $$S_1$$ and $$S_2$$ $$\in$$ $$F$$, then ($$S_1$$ $$\cup$$ $$S_2$$) also $$\in$$ $$F$$. 
3. $$\Omega$$ $$\in$$ $$F$$.  
&nbsp;

Probability Measure $$P$$는 다음의 공리를 가진다.  
$$P:, F, \rightarrow R$$  
1. Non-negative. P($$S$$) $$\geq$$ 0 for any event $$S \in F$$. 
2. $$\delta-additive$$. If the sets $$S_1, ...,... S_n, \in F$$ are disjoint to each other, then P($$\cup,S_i$$)=$$\Sigma P(S_i)$$.
3. Normalization. P($$\Omgea$$)=1.
&nbsp;