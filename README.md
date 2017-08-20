[SNS login] 여러가지 SNS로 로그인하기
==========

# 1. facebook javascript로 로그인 하기
## 1.1 SDK와 API는 무엇인가
    > API vs SDK 
    > API (Application Programming Interface) is an interface that allows software programs to interact with each other. 
    > API (Application Programming Interface)는 인터페이스다, 어떤 인터페이스냐면 그것은 허가한다, 소프트웨어 프로그램들이 서로 인터렉트 하게끔.
    > It defines a set of rules that should be followed by the programs to communicate with each other.
    > 그것은 정의한다, 규칙을, 반드시 지켜야할, 프로그램들이, 서로 소통하기 위해서.
    > APIs can be used to communicate between software applications, libraries and operating systems. 
    > API들은 사용될 수 있다, 소통하기 위해서 사이에 소프트웨어 어플리케이션, 라이브러리 그리고 operating system들.
    > SDK (Software Development Kit) is a set of tools that can be used to develop software applications targeting a specific platform.
    > SDK는 공구 셋트다, 사용될 수 있는, 소프트웨어 어플리케이션을 만들때, 특별한 platform을 겨냥한.
    > SDKs would include debugging tools and other utilities to aid the programmers and all of these are presented as an IDE (Integrated Development Environment).
    > SDK들은 디버깅 도구들과 다른 도구들을 포함하고 있다, 프로그래머들을 돕도록, 그리고 이 모든 것들은 표시된다 IDE에서.
    
    
    출처 : http://www.differencebetween.com/difference-between-api-and-vs-sdk/
    
## 1.2 javascript SDK로 로그인하기
    facebook은 SDK 형태로 제공해주므로 가져다가 쓰면 된다.
    
    https://developers.facebook.com/docs/javascript
    
## 1.3 login button 붙이기
    로그인 버튼은 기본적으로 간단하게 웹페이지에 넣을 수 있도록 코드를 facebook이 제공한다. BUT 굉장히 아름답지 못하다...
    
    그냥 button 하나 만들고 onclick 이벤트로 javascript function 구동시키는 방법을 추천. 로그아웃도 마찬가지.. iframe에 css 입혀보려다가 똥망..
    
    https://developers.facebook.com/docs/facebook-login/web/login-button