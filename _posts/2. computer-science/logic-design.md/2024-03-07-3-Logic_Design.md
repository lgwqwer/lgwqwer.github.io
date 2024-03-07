---
layout: single
title: '[Logic Design] 디지털 시스템 2'

categories:
  - logic-design

toc_label: 디지털 시스템
toc: true
toc_sticky: true

date: 2024-03-07
last_modified_at: 2024-03-07

comments: true
use_math: true
---

지난 시간에 이어, 디지털 시스템에 대해 더 알아보자.  

# 3. 디지털 정보의 표현

지난 시간에 이어, 디지털 정보의 표현 방법에 대해서 조금 더 알아보자.  

## - 전자 소자를 이용한 논리 표현  

### 1. 다이오드에 의한 스위칭

![LogicDesign1 2024-03-07 09_56_49](https://github.com/lgwqwer/lgwqwer.github.io/assets/129755540/8452464b-d8b2-475d-bce5-3c96c0740c34)

$V_s$로 걸어주는 전압이 5[V]면 a -> b 로 가는 D지점이 연결이 되어 스위치가 ON이 된다.

반대로, 걸어주는 전압이 0[V]면 a -> b 로 가는 D지점이 끊어지기 때문에, 스위치가 OFF 된다.  

<hr>

### 2. 쌍극성 트랜지스터에 의한 스위칭

![LD2 2024-03-07 09_58_44](https://github.com/lgwqwer/lgwqwer.github.io/assets/129755540/2094974b-22f0-4a98-9409-cd9fe01d29b4)

저런식으로 특정 지점이 끊겨있지 않으면, 아래로 전류가 흐르게 되어, $V_o$가 전류량이 0이 된다.  

$V_0$의 전류량이 1이 되기 위해서는 저 특정 지점이 끊겨있어야 한다. 

우리는 전기/전자 공학과가 아니기 떄문에 저런식으로 구성된다는 것만 알아두면 된다.  

### 3. NMOS 트랜지스터에 의한 스위칭

![LD3 2024-03-07 10_07_21](https://github.com/lgwqwer/lgwqwer.github.io/assets/129755540/3ec5baf2-cfde-4b0d-ba40-89929ca133df)

필자도 뭔지 모른다. 그냥 올린 거다.  
넘어가자.. 

<br>

# 4. 펄스 파형(Pulse Wave)

굉장히 중요하다.  
펄스 파형에 대해서 알아보도록 하자.  

펄스 파형은 Low 상태와 High 상태를 반복하는 전압레벨로 구성된다.  

펄스 파형은 주기 펄스(periodic pulse)와 비주기 펄스(non-periodic pulse)로 구분된다.  

<br>
<hr>

## - 이상적인 펄스 파형

![LD4 2024-03-07 10_33_22](https://github.com/lgwqwer/lgwqwer.github.io/assets/129755540/459690f3-d364-4890-b28e-32fcbd8499c9)

이상적인 주기 펄스는 상승에지(rising edge)와 하강에지(falling edge)로 구성된다.  

0에서 1로 뛰는 edge를 rising edge라고 부르고, 1에서 0으로 하강하는 edge를 falling edge라고 부른다.  

상승에지는 leading edge라고도 불린다.  
하강에지 또한 trailing edge라고도 불린다.  

<br>

## - 정논리(positive logic)와 부논리(negative logic)


![image](https://github.com/lgwqwer/lgwqwer.github.io/assets/129755540/ea45d698-7518-4cbb-9e37-44318dfeb16e)

정논리와 부논리는 디지털 논리 회로에서 사용되는 대표적인 표현 방식이다.    

높은 전압(5V)을 걸었을 때, "High = 1로 하자." 라고 정의하는 것을 정논리(positive logic)이라고 한다.  

반대로, 높은 전압(5V)를 걸었을 때, "High = 0으로 하자." 라고 정의하는 것을 부논리(negative logic)이라고 한다.  

<br>

## - 실제적인 펄스 파형

![LD5 2024-03-07 10_51_50](https://github.com/lgwqwer/lgwqwer.github.io/assets/129755540/8eecea61-998f-48d5-a402-95dbbce764c6)

현실에서는 이상적인 경우는 별로 없다.  
실제로는 이상적인 펄스 파형과 같이 0과 1로 즉각적인 형태가 아니다.  

상승시간, 하강시간, 펄스 폭은 그다지 중요하지 않으니 넘어가자.  

<br>

## - 주기(frequency)와 주파수(period)

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

### 예제 

주기가 $500\mu s$인 주기 파형이 있다. 이때 주파수를 구하여라.

<details>
<summary><font color='tomato'>풀이</font></summary>

$\mu s = 10^{-6}s$ 이므로, $500\mu s =  5 \cdot 10^{-4}s = T$ 이다. <br>

주파수-주기 관계에 의해, $f = \frac{1}{T} 이므로 \therefore f = \frac{1}{5 \cdot 10^{-4}} = 2000Hz = 2KHz$이다. 


</details>

<br>

# 5. 디지털 집적회로

- 디지털 회로: 디지털의 정보(0, 1)를 처리하는 디지털 시스템의 <font color='tomato'>하드웨어(hardware)</font>를 말한다.  

- 집척회로(IC: Integrated Circuit): 작은 실리콘 칩 위에 저항, 커패시터, 다이오드, 트랜지스터 등의 전자 부품을 여러 단계 공정을 거쳐서 내부적으로 상호 연결한 것을 의미한다.  

- 칩(chip): 실리콘 반도체를 의미한다.  

그냥 적당하게 뭐가 있는지 정도만 알면 된다.  

\+ 웨이퍼에 있는 회로 하나를 잘라서, 플라스틱을 씌우고 칩 처럼 만드는 이러한 과정을 패키징한다고 말한다.  

구체적인 과정은 알면 다친다.  

- 소자 수에 따른 집척 회로의 분류

소규모 집척회로: 100개 이하  
중규모 집척회로: 100 ~ 1,000개 ...

알 필요 없다.  
넘어가자.  

<br>

# 6. ADC와 DAC

ADC와 DAC는 아날로그-디지털 신호를 변환해주는 변환기라고 앞서 설명했다.  

변환기의 변환 과정을 간단하게 살펴보자.  

아날로그 신호를 디지털 신호로 변환하는 과정은 표본화 -> 양자화 -> 부호화로 구성되어 있다. 

이름부터 무섭다.. 변환 과정의 예시를 보면서 하나하나 살펴보도록 하자.  

## - 표본화(Sampling)

![S 2024-03-07 11_56_45](https://github.com/lgwqwer/lgwqwer.github.io/assets/129755540/79c88921-f1ff-48cc-b6c0-89caa3a79012)

저런식으로 단위시간(T)을 지정하여, <font color='tomato'>몇 번</font> 데이터(대표값)를 추출할 것인지 정하는 것이다.  

위 그래프는 아날로그 신호를 8번의 단위시간으로 쪼개어 샘플링을 진행했다.  

<br>
<hr>

## - 양자화(Quantization)

![s 2024-03-07 12_03_09](https://github.com/lgwqwer/lgwqwer.github.io/assets/129755540/7fcf2275-b030-4268-a8af-428010f0649a)

샘플링한 데이터(아날로그 신호의 값)들을 디지털화 하기 위해 <font color='tomato'>이산적인 값</font>으로 변환한다. 

위 그래프는 샘플링한 데이터를 반올림하여 디지털 값으로 근사시켰다.  

<br>
<hr>

## - 부호화(Coding)

![s 2024-03-07 12_06_56](https://github.com/lgwqwer/lgwqwer.github.io/assets/129755540/2e510d4e-6937-44b4-a456-f35fc0da52be)

디지털화 된 데이터들을 2진수 비트로 변환하는 과정을 말한다.  

\+ '부호화'라는 용어 자체는 무언가 1대1 대응되게 매칭하는 것을 의미한다.  
ex) encoding, decoding

