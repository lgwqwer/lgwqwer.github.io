---
layout: single
title: '깃허브 활용 방법'
categories:
  - dormitory-project
comments: true
use_math: true
---

<br>

# 2024-01-19 회의 목적
> 깃허브 활용 방법 숙지  

<br>

# 깃허브 활용 방법 숙지

<br>

## 1. 로컬 저장소를 만들 루트 파일 만들기

![image](https://github.com/lgwqwer/lgwqwer.github.io/assets/129755540/e1707a7f-b01d-4e2a-9545-207112ae3ff5)
각자 로컬 PC에서 원하는 위치(본인이 경로를 인지하고 있는 위치)에 로컬 저장소를 만들 파일을 생성한다. 

<hr>
<br>

## 2. 루트 파일에 들어가서 git bash를 실행한다

![image](https://github.com/lgwqwer/lgwqwer.github.io/assets/129755540/fce21db6-8205-4454-968c-c418a1d33afe)

<hr>
<br>

## 3. git 초기화를 하여 로컬 저장소 만들기

![image](https://github.com/lgwqwer/lgwqwer.github.io/assets/129755540/78f05fc7-d8f0-422b-a826-b84b0cb9e6fa)

git bash를 실행하고, git init 명령어를 입력한다.  
(노란색 글자 부분은 현재 경로를 의미한다.)

<hr>
<br>

![image](https://github.com/lgwqwer/lgwqwer.github.io/assets/129755540/57f6722f-1839-4f17-895f-0d17c58ec5d4)


파일에 .git이 생겼을 것이다. -> 로컬 저장소를 만들었다는 의미!

## 4. git remote add origin "리포지토리 주소" 명령어로 로컬 저장소와 리포지토리 연결하기

![image](https://github.com/lgwqwer/lgwqwer.github.io/assets/129755540/631f1926-0316-4dce-bfc8-b5b8b8771a86)

여기에 있는 "리포지토리 주소"는 깃허브 리포지토리에 가서 Code를 누르고 복사해오면 된다.

![image](https://github.com/lgwqwer/lgwqwer.github.io/assets/129755540/8b3b881f-0ea3-403f-85dd-e4428ebb2a40)

참고로 git에서 붙여넣기는 "shift + insert"키 이다.

<hr>
<br>

## 5. git remote -v를 통해 잘 연결됐는지 확인

![image](https://github.com/lgwqwer/lgwqwer.github.io/assets/129755540/b95bc1be-2c3c-48de-812b-55f4d8b1446d)

이런식으로 잘 뜨면 성공

<hr>
<br>

## 6. git pull origin "브랜치 명" 명령어로 리포지토리에 있는 프로젝트 파일들을 내 로컬 저장소에 가져오기

![image](https://github.com/lgwqwer/lgwqwer.github.io/assets/129755540/92497061-d04e-4bc9-ad91-8574e2e64c11)

우리는 master 브랜치에 있는 파일들을 가져올 것이기 때문에  
git pull origin **master** 명령어를 치면 된다.  

<hr>
<br>

![image](https://github.com/lgwqwer/lgwqwer.github.io/assets/129755540/e88430a0-f300-48f8-916d-46d0a608b3fe)

다음과 같이 로컬 저장소에 파일이 생성되면 성공

<hr>
<br>

![image](https://github.com/lgwqwer/lgwqwer.github.io/assets/129755540/5bb00aa4-be95-42a3-a923-0713a7987bcd)


깃허브에 들어가서 master 브랜치의 파일들과 일치한지 한번 더 확인

<hr>
<br>

## 7. vscode와 연결

![image](https://github.com/lgwqwer/lgwqwer.github.io/assets/129755540/20e21f07-b256-440e-bd87-00c77c5994a1)

vscode를 들어가서 폴더 열기를 눌러준다. 

<hr>
<br>

![image](https://github.com/lgwqwer/lgwqwer.github.io/assets/129755540/fb21a4ad-5a34-4efb-af88-1380659069e0)

아까 로컬 저장소를 만들어뒀던 경로로 가서 폴더를 선택한다. 

<hr>
<br>

![image](https://github.com/lgwqwer/lgwqwer.github.io/assets/129755540/9d190793-7296-41ef-b890-b64ad9302b0a)

이런식으로 master 브랜치에 있던 파일들이 내 로컬 IDE에 불러와졌으면 성공

<hr>
<br>

## 8. 푸시(push)를 해보자
![image](https://github.com/lgwqwer/lgwqwer.github.io/assets/129755540/536c3125-22cc-44c3-bec9-2158c723d3b5)
파일에 변경사항이 생긴다면, 반드시 커밋(commit)을 해줘야 한다.   
커밋은 체크포인트 같은 개념이다.


<hr>
<br>

![image](https://github.com/lgwqwer/lgwqwer.github.io/assets/129755540/41616a64-5b19-4b12-8140-06c0f0408080)

변경 사항이 생기고 "ctrl + s"를 통해 저장을 해주면, 다음과 같이 소스 제어 탭에 표시가 생길 것이다.

<hr>
<br>

![image](https://github.com/lgwqwer/lgwqwer.github.io/assets/129755540/e0414c0f-35bd-4078-b0db-48fcc600e80e)

소스 제어 탭을 누르면 다음과 같은 화면이 뜰 것이다.  
별표 친 부분은 커밋메세지를 남기는 공간이고, 밑에 커밋 버튼으로 커밋을 진행하면 된다.

<hr>
<br>

![image](https://github.com/lgwqwer/lgwqwer.github.io/assets/129755540/4f025b00-79f4-4075-a538-2285fd2e6b60)

긍정적인 대답을 해주면 된다.

<hr>
<br>

![image](https://github.com/lgwqwer/lgwqwer.github.io/assets/129755540/d22ea8bd-0e9c-4446-8b08-a732482e036c)

마지막으로 저 버튼을 눌러주면 푸시(push)가 된다.

> 푸시(push)는 파일의 변경 사항이 생기기 전 깃발을 꽃고(commit), 변경 사항 후의 파일을 브랜치에 밀어 넣는(push) 과정을 말한다. 

<hr>
<br>

![image](https://github.com/lgwqwer/lgwqwer.github.io/assets/129755540/a6bd0110-d8c7-4d0b-80be-b73d9198e38e)

마지막으로 깃허브에 돌아가서 파일이 수정이 됐는지 확인하면 성공!

<hr>
<br>

## 과제

1. vscode에서 브랜치를 직접 지정하여 pull/push    하는 방법을 숙지하고, develop 브랜치의 파일들을 본인 로컬 저장소에 불러오기
   
2. develop 브랜치의 README 파일에다가 각자 이름을 적고, push 해보기.   
  (오류가 생긴다면 이유를 분석하고 해결하기)


