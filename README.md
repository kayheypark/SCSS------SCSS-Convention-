# SCSS 코딩 컨벤션

### 1. 네이밍(Naming)

+ #### 클래스(Class)

    **스네이크 표기법**(Snake Case)으로 소문자와 언더스코어(_)로 작성
    
    ```scss
    //GOOD
    .nav_wrap

    //BAD
    .nav-wrap
    ```

+ #### 아이디(Id)

    **파스칼 표기법**(Pascal Case)으로 대문자와 소문자로 작성
    
    ```scss
    //GOOD
    #UserName

    //BAD
    #user_name
    ```

### 2. 재활용(Recycle)


스타일을 적용받는 노드를 **저격**하여 스타일을 작성함

```scss
//GOOD
.login_button { color: red; }

//BAD
.login button { color: red; }
```
     
### 3. 템플릿 오버라이팅

템플릿과 똑같은 선택자를 주어 오버라이팅

템플릿
```scss
nav.navigation-wrap.sticky { background-color: black; }
```

GOOD
```scss
nav.navigation-wrap.sticky { background-color: red; } (선택자가 똑같음)
```
BAD
```scss
.sticky { background-color: red !important; } (임폴턴트 사용)
```
