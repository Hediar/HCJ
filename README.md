# HCJ
HTML,CSS,JS 복습
참조: 생활코딩 https://opentutorials.org/course/3083 

# HTML

Notion 정리 : [https://deeply-silence-9a4.notion.site/HTML-c5fc73aec3b040bb81d92dd4b524d8d6](https://deeply-silence-9a4.notion.site/HTML-CSS-JS-2e0de702f7fb40c3976811ef53f70c73)

### 처음 만들어보고 수행해보기

1.html

```html
Hello world
```

브라우저로 여는 법 : Ctrl + O

글자 그대로 나옴


### 태그

<> ~ </> 로 작성하며 안에 들어간 것을 특정한 명령 수행

- 기본 태그
    
    <!DOCTYPE html> : 문서 유형을 html로 지정
    
    <html lang="ko"> : 문서를 html로 시작, 언어를 한국어로 지정
    
    <head> : 주로 브라우저의 정보를 입력
    
    <body> : 문서 내용 입력
    
- 문서 구조 태그
    
    <header>
    
    <main>
    
    <section>
    
    <aside>
    
    <footer>
    
    <nav>
    
    <article>
    
    <section>
    
    <div>
    
- 내용 입력

# CSS
스타일 시트 내에서는 세미콜론으로 구분함!

- 주석처리 태그
    
    <!— —>
    
- 스타일 태그
    
    <style> </style> 
    
    HTML의 문
    
    ```html
    <style>
        a {
        color: red;}
    </style>
    ```
    
    ⇒ a태그의 글자색을 빨간색으로 변경하는 예시 
    
- 링크 밑줄 없애기
    
    ```html
    <style>
    text-decoration: none;
    </style>
    ```
    
- 선택자(css selector)
    
    특정 요소들을 어떻게 렌더링 할 것인지 알려줌 
    
    - ex) 모든 링크 기본: 검정,  방문했던 것 : 회색, 현재 페이지: 빨강
    - 클래스 지정
        
        ```html
        <style>
        .saw {
        		color: gray;
        }
        </style>
        
        <a href="1.html" class="saw">HTML</a>
        <!--해당 클래스만 설정가능-->
        ```
        
        ⇒ . (점)을 앞에 붙이면 웹 페이지에서 class가 saw인 모든 태그를 가짐 
        
        띄어쓰기로 클래스 구분 
        
        순서에 따라 동작이 바뀜 saw active로 설정할 경우 active가 마지막으로 적용됨 → 선언문의 순서에 따라 .~{} 부분 
        
    - 선택자 우선순위
        
        id 선택자 > class 선택자 > tag 선택자 
        
        같은 형태의 선택자의 경우 가장 마지막이 우선순위가 높다. 
        
    - id 선택자
        
        웹 페이지에서 한번만 사용 가능 
        
        ```html
        <!--스타일 시트-->
        #active{ color: red; }
        
        <!--body 내-->
        < ~~~ id="active"> ~~
        ```
        
- 박스 모델
    - 테두리 만들기
        
        ```html
        border: 1px solid gray; #전체박스
        ```
        
        margin값 사용함
        
        padding으로 글자와의 간격 조절 가능 
        
        개발자 도구를 켜서 margin과 padding값을 볼 수 있다.
        
        1. 아래 테두리
            
            ```html
            border-bottom: 1px solid gray #아래 밑줄만 있는 박스 
            ```
            
            
            ⇒ margin 0, padding 20px

        - 중복 제거
    
    중복되는 것은 ,(콤마)를 이용하여 사용가능
    
    ```html
    h1, a {
                    border-width: 5px;
                    border-color: red;
                    border-style: solid;
                }
    ```
    
    ```html
    h1, a {
                    border: 5px solid red;
                }
    ```
    
    ⇒ 같은 결과로 출력됨
   
- 콘텐츠와 테두리 사이에 여백 추가하기
    
    ```html
    h1 {
                    border: 5px solid red;
                    padding: 20px;
    }
    ```
    - 박스 모델
    - 테두리 만들기
        
        ```html
        border: 1px solid gray; #전체박스
        ```
        
        margin값 사용함
        
        padding으로 글자와의 간격 조절 가능 
        
        개발자 도구를 켜서 margin과 padding값을 볼 수 있다.
        
        1. 아래 테두리
            
            ```html
            border-bottom: 1px solid gray #아래 밑줄만 있는 박스 
            ```
            
            
            ⇒ margin 0, padding 20px
            
            
        
    - 중복 제거
        
        중복되는 것은 ,(콤마)를 이용하여 사용가능
        
        ```html
        h1, a {
                        border-width: 5px;
                        border-color: red;
                        border-style: solid;
                    }
        ```
        
        ```html
        h1, a {
                        border: 5px solid red;
                    }
        ```
        
        ⇒ 같은 결과로 출력됨 
        
    - 콘텐츠와 테두리 사이에 여백 추가하기
        
        ```html
        h1 {
                        border: 5px solid red;
                        padding: 20px;
        }
        ```
        
        
    - 테두리와 테두리 사이의 간격
        
        ```html
        <!DOCTYPE HTML>
        <html>
            <head>
                <meta charset="utf-8">
                <title></title>
                <style>
                    h1 {
                        border: 5px solid red;
                        padding: 20px;
                        
                    }
                </style>
            </head>
            <body>
                <h1>CSS</h1>
                <h1>CSS</h1>
            </body>
        </html>
        ```
        
        
    - 너비 (width)
        
        ```html
        <!DOCTYPE HTML>
        <html>
            <head>
                <meta charset="utf-8">
                <title></title>
                <style>
                    h1 {
                        border: 5px solid red;
                        padding: 20px;
                        margin: 20px;
                        display: block;
                        width: 100px;
                    }
                </style>
            </head>
            <body>
                <h1>CSS</h1>
                <h1>CSS</h1>
            </body>
        </html>
        ```

        
- 그리드
    - <div> : division의 약자
        
        화면 전체 사용, 묶어주는 개념 
        
    - <span> : inline태그
    
    나란히 두기 위해 부모 태그를 만들어 사용한다면?
    
    ```html
    <!DOCTYPE html>
    <html>
        <head>
            <meta charset="uft-8">
            <title></title>
            <style>
                #grid {
                    border: 5px solid pink;
                }
                div {
                    border: 5px solid gray;
                }
            </style>
        </head>
        <body>
            <div id="grid">
            <div>NAVIGATION</div>
            <div>ARTICLE</div>
            </div>
        </body>
    </html>
    ```
    
    
    - grid 속성
        
        스타일 태그 내 display속성에서 grid 설정하기 
        
        ```html
        <!DOCTYPE html>
        <html>
            <head>
                <meta charset="uft-8">
                <title></title>
                <style>
                    #grid {
                        border: 5px solid pink;
                        display: grid;
                        grid-template-columns: 150px 1fr;
                    }
                    div {
                        border: 5px solid gray;
                    }
                </style>
            </head>
            <body>
                <div id="grid">
                    <div>NAVIGATION</div>
                    <div>ARTICLE</div>
                </div>
            </body>
        </html>
        ```
        
        
    - grid-template-columns
        
        : navigation은 ~px정도 가짐, article은 1fr(나머지 공간을 다 사용한다.)
        
        fr: 화면의 크기에서 어떤 비율만큼 자동으로 조정해줌 
        
    - grid 밑에 특정 태그
        
        ```css
        #grid ol{
                        padding-left: 33px;
                    }
        #그리드 밑에 있는 ol태그에 적용
        ```
        
- 반응형 디자인
    
    화면에 크기에 따라 최적화된 모양으로 변하게 만드는 것 
    
    - 화면 크기 보는법
        
        우클릭 → 검사 
        
    - media()
        
        ```css
        @media(min-width:800px){
                        div {
                            display: none;
                        }
                    }
        ```
        
        min-width:800px ⇒ 800px보다 크다 
        
        max-width:800px ⇒ 800px보다 작다 
        
    - 2.html 개편
        
        작아지면 선이 없어지고 본문이 아래로 내려가도록, 작게 만들기

    
