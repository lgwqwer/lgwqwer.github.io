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

반대로, 걸어주는 전압이 0[V]면 a -> b 로 가는 D지점이 끊이지기 때문에, 스위치가 OFF 된다.  

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

## - 펄스 파형

