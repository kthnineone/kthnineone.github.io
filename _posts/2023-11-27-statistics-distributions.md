---
layout: post
title:  "Statistical Distributions"
date:   2023-11-27 14:11:00 +0900
categories: Statistics
tags: distribution
use_math: true
---
{% raw %}
#### Discrete Distribution  
  
| 이름 | Name | pmf | Notation |
|---------------|-----|--------------------------------------------------------|---|
|베르누이 분포 |Bernoulli Dist | $${p^x} q^{1-x}$$ where $$q=1-p$$ | Bernoulli($$p$$) |
|이항 분포 |Binomial Dist | $$\binom{n}{k}$$ $${p^k} q^{n-k}$$  | Bin($$n, p$$) |
|다항 분포 | Multinomial Dist | $$\frac{n!}{x_1!,...,x_k!}{{p_1}^{x_1},...,{p_k}^{x_k}}$$  | Multinomial($$n$$, $$(p_1,...,p_k)$$) |
|포아송 분포 | Poisson Dist | $$\frac{{\lambda}^{k}}{k!}e^{-\lambda}$$  | Pois($$\lambda$$)|
|기하 분포 $$k$$ 시도 | Geometric Dist with $$k$$ Trials| $${(1-p)^k}p$$ | - |
|기하 분포 $$k$$ 실패 | Geometric Dist with $$k$$ Failures| $$(1-p)^{k-1} p$$  | - |
|음이항 분포 | Negative Binomial Dist | $$\binom{k+r-1}{k}$$ $$(1-p)^k p^r$$   | NB($$r, p$$) |
|초기하 분포 | Hypergeometric Dist | $$\frac{\binom{K}{k}\binom{N-K}{n-k}}{\binom{N}{n}}$$  | - |
|유니폼 분포 | Uniform Dist | $$\frac{1}{n}$$ where $$n=b-a+1$4 | Unif($$a,b$$) |  
    
#### Continuous Distribution  
  
| 이름 | Name | cdf | pdf | Notation |
|---------------|-----|--------------------------------------------------------|---|
| 정규(가우시안) 분포 | Normal (Gaussian) Dist | $$equation$$ | $$equation$$ | N($$\mu, \sigma^2$$) |
| 표준 정규 분포 |S tandard Normal Dist | $$equation$$  | $$equation$$ | N(0, 1) |
| 티 분포 | t-Dist | $$equation$$  | $$equation$$ | t($$\nu$$) |
| 카이제곱 분포 | Chi-squared ($$\chi^{2}$$) Dist | $$equation$$  | $$equation$$ | $$\chi^{2}(k)$$ |
| 에프 분포 | F-Dist | $$equation$$  | $$equation$$ | F($$d_1, d_2$$) |
| 감마 분포 | Gamma Dist | $$equation$$  | $$equation$$ | Gamma(k, $$\theta$$) or  Gamma($$\alpha, \beta$$)|
| 지수 분포 | Exponential Dist | $$equation$$  | $$equation$$ | exp($$\lambda$$) |
| 베타 분포 | Beta Dist | $$equation$$  | $$equation$$ | Beta($$\alpha, \beta$$) |
| 와이블 분포 | Weibull Dist | $$equation$$  | Weib($$\lambda$$, k) |
| 랭 분포 | Erlang Dist | $$equation$$  | $$equation$$ | 1 |
| 디리클레 분포 | Dirichlet Dist | $$equation$$  | Dir($$\vec{\alpha}$$) where $$\vec{\alpha}$$ = ($$\alpha_1,...,\alpha_K$$)|
| 파레토 분포 | Pareto Dist | $$equation$$  | $$equation$$ | 1 |
| 제타 분포 | Zeta Dist | $$equation$$  | $$equation$$ | 1 |
| 라플라시안 분포 | Laplacian Dist | $$equation$$  | $$equation$$ | 1 |
| 코시 분포 | Cauchy Dist | $$equation$$  | $$equation$$ | 1 |
| 유니폼 분포 | Uniform Dist | $$equation$$  | $$equation$$ | Unif(a,b) |  
  
{% endraw %}


