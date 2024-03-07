---
layout: single
title: '[Logic Design] 디지털 논리회로 1'

categories:
  - logic-design

toc_label: 디지털 논리회로
toc: true
toc_sticky: true

date: 2024-03-07
last_modified_at: 2024-03-07

comments: true
use_math: true
---

오늘은 디지털 시스템에 대해서 알아보도록 하자. 

<br>

# 1. 아날로그 신호 vs 디지털 신호 

우리는 디지털과 반대되는 개념을 흔히 아날로그라고 생각한다. 

각각의 특징과 차이점을 알아보자.  

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

# 2. 디지털과 아날로그 신호는 완전히 다른 개념인가?

꼭 그렇지만은 않다.  
디지털 신호를 무한정 쪼개어보면, 이산적인 값도 결국 연속적으로 보이기 때문에, 서로 변환이 가능하다.  

이러한 아날로그 신호를 디지털 신호로 변환해주는 장치를 바로 <font color='tomato'>A/D converter</font>(Analog-to-Digitalconverter)라고 한다.  

변환한 디지털 신호를 그대로 출력할 수도 있고, 가공하여 다시 아날로그 신호로 변환할 수 있다.  

이렇게 디지털 신호를 아날로그 신호로 바꿔주는 장치를 <font color='tomato'>D/A converter</font>(Digital-to-Analog converter)라고한다.  

즉, 아날로그 시스템과 디지털 시스템은 무작정 서로 동떨어진 개념이 아니고, 언제든지 변환하고 서로 영향을 줄 수 있는 시스템이다.

<br>

# 3. 디지털 정보를 표현하는 방법

앞서 말했다시피, 디지털은 정보를 이산적인 방식으로 처리한다고 했다.  
구체적으로 정보를 어떻게 표현하는지 알아보자.

## - 디지털 정보의 전압레벨 

디지털 시스템은 보통 이진수 체계(Binary System)을 사용한다.   

0과 1만의 디지트(digit)를 사용한다.  

![이름 없는 노트북 2024-03-07 06_43_22](https://github.com/lgwqwer/lgwqwer.github.io/assets/129755540/fd49f219-0b25-42c0-8ba9-f16879c69b73)

위 그래프와 같이, 높은 범위, 낮은 범위를 설정하고, 그 높은 범위에 속하면 1, 낮은 범위에 속하면 0으로 정보를 처리한다.

<br>

## - 디지털 정보의 표현 단위

디지털 정보의 표현 단위는 굉장히 기본이 되는 내용이라 꼭 알아둬야한다.  

![image](https://github.com/lgwqwer/lgwqwer.github.io/assets/129755540/957035c5-3511-4716-9560-91982bd67d1d)


- 1 nibble = 4 bit
- 1 byte = 8 bit
- 1 byte = 1 character (영어는 1문자 = 1byte, 한글은 1문자 = 2byte)
- 1 word: 특정 CPU에서 취급하는 명령어나 데이터의 길이에 해당하는 비트 수

<br>

여기서 1 word가 의아할 것이다.  
1 word는 특정한 길이가 정해져 있는 것이 아니라, 한 개의 명령어를 한번에 처리하는데에 들어가는 비트 수 만큼 길이를 가진다.  

<hr>
<br>


추가로, MSB(Most Significant Bit)와 LSB(Least Significant Bit)가 뭔지 알아보자.  

보통 10진수로 표기를 할 때, 가장 왼쪽의 숫자가 가장 큰 자릿 수를 표현한다.  
예를 들어, 82712라는 숫자를 가져오면, 가장 왼쪽의 수인 8이 가장 큰 자릿 수인 것을 알 수 있다.  

하지만, 컴퓨터에서 숫자를 표현할 때는 꼭 왼쪽이 가장 큰 자릿 수라는 것을 보장하지 않는다.  

따라서, 이진수를 사용할 때에는, 가장 큰 자릿수와 가장 작은 자릿수를 직접 표기해줘야 한다.  

바로 그 역할을 하는 것이 MSB와 LSB이다.  

![image](https://github.com/lgwqwer/lgwqwer.github.io/assets/129755540/fbd13ca0-7a7b-4ec5-953a-adefea367cef)


MSB라고 표기해준 부분이 가장 큰 자릿수를 의미한다.  
반대로, LSB는 가장 작은 자릿수를 의미한다.  

<br>

## - SI 단위와 IEC 단위 비교
![image](https://github.com/lgwqwer/lgwqwer.github.io/assets/129755540/4c84fd17-0b5d-4d49-baf8-1a84515b1ce9)
(출처: 위키디피아)

우리는 줄곧 1,000단위를 K(킬로), 1,000,000를 M(메가), 1,000,000,000은 G(기가) 등등 여러 10진 단위를 사용해왔다.  

그 10진 단위를 SI 단위라고 한다.  
추가로, 10진 단위는 [밑 수](https://ko.wikipedia.org/wiki/%EB%B0%91%EC%88%98)가 10인 단위를 의미한다.  


하지만, 디지털 세계에서는 2진수로 표현하므로, 단위가 조금 다르다.  

![image](https://github.com/lgwqwer/lgwqwer.github.io/assets/129755540/7ada8632-c252-4bde-908d-3f18c2cdd697)

밑 수가 2인 단위를 2진 단위라고 하고, 그 2진 단위를 IEC 단위라고 한다.  

Ki(키비)/K(킬로), Mi(메비)/M(메가), ... SI 단위랑 IEC 단위랑 뭔가 비슷해보인다.  

그러나 밑 수가 다르기 떄문에, 약간의 오차가 있는 것을 알 수 있다. 

예제를 한번 풀어보자.  

### 예제

일반 DVD-ROM은 9.6GiB의 디지털 데이터를 저장할 수 있다.  
DVD-ROM에는 얼마나 많은 데이터(bit)가 저장 되는가?   
(GiB의 B는 Byte를 나타낸다.)

### 풀이

9.6Gi(기비)는 $9.6 \cdot 2^{30}$이다. 즉, $9.6$GiB(기비바이트)는 $9.6 \cdot 2^{30}$byte이다.  
그런데, 비트(bit)로 표현해야 하므로, DVD-ROM은 $76.8 \cdot 2^{30}$ bit를 저장할 수 있다.  