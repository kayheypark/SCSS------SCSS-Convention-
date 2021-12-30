﻿# SCSS 코딩 컨벤션
------------
## 1. 네이밍

+ 클래스
    > class명은 '스네이크 표현법'으로 소문자와 언더스코어(_)로 작성

    **예시**
    GOOD
    ```
    ```.nav_wrap
    ```
    BAD
    ```
    .nav-wrap
    ```

+ 아이디
    > id명은 '파스칼 표현법'으로 대문자와 소문자로 작성

    **예시**
    GOOD
    ```
    #UserName
    ```
    BAD
    ```
    #user_name
    ```

## 2. 재활용

> 스타일을 적용받는 노드를 저격하여 스타일을 작성함

**예시**

GOOD
```
```.login_button { color: red; }
```
BAD
```
.login button { color: red; }
```
     
## 3. 템플릿 오버라이팅

> 템플릿과 똑같은 선택자를 주어 오버라이팅

**예시**

템플릿
```
nav.navigation-wrap.sticky { background-color: black; }
```

GOOD
```
nav.navigation-wrap.sticky { background-color: red; } (선택자가 똑같음)
```
BAD
```
.sticky { background-color: red !important; } (임폴턴트 사용)
```
