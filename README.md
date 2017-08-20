[SNS login] 여러가지 SNS로 로그인하기
==========

# 1. facebook javascript로 로그인 하기
## 1.1 SDK와 API는 무엇인가
> API vs SDK 
> API (Application Programming Interface) is an interface that allows software programs to interact with each other. 
> It defines a set of rules that should be followed by the programs to communicate with each other.
> APIs can be used to communicate between software applications, libraries and operating systems. 
> SDK (Software Development Kit) is a set of tools that can be used to develop software applications targeting a specific platform.
> SDKs would include debugging tools and other utilities to aid the programmers and all of these are presented as an IDE (Integrated Development Environment).

> API (Application Programming Interface)는 인터페이스다. API는 소프트웨어 프로그램들이 서로 인터렉트 하게끔 허가한다.
> SDK는 공구 셋트다.

    
출처 : http://www.differencebetween.com/difference-between-api-and-vs-sdk/
    
## 1.2 javascript SDK로 로그인하기
facebook은 SDK 형태로 제공해주므로 가져다가 쓰면 된다.

https://developers.facebook.com/docs/javascript
    
## 1.3 login button 붙이기
로그인 버튼은 기본적으로 간단하게 웹페이지에 넣을 수 있도록 코드를 facebook이 제공한다. BUT 굉장히 아름답지 못하다...

그냥 button 하나 만들고 onclick 이벤트로 javascript function 구동시키는 방법을 추천. 로그아웃도 마찬가지.. iframe에 css 입혀보려다가 똥망..

https://developers.facebook.com/docs/facebook-login/web/login-button