---
layout: single
title: '[논리설계] Ch 1-3 펄스 파형(Pulse Wave)'

categories:
  - logic-design

toc_label: 펄스 파형
toc: true
toc_sticky: true

date: 2024-03-07
last_modified_at: 2024-03-07

comments: true
use_math: true
---

펄스 파형에 대해서 알아보도록 하자.

<br>

# 펄스 파형(Pulse Wave)

펄스 파형은 Low 상태와 High 상태를 반복하는 전압레벨로 구성된다.  

펄스 파형은 주기 펄스(periodic pulse)와 비주기 펄스(non-periodic pulse)로 구분된다.  

<br>
<hr>

# 1. 이상적인 펄스 파형

![LD4 2024-03-07 10_33_22](https://github.com/lgwqwer/lgwqwer.github.io/assets/129755540/459690f3-d364-4890-b28e-32fcbd8499c9)

이상적인 주기 펄스는 상승에지(rising edge)와 하강에지(falling edge)로 구성된다.  

0에서 1로 뛰는 edge를 rising edge라고 부르고, 1에서 0으로 하강하는 edge를 falling edge라고 부른다.  

상승에지는 leading edge라고도 불린다.  
하강에지 또한 trailing edge라고도 불린다.  

<br>

# 2. 정논리(positive logic)와 부논리(negative logic)


![image](https://github.com/lgwqwer/lgwqwer.github.io/assets/129755540/ea45d698-7518-4cbb-9e37-44318dfeb16e)

정논리와 부논리는 디지털 논리 회로에서 사용되는 대표적인 표현 방식이다.    

높은 전압(5V)을 걸었을 때, "High = 1로 하자." 라고 정의하는 것을 정논리(positive logic)이라고 한다.  

반대로, 높은 전압(5V)를 걸었을 때, "High = 0으로 하자." 라고 정의하는 것을 부논리(negative logic)이라고 한다.  

<br>

# 3. 실제적인 펄스 파형

![LD5 2024-03-07 10_51_50](https://github.com/lgwqwer/lgwqwer.github.io/assets/129755540/8eecea61-998f-48d5-a402-95dbbce764c6)

현실에서는 이상적인 경우는 별로 없다.  
실제로는 이상적인 펄스 파형과 같이 0과 1로 즉각적인 형태가 아니다.  

상승시간, 하강시간, 펄스 폭은 그다지 중요하지 않으니 넘어가자.  

<br>

# 4. 주기(frequency)와 주파수(period)

주기와 주파수는 고등 물리 시간에 배웠을 것이다.  
혹여 안 배웠더라도 중요하니 열심히 공부해두자.

<br>

![LD6 2024-03-07 11_00_59](https://github.com/lgwqwer/lgwqwer.github.io/assets/129755540/a3499bb0-9615-4063-ac68-f4f1c43dc32b)


- 주파수: 주기적인 파형이 <font color="tomato">1초동안 진동한 횟수</font>를 의미 ( 단위: Hz )

예를 들어, 120hz 라고 한다면, 1초에 120번 진동하는 것이다.  

<br>
<hr>
<br>

![S 2024-03-07 11_02_35](https://github.com/lgwqwer/lgwqwer.github.io/assets/129755540/6fe55b92-6d7c-4db8-b487-bd97ba757063)


- 주기: 주기적인 파형이 <font color="tomato">한 번 진동하는데 걸리는 시간</font>을 의미한다. 

딱 보면 둘 사이의 관계가 있어보이지 않는가??  

주파수가 커지면, 1초에 진동하는 횟수가 많아진다는 것이니, 자연스럽게 주기가 줄어들 것이다.  

즉, 주파수와 주기는 반비례 관계이다.  

식으로 나타내면 다음과 같다.  

>$T = \frac{1}{f}\ \  f = \frac{1}{T} \ \ (주파수: f, 주기: T)$ 

예제를 한번 풀어보자.

<br>

## - 예제

주기가 $500\mu s$인 주기 파형이 있다. 이때 주파수를 구하여라.

<details>
<summary><font color='tomato'>풀이</font></summary>

$\mu s = 10^{-6}s$ 이므로, $500\mu s =  5 \cdot 10^{-4}s = T$ 이다. <br>

주파수-주기 관계에 의해, $f = \frac{1}{T} 이므로 \therefore f = \frac{1}{5 \cdot 10^{-4}} = 2000Hz = 2KHz$이다. 


</details>