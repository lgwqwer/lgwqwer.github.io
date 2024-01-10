---
layout: archive
title: 'Chapter 1-2 기본적으로 필요한 미적분학'
categories:
  - linear-algebra
comments: true
use_math: true
---

# 1. 주요 함수들의 미분

미분방정식을 공부하기 전에 먼저 알아야할 것은 미적분학이다.  
다음과 같은 멱함수의 미분, 삼각함수의 미분, 지수함수의 미분, 로그함수의 미분 등 여러가지 형태의 함수들을 미분할 수 있어야 한다.  
   
>$\frac{d}{dx}(x^n) = nx^{n-1}$ <br>       
>$\frac{d}{dx}(sin\,x) = cos\,x$<br>      
>$\frac{d}{dx}(cos\,x) = sin\,x$<br>     
>$\frac{d}{dx}(e^x) = e^x$      <br>           
>$\frac{d}{dx}(ln\,x) = \frac{1}{x}$  

<br>

# 2. 미분 법칙

주요 함수들의 덧셈, 뺼셈, 곱셈, 나눗셈의 형태를 미분하기 위해서는 다음과 같은 미분 법칙들을 알아야 한다.

- 덧셈/뺼셈 미분 법칙   

>$\frac{d}{dx}\{f(x) \pm g(x)\} = f'(x) \pm g'(x)$

- 곱 미분 법칙  

>$\frac{d}{dx}\{f(x)g(x)\} = f'(x)g(x) + f(x)g'(x)$

- 몫 미분 법칙 

>$\frac{d}{dx}\{\frac{g(x)}{f(x)}\} = \frac{g'(x)f(x)-g(x)f'(x)}{f(x)^2}$

위와 같은 미분 법칙들을 알아야 한다.

<br>

- 연쇄 법칙
  
주요 함수들을 더 광범위하게 다루기 위해서는 연쇄 법칙(chain rule)을 알아야 한다.
예를들어 $y = e^x$ 와 $x = sin\, t$ 를 합성하면 $y = e^{sin \, t}$ 가 된다.   
연쇄 법칙을 통해 $\frac{dy}{dt}$는 $\frac{dy}{dx}$와 $\frac{dx}{dt}$와의 곱임을 알 수 있다. 

<br>

>$\frac{dy}{dt} = \frac{dy}{dx} \frac{dx}{dt} = e^x\,cos\,t = y\,cos\,t$

<br>

# 3. 미적분학의 기본 정리

- 차의 합 <br>
>$(y_1 - y_0) + (y_2 - y_1) + ... + (y_n - y_{n-1}) = y_n - y_0$