---
layout: archive
title: 'Chapter 1-2 벡터공간(vector space)'
categories:
  - linear-algebra
comments: true
use_math: true
---

# 목차
> 1. 벡터공간(vector space)
> 2. $n$순서쌍($n$-tuple)
> 3. 행렬(matrix)
> 4. 다항식(polynomial)
> 5. 여러가지 기본 성질

<br>

# 1. 벡터공간(vector space)

> - keyword  
> 벡터공간(vector), 스칼라(scalar), 벡터(vector)

> - Definition  
> 벡터공간(vector space)혹은 선형공간(linear space) $V$는 특정한 8가지 조건을 만족하여 정의된 합(sum)과 스칼라 곱(scalar multiplication) 두 연산을 가진 집합이다

여기서 말하는 8가지 조건은 다음과 같습니다

> - 8가지 조건  
> 1. $\forall (x,\,y) \in V$에 대하여 $x + y = y + x$ 이다.   (덧셈의 교환법칙)
> 2. $\forall (x,\,y,\,z) \in V$에 대하여 $(x + y) + z = x + (y + z)$ 이다. (덧셈의 결합법칙)
> 3. $\forall x \in V$에 대하여 $x + 0 = x$ 인 $0 \in V$가 존재한다. (영벡터의 존재성)
> 4. $\forall (x,\,y) \in V$에 대하여 $x + y = 0$인 $y \in V$가 존재한다. (역벡터의 존재성)
> 5. $\forall x \in V$에 대하여 $1x = x$이다.
> 6. $\forall (a,\,b) \in F$와 $\forall x \in V$에 대하여 $(ab)x = a(bx)$ 이다. (곱셈의 결합법칙)
> 7. $\forall a \in F$와 $\forall (x,\,y) \in V$에 대하여 $a(x + y) = ax + by$ 이다. (곱셈의 분배법칙)
> 8. $\forall (a,\,b) \in F$와 $\forall x \in V$에 대하여 $(a + b)x = ax + bx$ 이다. (분배법칙)

이와 같은 8가지 조건을 만족시키는 두 연산(합, 스칼라 곱)이 정의되어있는 집합이 벡터공간입니다

여기서 $F$의 원소는 스칼라(scalar)이고, 벡터공간 $V$의 원소는 벡터(vector)입니다!   
($*$ 여기서 말하는 벡터는 우리가 흔히 알고있는 크기와 방향을 가진 물리량의 개념과는 다른 것임에 주의!)

벡터공간을 정의할 때, 두 연산(합과 스칼라곱)의 정의를 반드시 기술해야 합니다  
두 연산을 정의할 때는 위 8가지 조건을 만족하는지 확인해야 해요!

<br>

# 2. $n$순서쌍($n$-tuple)

> - keyword  
> $n$순서쌍($n$-tuple), 성분(entry), 행 벡터(row vector), 열 벡터(column vector) 

> - Definition  
> $a_1,\,a_2,\,a_3, \ldots,\,a_n$이 $F$의 원소일 때, $(a_1,\,a_2,\,a_3, \ldots,\,a_n)$꼴을 $F$에서 성분을 가져온 $n$순서쌍($n$-tuple) 이라고 한다.   
여기서 $a_1, \, a_2$와 같은 $n$순서쌍의 원소를 성분(entry 또는 component)라고 한다.

$F$에서 성분을 가져온 두 $n$순서쌍 $(a_1,\,a_2,\,a_3, \ldots,\,a_n)$와 $(b_1,\,b_2,\,b_3, \ldots,\,b_n)$가 $a_i = b_i \,(i = 1,\,2,\,3,\ldots, n)$일 때, 두 순서쌍은 같다(equal)고 정의합니다  

예를 들어, $(1,\,4,\,5,\,6,\,10)$, $(1,\,4,\,5,\,6,\,10)$ 처럼  두 순서쌍의 성분이 같으면 서로 같은 $n$순서쌍 입니다

이제 벡터 공간을 한번 정의해봅시다  
정의를 하기에 앞서 표기법 하나를 짚고 가겠습니다
> - Notation  
> $F^n$ : 체 $F$에서 성분을 가져온 모든 $n$순서쌍의 집합

$u = (a_1,\,a_2,\,,\ldots,\,a_n) \in F^n$, $v = (b_1,\,b_2,\,,\ldots,\,b_n) \in F^n$, $c \in F^n$ 일 떄, 합과 스칼라 곱의 정의가

> - 합: $u + v = (a_1 + b_1,\, a_2 + b_2, \ldots, a_n + b_n)$  
> - 스칼라 곱: $cu = (ca_1,\, ca_2, \ldots,\, ca_n)$

이면 앞서말한 8가지 조건을 모두 만족하기에, 이 집합은 $F$-벡터공간 입니다

추가적으로, $F^n$의 벡터는 주로 행 벡터(row vector)보다는 열 벡터(column vector)로 표현합니다

<br>

# 3. 행렬(matrix)

> - keyword \\  
>  행렬(matrix), 대각성분(diagonal entry), 행(row), 열(column), 영 행렬(zero matrix), 정사각행렬(square matrix)

행렬:
$
\begin{bmatrix}
  a & b \\
  c & d
\end{bmatrix}
$
