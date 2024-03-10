---
layout: single
title: '[Logic Design] 아날로그(Analog) vs 디지털(Digital)'

categories:
  - logic-design

toc_label: 아날로그 vs 디지털
toc: true
toc_sticky: true

date: 2024-03-07
last_modified_at: 2024-03-07

comments: true
use_math: true
---

아날로그와 디지털 각각의 특징과 차이점을 알아보도록 하자.

<br>

## - 아날로그 신호(Analog Signal)란?

아날로그 신호는 <font color='tomato'>자연계에서 일어나는 물리적 현상에 대한 신호</font>를 말한다.  

![image](https://github.com/lgwqwer/lgwqwer.github.io/assets/129755540/11835842-bfba-4843-96c6-a72dcf24c7ce)
(출처: 기상청-기상자료개발포털)  

에를 들어 위의 기온 분석 그래프를 보면, 기온 같은 <font color='tomato'>자연 현상</font>은 시간에 따른 기온이 <font color='tomato'>연속적으로</font> 변한다.

기온 뿐만 아니라 소리, 빛 등 여러 자연현상은 대부분 연속적으로 존재한다.  

이러한 연속적인 특성을 가진 자연현상을 표현하는 신호가 바로 <font color='tomato'>아날로그 신호(Analog Signal)</font>이다.

<br>

## - 디지털 신호(Digital Signal)란?

![image](https://github.com/lgwqwer/lgwqwer.github.io/assets/129755540/20f4359a-713c-473b-9cac-aaf59dd26e4f)

디지털 신호는 아날로그 신호와는 반대로, <font color='tomato'>이산적인</font> 값을 가지는 특성이 있다.  

<br>

![image](https://github.com/lgwqwer/lgwqwer.github.io/assets/129755540/6f0dfcad-c88b-46d8-bf0b-1b98bb201fdb)

위 디지털 온도계같이, 버튼만 누르면 바로 온도가 뜨는 것과 같은 <font color='tomato'>이산적인</font> 특징을 가지면, <font color='tomato'>디지털 신호</font>라고 볼 수 있다.


<br>

## - 아날로그 신호/디지털 신호의 특징

- 디지털 신호

1. 0과 1의 형태로만 신호를 보내기 때문에, 외부 잡음(Noise)에 강함.

2. 설계하기가 쉬움.

3. 프로그래밍으로 전체 시스템을 제어할 수 있어서 사양의 변경에 쉽게 대응할 수 있음.

4. 이산적인 특징으로, 정보를 가공하기 쉬움.

5. 정보 처리의 정확성과 정밀도를 높일 수 있음.

6. 설계하기 쉽고, 제어하기 쉽기 때문에 전체 시스템에 대한 비용 절감.

7. 전체 시스템 소형화 가능.  

<hr>

- 아날로그 신호

1. 외부 잡음(Noise)에 약함.

2. 전송 거리가 멀어질 수록 신호 감쇠 발생.

<br>

# - 디지털과 아날로그 신호는 완전히 다른 개념인가?

꼭 그렇지만은 않다.  

디지털 신호를 무한정 쪼개어보면, 이산적인 값도 결국 연속적으로 보이기 때문에, 서로 변환이 가능하다.  

이러한 아날로그 신호를 디지털 신호로 변환해주는 장치를 바로 <font color='tomato'>ADC</font>(Analog-to-Digital converter)라고 한다.  

변환한 디지털 신호를 그대로 출력할 수도 있고, 가공하여 다시 아날로그 신호로 변환할 수 있다.  

이렇게 디지털 신호를 아날로그 신호로 바꿔주는 장치를 <font color='tomato'>DAC</font>(Digital-to-Analog converter)라고한다.  

즉, 아날로그 시스템과 디지털 시스템은 무작정 서로 동떨어진 개념이 아니고, 언제든지 변환하고 서로 영향을 줄 수 있는 시스템이다.

