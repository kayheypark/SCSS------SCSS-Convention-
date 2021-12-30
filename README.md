# SCSS 코딩 컨벤션

<br>

### 1. 네이밍(Naming)

+ #### 클래스(Class)

    **스네이크 표기법**(Snake Case)으로 소문자와 언더스코어(_)로 작성
    
    ```scss
    //GOOD
    .nav_wrap

    //BAD
    .nav-wrap
    ```
    <br>

+ #### 아이디(Id)

    **파스칼 표기법**(Pascal Case)으로 대문자와 소문자로 작성
    
    ```scss
    //GOOD
    #UserName

    //BAD
    #user_name
    ```
    > ※ 아이디로 스타일을 주지 마세요! 아이디는 개발자가 임의로 수정할 수 있습니다!
    <br>

### 2. 재활용(Recycle)

스타일을 **적용받는 노드를 저격**하여 스타일을 작성함

```scss
//GOOD
.login_button { color: red; }

//BAD
.login button { color: red; }
```
> 브라우저는 'Nesting 구조를 해석하는 속도'보다 '클래스명을 직접 찾는 속도'가 더 빠릅니다.
<br>

### 3. 다른 작성자 오버라이팅 (Vendor Overwriting)

템플릿 혹은 플러그인 등 다른 사람에 의하여 작성된 **똑같은 선택자**를 주어 오버라이팅

```scss
//Vendor
#navigation.sticky { background-color: black; }

//GOOD
#navigation.sticky { background-color: red; } //선택자가 똑같음

//BAD
.sticky { background-color: red !important; } //임폴턴트 사용
```
<br>