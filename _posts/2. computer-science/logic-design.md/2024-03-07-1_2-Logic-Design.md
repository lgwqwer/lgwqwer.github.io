---
layout: single
title: '[논리설계] Ch 1.2 디지털 정보를 표현하는 방법'

categories:
  - logic-design

toc_label: 디지털 정보를 표현하는 방법
toc: true
toc_sticky: true

date: 2024-03-07
last_modified_at: 2024-03-07

comments: true
use_math: true
---
앞 챕터에서 말했다시피, 디지털은 정보를 이산적인 방식으로 처리한다고 했다.  
디지털 정보(0, 1)를 표현하는 여러가지 방법을 알아보자.

<br>

# 1. 디지털 정보의 전압레벨 

디지털 시스템은 보통 이진수 체계(Binary System)을 사용한다.   

0과 1만의 디지트(digit)를 사용한다.  

![이름 없는 노트북 2024-03-07 06_43_22](https://github.com/lgwqwer/lgwqwer.github.io/assets/129755540/fd49f219-0b25-42c0-8ba9-f16879c69b73)

위 그래프와 같이, 높은 범위, 낮은 범위를 설정하고, 그 높은 범위에 속하면 1, 낮은 범위에 속하면 0으로 정보를 처리한다.

<br>

# 2. 디지털 정보의 표현 단위

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

# 3. SI 단위와 IEC 단위 비교
![image](https://github.com/lgwqwer/lgwqwer.github.io/assets/129755540/4c84fd17-0b5d-4d49-baf8-1a84515b1ce9)  
(출처: 위키디피아)

우리는 줄곧 1,000단위를 K(킬로), 1,000,000를 M(메가), 1,000,000,000은 G(기가) 등등 여러 10진 단위를 사용해왔다.  

그 10진 단위를 SI 단위라고 한다.  
추가로, 10진 단위는 [밑 수](https://ko.wikipedia.org/wiki/%EB%B0%91%EC%88%98)가 10인 단위를 의미한다.  


하지만, 디지털 세계에서는 2진수로 표현하므로, 단위가 조금 다르다.  

![image](https://github.com/lgwqwer/lgwqwer.github.io/assets/129755540/7ada8632-c252-4bde-908d-3f18c2cdd697)  
(출처: 위키디피아)


밑 수가 2인 단위를 2진 단위라고 하고, 그 2진 단위를 IEC 단위라고 한다.  

Ki(키비)/K(킬로), Mi(메비)/M(메가), ... SI 단위랑 IEC 단위랑 뭔가 비슷해보인다.  

그러나 밑 수가 다르기 떄문에, 약간의 오차가 있는 것을 알 수 있다. 

예제를 한번 풀어보자.  

## 예제

일반 DVD-ROM은 9.6GiB의 디지털 데이터를 저장할 수 있다.  
DVD-ROM에는 얼마나 많은 데이터(bit)가 저장 되는가?   
(GiB의 B는 Byte를 나타낸다.)


<details>
  <summary><font color='tomato'>풀이</font></summary>
  
9.6Gi(기비)는 $9.6 \cdot 2^{30}$이다. 즉, $9.6$GiB(기비바이트)는 $9.6 \cdot 2^{30}$byte이다. <br>
그런데, 1 byte = 8 bit이므로, DVD-ROM은 $76.8 \cdot 2^{30}$ bit를 저장할 수 있다.  

</details>

<br>

# 4. 전자 소자를 이용한 논리 표현  

## 4-1 다이오드에 의한 스위칭

![LogicDesign1 2024-03-07 09_56_49](https://github.com/lgwqwer/lgwqwer.github.io/assets/129755540/8452464b-d8b2-475d-bce5-3c96c0740c34)

$V_s$로 걸어주는 전압이 5[V]면 a -> b 로 가는 D지점이 연결이 되어 스위치가 ON이 된다.

반대로, 걸어주는 전압이 0[V]면 a -> b 로 가는 D지점이 끊어지기 때문에, 스위치가 OFF 된다.  

<hr>

## 4-2 쌍극성 트랜지스터에 의한 스위칭

![LD2 2024-03-07 09_58_44](https://github.com/lgwqwer/lgwqwer.github.io/assets/129755540/2094974b-22f0-4a98-9409-cd9fe01d29b4)

저런식으로 특정 지점이 끊겨있지 않으면, 아래로 전류가 흐르게 되어, $V_o$가 전류량이 0이 된다.  

$V_0$의 전류량이 1이 되기 위해서는 저 특정 지점이 끊겨있어야 한다. 

우리는 전기/전자 공학과가 아니기 떄문에 저런식으로 구성된다는 것만 알아두면 된다.  

## 4-3 NMOS 트랜지스터에 의한 스위칭

![LD3 2024-03-07 10_07_21](https://github.com/lgwqwer/lgwqwer.github.io/assets/129755540/3ec5baf2-cfde-4b0d-ba40-89929ca133df)

필자도 뭔지 모른다. 그냥 올린 거다.  
넘어가자.. 