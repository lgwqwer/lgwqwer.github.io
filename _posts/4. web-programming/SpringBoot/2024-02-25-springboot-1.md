---
layout: single
title: '[Springboot] Spring Boot 프로젝트 세팅'
categories:
  - spring-boot
comments: true
use_math: true
---

<br>

# - TMI

'웹 기반 기숙사 추천 플랫폼' 이라는 주제로 웹 개발 프로젝트를 진행하다가, 서버쪽 개발 플랫폼을 무엇으로 할지 고민이 많았다.  

마침 다음 학기 커리큘럼이 Java 프로그래밍 이기도 하고, 요즘 실무에서 많이 쓰이는 자바 프레임워크가 Spring이기에, Spring으로 서버 구현을 하기로 했다.

Spring과 Spring boot의 명확한 차이는 아직 잘 모르겠다.  
하지만 여러 구글링을 해본 결과, Spring Boot가 조금 더 가볍고 편리한 기능이 많다고 판단이 들어, 입문자들인 우리 팀은 Spring boot로 프로젝트를 진행했다.  

미리 말하지만 우리 팀은 전문적인 지식을 가지고 프로젝트를 시작하는 것이 아닌, 무(無)에서 부터 시작하는 입문자들이기에 옵션 하나하나가 무슨 의미인지 정확히 알지 못한다.  
여러 인강을 통해 세팅하는 방법을 따라한 것 뿐이다.

그럼 이제 이제 Spring Boot의 프로젝트 세팅 방법을 알아보자.

<br>

# - 프로젝트 세팅

![image](https://github.com/lgwqwer/lgwqwer.github.io/assets/129755540/fcfee482-9013-4587-ba5e-0f81866a6d2e)

우선 원하는 위치에 프로젝트 파일을 넣을 디렉토리를 하나 생성한다.
<hr>
<br>

![image](https://github.com/lgwqwer/lgwqwer.github.io/assets/129755540/ce9228ed-d5f0-412d-8ba2-30a316c92487)

그 다음에 구글에 Spring initializr 사이트에 들어간다.

<hr>
<br>

![image](https://github.com/lgwqwer/lgwqwer.github.io/assets/129755540/d39df875-bdf1-4316-b8a2-ad8fb129eb16)

들어가면 이런 화면이 뜰 텐데, 뭔가 복잡한 것들이 많아보인다.  
그래도 한번 해보자.

Project에 있는 Gradle, Maven은 프로젝트에서 필요한 여러 파일들을 자동으로 인식해서 빌드해주는 '빌드 관리 툴'이다.  
사실 나도 아직은 이게 뭔지 잘 모른다. 이게 정확히 뭔지는 차후에 공부해보자.  
일단 Gradle로 하는게 좋다고 한다.

Spring Boot 버전은 그냥 기본 설정되어있는 걸로 했다.

우리는 Java를 쓸 것이기에 Language는 Java로 선택하고,
Group은 보통 기업 명이나 회사 명을 쓴다고 한다.  
(나는 우리 프로젝트 팀명으로 대충 넣어놨다.)

Artifact는 그냥 프로젝트 명 같은 느낌이라고 한다.

밑에 좀 잘렸는데, Packaging은 **Jar**로 선택했고, 자바 버전은 **17**버전으로 진행했다. 
<hr>
<br>

![image](https://github.com/lgwqwer/lgwqwer.github.io/assets/129755540/cf0a608f-086b-4ced-a7a4-0611c9afa445)

중요한 것은 저 부분이다.  
Dependencies.. 의존성? 뭔가 어려운 단어가 나왔다.  
일단은 라이브러리를 가져와서 쓸 수 있게 하는 부분인 것 같다. 

<hr>
<br>

![image](https://github.com/lgwqwer/lgwqwer.github.io/assets/129755540/e3fdc5f7-cdbe-43dc-99ab-dce696a7c09f)

눌러보면 이런식으로 라이브러리를 추가할 수 있게 된다.  
우리는 웹 개발 프로젝트이기에 Spring Web을 추가한다.  

<hr>
<br>

![image](https://github.com/lgwqwer/lgwqwer.github.io/assets/129755540/a8ff776b-5143-4eeb-831c-2acba6d22f2b)

추가하면 저런식으로 뜨게 된다.  

우리 프로젝트는 SPA(Single Page Aplication)를 구현할 정도의 수준이 되지 못하기에, SSR(Server Side Rendering)방식으로 진행 할 것이다.  
SSR방식에 잘 맞는 Thymeleaf 템플릿 엔진을 하나 더 추가했다.  

이제 GENERATE 버튼을 눌러준다!

<hr>
<br>

![image](https://github.com/lgwqwer/lgwqwer.github.io/assets/129755540/e34ecfd1-14c5-4c64-b7db-f1978f6c5c98)

필자는 앞전에 몇 번 세팅했었어서 다운로드 파일이 몇 개 있는데, 일단 저런식으로 프로젝트 파일이 다운로드 될 것이다.

저걸 아까 만들어둔 디렉터리에 압축 풀기한다.

<hr>
<br>

![image](https://github.com/lgwqwer/lgwqwer.github.io/assets/129755540/b5e27dd7-c076-41af-bf08-586e23e15a72)


이제 Java IDE인 intellij에서 프로젝트 파일을 열어주면 저렇게 뜰 것이다.  
거의 다 왔다! 이제 과정 하나만 더 진행하면 세팅이 완료된다. 

<hr>
<br>

![image](https://github.com/lgwqwer/lgwqwer.github.io/assets/129755540/c0fbcfa6-1796-445e-9442-75a6c8f9aa78)


File -> Project Structure -> Project Setting -> Project에 가면 자바 버전을 맞출 수 있는 옵션이 있을 것이다.  

아까 자바 17버전으로 프로젝트를 만들었으므로, 17버전을 맞추면 된다.  

**로컬 자바 버전을 꼭 확인해주길 바란다.**

프로젝트 세팅 끝!


