---
layout: single
title: '[Logic Design] ADC와 DAC'

categories:
  - logic-design

toc_label: 디지털 시스템
toc: true
toc_sticky: true

date: 2024-03-10
last_modified_at: 2024-03-10

comments: true
use_math: true
---

ADC와 DAC에 대해서 알아보도록 하자.  

<br>

# - ADC와 DAC

ADC와 DAC는 아날로그-디지털 신호를 변환해주는 변환기라고 앞서 설명했다.  

변환기의 변환 과정을 간단하게 살펴보자.  

아날로그 신호를 디지털 신호로 변환하는 과정은 표본화 -> 양자화 -> 부호화로 구성되어 있다. 

이름부터 무섭다.. 변환 과정의 예시를 보면서 하나하나 살펴보도록 하자.  

## 1. 표본화(Sampling)

![S 2024-03-07 11_56_45](https://github.com/lgwqwer/lgwqwer.github.io/assets/129755540/79c88921-f1ff-48cc-b6c0-89caa3a79012)

저런식으로 단위시간(T)을 지정하여, <font color='tomato'>몇 번</font> 데이터(대표값)를 추출할 것인지 정하는 것이다.  

위 그래프는 아날로그 신호를 8번의 단위시간으로 쪼개어 샘플링을 진행했다.  

<br>
<hr>

## 2. 양자화(Quantization)

![s 2024-03-07 12_03_09](https://github.com/lgwqwer/lgwqwer.github.io/assets/129755540/7fcf2275-b030-4268-a8af-428010f0649a)

샘플링한 데이터(아날로그 신호의 값)들을 디지털화 하기 위해 <font color='tomato'>이산적인 값</font>으로 변환한다. 

위 그래프는 샘플링한 데이터를 반올림하여 디지털 값으로 근사시켰다.  

<br>
<hr>

## 3. 부호화(Coding)

![s 2024-03-07 12_06_56](https://github.com/lgwqwer/lgwqwer.github.io/assets/129755540/2e510d4e-6937-44b4-a456-f35fc0da52be)

디지털화 된 데이터들을 2진수 비트로 변환하는 과정을 말한다.  

\+ '부호화'라는 용어 자체는 무언가 1대1 대응되게 매칭하는 것을 의미한다.  
ex) encoding, decoding

</details>
