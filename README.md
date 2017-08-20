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

    
출처 : <http://www.differencebetween.com/difference-between-api-and-vs-sdk/>
    
## 1.2 javascript SDK로 로그인하기
facebook은 SDK 형태로 제공해주므로 가져다가 쓰면 된다.

<https://developers.facebook.com/docs/javascript>
    
## 1.3 login button 붙이기
로그인 버튼은 기본적으로 간단하게 웹페이지에 넣을 수 있도록 코드를 facebook이 제공한다. BUT 굉장히 아름답지 못하다...

그냥 button 하나 만들고 onclick 이벤트로 javascript function 구동시키는 방법을 추천. 로그아웃도 마찬가지.. iframe에 css 입혀보려다가 똥망..

<https://developers.facebook.com/docs/facebook-login/web/login-button>


# 2. Google login
## 2.1 Google
페이스북을 한 번 해보고 나서 그런가 google login 하기는 facebook보다 좀 더 쉬운 느낌이다. 아래 출처의 가이드를 따라 가면 된다. 

> 디버깅 :: 401에러가 뜨면 앱의 Client ID가 제대로 적혀져있는지 확인한다.

<https://developers.google.com/identity/sign-in/web/devconsole-project>

## 2.2 login button 커스터마이징
> 총 두가지 방법이 있는 것 같다. render라는 function을 이용해 google이 어느정도 정해주는 가이드 안에서 변경을 하는 방법이랑
> 아예 자유롭게 html, css, js를 커스터마이징 할 수 있는 방법. 전자의 것을 이용해서 하려고 했더니 어떤 속성을 건드릴 수 있는 건지 잘 모르겠어서(그 내용이 어디에 적혀있는지도 잘 모르겠어서) render는 한번 코드 써서 되는지만 확인해보고 그냥 자유롭게 커스텀 할 수 있는 방법으로 최종적으로 적용해볼까 함.

<https://developers.google.com/identity/sign-in/web/build-button>

### ++ 주절주절
중간쯤에 유저 정보 가져오는 부분에서 아래와 같은 주의사항이 발견되는데 정확히 무슨 소린지 잘 모르겠다. user ID 가져오지 말고 ID token을 서버로 보내라고 하는 것 같은데 이게 우리 서버를 말하는 건지 아니면 google 쪽 서버를 얘기하는 건지 잘 모르겠다. current user에서 getId로 정보를 그냥 들고와서 이미지나 아이디를 찾지 말고 ID token을 보내서 찾으라는 건가. 그게 더 정확하다는 건가.

Important: Do not use the Google IDs returned by getId() or the user's profile information to communicate the currently signed in user to your backend server. Instead, send ID tokens, which can be securely validated on the server.