# 01)_HTML & CSS

## HTML 기본태그 

``` txt 

h : 글제목 
p : 본문 
button : 버튼 태그 
a : 링크 태그 / href : 링크 입력
ul, li : 리스트 태그
img : 이미지 태그 
src 이미지 경로 // alt : 이미지를 보여줄수 없을때 텍스트로 대처

```

## Tag 이용 
```html

 <h1>글 제목</h1>
    <p>본문</p>
    <button>버튼 태그</button>
    <!-- 링크  -->
    <a href="https://google.com">링크</a>
   
    <!-- 리스트 -->
   <ul>
    <li>항목1</li>
    <li>항목2</li>
   </ul>
    <!-- src: 이미지 경로 // alt : 이미지를 보여줄수 없을때 텍스트로 대처-->
    <img src="img.png" alt="">
    <h2>랑크로 이미지 대처</h2>
   <!-- 링크를 이미지로 대처 -->
    <a href="https://google.com">
        <img src="img.png" alt="">
    </a>

```
## 과제1 : 글자 일부를 누르면 이동
``` html
<h2>
    과제 입니다. 
    <a href="https://naver.com">
        이동하기
    </a>
</h2>

```

## 기본적인 웹페이즈 스타일링

```txt

이미지 가운데 정렬 : display: block; margin-left: auto; margin-right: auto
font 사이즈 vw :  현재 브라우저 창의 너비 // %: 내 부모태그의 사이즈에 비례
자간 사이즈 : letter-spacing
font 가운데 정렬 : font-align : center

글자 굵기 : font-weight or stong

```

```html 
 <!-- 이미지 가운데 정렬 : display: block; margin-left: auto; margin-right: auto -->
    <img src="lion.png" style="display: block; margin-left: auto; margin-right: auto;">

    <!-- font 사이즈 vw :  현재 브라우저 창의 너비 // %: 내 부모태그의 사이즈에 비례 -->
    <!-- 자간 사이즈 : letter-spacing-->
    <!-- font 가운데 정렬 : font-align : center -->
    <h3 style="letter-spacing: 5px; text-align: center;">LION</h3>
    <!-- 일부 글자만 스타일링 -->
    <!-- span : 아무 의미 없는 태그 -->
    <!-- 글자 굵기 : font-weight or stong -->
    <p>
        <span style="color: red; font-weight:600;">King</span> of the safari</p>

    <!-- 과제2 : 본인 프로필 페이지 제작 -->
    <img src="minjun.png" alt="프로필 이미지" style="display: block; margin-left: auto; margin-right: auto;">
    <h3 style="text-align: center; letter-spacing: 5px; font-size: 2.5vw;">MinJun</h3>

```

## 과제2 : 자기 프로필 만들기 

<img width="399" alt="스크린샷 2024-02-05 오후 9 32 00" src="https://github.com/choiminjun94/TIL2024/assets/60457431/6ab221d3-b8a9-4c64-8fa2-05bfa6ba2794">

```html
 <img src="minjun.png" alt="프로필 이미지" style="display: block; margin-left: auto; margin-right: auto;">
    <h3 style="text-align: center; letter-spacing: 5px; font-size: 2.5vw;">MinJun</h3>

    <p style="text-align: center; font-size: 200%;">
        <span style="color: red; font-weight: bolder;">
            Front-end
        </span>
         Developer
    </p>
```
## CSS 만들고 첨부

```txt 

CSS의 우선 순위 

html 안의 style> id > class > tag

```
## Tag 우선순위

```txt

.이름 : 클래스 선언
태그 : 해당 태그에 전부 적용
# : id 선언

```

## html에 css 선언

```html

<head>
    <!-- CSS 폴더 -->
    <link rel="stylesheet" href="../css/main.css" rel="stylesheet">
</head>

```

## CSS 파일 작성
```css
/* class 선언 */
/* class 특징  1. 점 찍고 작명, 2. 이름 중복 피하기*/
.profile{
    display: block; 
    margin-left: auto;
    margin-right: auto; 
}
.name{
    text-align: center; 
    letter-spacing: 5px; 
    font-size: 2.5vw;
}
.content{
    color: blueviolet;
}
/* 모든 p태그에 밑에 CSS 작용 */
p{
    text-align: center; 
    font-size: 200%;
    color: blue;
}

/* id선언 - 별로 안씀 */
#special{
    text-align: center; 
    font-size: 200%;
    color: chartreuse;
}

```

## div 박스 만들기 

```txt 

margin : 상하좌우 여백 
padding : 상하좌우 안쪽 여백
border : 테두리
border-radius : 테두리 둥글게

가운데 정렬 
display: block;
margin-left: auto;
margin-right: auto;

box-shadow : 그림자 효과 

```
그림자 참고 URL : https://codingbroker.tistory.com/65 


![스크린샷 2024-02-06 오후 3 28 25](https://github.com/choiminjun94/TIL2024/assets/60457431/e9ed14c5-b575-4509-a02d-fdcb7de1008c)


```html 

 <div class="box">박스 추가</div>

```

```css


.box{
    text-align: center;
    background-color: aqua;
    width: 200px;
    
    /* 상하좌우 여백 */
    margin :10px;
    /* 상하좌우 안쪽 여백 */
    padding: 40px;
 
    border-radius: 15px;

    /* 가운데 정렬 */
    display: block;
    margin-left: auto;
    margin-right: auto;
    font-size: 30px;

    /* 숙제3 - 박스에 그림자 효과 */
    box-shadow: 10px 10px 0 0 ;
}

```
## 레이아웃 float 만들기 1

> 이부분은 하기의 이미지를 만들기 위한 것

<img width="818" alt="스크린샷 2024-02-06 오후 5 29 12" src="https://github.com/choiminjun94/TIL2024/assets/60457431/ea67eec2-1881-4690-929a-fd8aee9771cc">

```html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="../css/layout.css">
    <title>레이아웃</title>
</head>
<body>
    <div class="container">
        <div class="header"></div>
        <div class="left-menu"></div>
        <div class="right-menu"></div>
        <div class="footer"></div>
    </div>    
</body>
</html>

```

### css 설명

```txt

요소를 왼쪽정렬 (공중에 띄어져 있는것) > float: left
float:left하는 이유 : div는 기본적으로 display:black이 되어있기에 한행을 전부 차지

float 해결방안(공중에 띄어져 있는것의 해결방안)
clear:both;

```

```css 

.container{
    width: 800px;
}

.header{
    /* 부모태그 width의 100% */
    width: 100%;
    height: 100px;
    background-color: aquamarine;
}
/* float:left하는 이유 : div는 기본적으로 display:black이 되어있기에 한행을 전부 차지 */
.left-menu{
    width: 20%;
    height: 400px;
    background-color: blue;
    /* 요소를 왼쪽정렬 (공중에 띄어져 있는것) */
    float: left;
}
.right-menu{
    width: 80%;
    height: 400px;
    background-color: cadetblue;
    /* 요소를 왼쪽정렬 (공중에 띄어져 있는것)*/
    float: left;
}
.footer{
    width: 100%;
    height: 100px;
    background-color: brown;
    /* float 해결방안 */
    clear:both;
}

```
## 레이아웃 inline-block 만들기 

> 공부한걸 정리를 하겠지만 안쓰는것이 좋다. 불편

``` txt
display: inline-block; - 내 크기만큼 차지하게 해주세요
inline-block 사용 시 공백을 삭제 해주어야 한다.

```

```html
 <div class="container">
        <div class="header"></div>
        <!-- css에서 display: inline-block;를 사용시 공백을 없애야 한다. -->
        <div class="left-menu"></div><div class="right-menu"></div>
        <div class="footer"></div>
    </div>  
```

```css

.container{
    width: 800px;
}

.header{
    /* 부모태그 width의 100% */
    width: 100%;
    height: 100px;
    background-color: aquamarine;
}
.left-menu{
    width: 20%;
    height: 400px;
    background-color: blue;
    /* display: inline-block; - 내 크기만큼 차지하게 해주세요 */
    display: inline-block;
}
.right-menu{
    width: 80%;
    height: 400px;
    background-color: cadetblue;
    display: inline-block;
}
.footer{
    width: 100%;
    height: 100px;
    background-color: brown;
}

```

## 레이아웃 과제 

> 하기와 같은 레이아웃을 만들어야 한다.

![스크린샷 2024-02-06 오후 7 35 55](https://github.com/choiminjun94/TIL2024/assets/60457431/546ad1d8-13c7-4e82-9e73-ac1b3da41e72)


```txt

 그러기 위해선 구획을 먼저 나누어 주고 시작

 1. 본문과 사진이 들어갈 자리를 background-color로 표시
 2. 본문에서 사진, 이름, 시간을 작성
 3. 본문 작성
 4. 이미지 추가 

순으로 하면 된다.  
이때 미세 margin 및 padding도 들어간다. 
```

> 하기의 사진은 본인이 만들것 (헤더는 그냥 넣어봄)

<img width="855" alt="스크린샷 2024-02-06 오후 7 41 09" src="https://github.com/choiminjun94/TIL2024/assets/60457431/a9a91dfc-e541-403d-a7b4-27b4273f5a48"> 

```html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="../css/layoutHomeWork.css">
    <title>레이아웃 과제</title>
</head>
<body>
    <div class="container">
        <div class="header">
            <p style="padding: 2px;">레이아웃 첫번째 과제</p>
        </div>
        <div class="content">
            <img src="./minjun.png" alt="" style="width: 10%; float: left;">
            <div class="blog-name">
                <h4 style="margin: 8px;">최민준</h4>
                <p style="margin: 8px;">1시간전</p>
            </div>
            <div class="blog-content">
                <h4 style="margin: 10px;">더러운 화장실 변기엔 역시 Bref!!!!</div>
                <p style="margin: 10px;"> 더러운 화장실 변기 청소떄문에 고생하시는 당신을 위한 아이템! 독일 변기 세정제 Bref!!!!</p>
            </div>
        </div>
        <div class="blog-img">
            <img src="./bref.png" alt="" class="size">
        </div>
    </div>
</body>
</html>

```

```css 

.container{
    width: 800px;
}
.header{
    width: 100%;
    height: 50px;
    text-align: center;
    border-style:solid;
}
.content{
    width: 70%;
    height: 300px;
    float: left;
    clear: both;
}
.blog-name{
    float: left;
}
.blog-content{
    clear: both;
}
.blog-img{
    width: 20%;
    height: 300px;
    float: left;
    background-color: pink;

}
.size{
    width: 100%;
}

```
## Nav 만들기 

```txt

1. nav라는 태그 생성
   nav도 div랑 같지만 nav라고 알기 위해서 사용

2. nav css 생성
navbar li는 모두 아래의 css를 적용
navbar>li는 직계 자손만 적용 


```

<img width="835" alt="스크린샷 2024-04-08 오후 2 40 35" src="https://github.com/choiminjun94/TIL2024/assets/60457431/a6ebf62f-32e7-4ae7-82ab-f1d256e8709f">


```html

 <!-- nav도 div랑 같지만 nav라고 알기 위해서 사용 -->
    <nav>
        <ul class="navbar">
            <li><a href="#">영화</a></li>
            <li><a href="#">맛집</a></li>
            <li><a href="#">IT</a></li>
            <li><a href="#">PC</a></li>
        </ul>
    </nav>


```

```css

/* navbar li는 모두 아래의 css를 적용 */
.navbar li{
    display: inline-block;
    width: 60px;
    text-align: center;
    background-color: #eee;
    padding: 15px;
    border-radius: 10px;
  
}
.navbar a{
    font-size: 16px;
    /* a태그 밑줄 제거 */
    text-decoration: none;
    /* 방문 후 표시색 변경*/
}
a:visited {
    color : green;
}
a:hover {
    color : red;
}

/* 만약에 space가 아닌 >를 사용시 직계 자식에만 적용 */
/* 직계자식 예시 */
/* 

.navbar>li{
    display: inline-block;
}

*/

```

## 배경 이쁘게 넣는 스킬들 & margin collapse

<img width="1364" alt="스크린샷 2024-04-08 오후 3 59 09" src="https://github.com/choiminjun94/TIL2024/assets/60457431/e4739f28-b8c2-4537-9ebe-9b5fabffa882">

```txt

    1. 이미지 경로 추가 
        background-image: url(이미지 경로 추가);

    2. 배경 이미지 사이즈 조절
        2.1  cover : 배경 짤려도 상관 없이 꽉채우기
            background-size: cover;
        2.2  contain : 배경이 안짤리게
            background-size: contain;
    3. 배경 이미지의 반복 여부와 반복 방향을 정합니다
         background-repeat: no-repeat

    4. 배경 이미지의 위치를 정하는 속성입니다
        background-position: center;
    
    5. 스크롤 여부를 정합니다
        background-attachment: fixed;

    6. 필터 조절 
        filter : 조건 입력 
        단 사진에 필터를 입력 시 사진 안에 글도 필터가 적용

    7. padding을 사용하는 이유 : margin collaps 때문이다.
       margin collaps이란 
       마진 겹침 현상 이다. 

       이때 padding 1을 주면 해결

```

Margin-collapsing 참고 url : https://velog.io/@raram2/CSS-마진-상쇄Margin-collapsing-원리-완벽-이해

> 과제 정리

```txt 

    1. 글자 가운데로 정렬 : text-align: center

    2. 버튼 가운데 정렬 
        버튼을 가운데 정렬 하기 위해선 아래와 같은 구조를 가져야 한다. 
        <div>
            <button></button>
        </div> 

        2.1 div의 css
            text-align: center;
        2.2 button의 css
            display :inline-block; 

    3. 버튼 테두리 없애기
        border: none;

```
##  position과 좌표

```txt

position 사용 시
1. 좌표 이동 가능
2. 공중에 뜸 (만약에 글씨가 있을 시 글씨에 영향을 주지 않는다.)

position: relative : 내 원래 위치를 기준으로 이동
position: static : 좌표이동 X
position: fixed : 현재화면이 기준
position: absolute : 내부모 태그 ( relative 가진 부모)

position: absolute 시용 시 가운데 정렬

    left: 0;
    right: 0;
    margin: auto;    
    width: 200px;

```

<img width="1366" alt="스크린샷 2024-04-08 오후 5 14 51" src="https://github.com/choiminjun94/TIL2024/assets/60457431/83c417f2-9353-4302-a3bd-54ed286755f6">


```html 

<body style="margin: 0px;">
    <div class="main-background">
        <h4 class="main-title">Welcome To Our Mall</h4>
        <!-- 숙제 세일즈 문구 적용 (버튼 추가)-->
        <p class="sale-contect">Let's go meet the best quality shoes in the world </p>
        <button class="button-css"> Click Here </button>
    </div>
</body>

```

```css

.main-background{
    width: 100%;
    height: 500px;
    /* 이미지 경로 추가 */
    background-image: url(./img/shoes.jpg);
    /* cover : 배경 짤려도 상관 없이 꽉채우기  */
    /* contain : 배경이 안짤리게 */
    background-size: cover;
    /* 배경 이미지의 반복 여부와 반복 방향을 정합니다 */
    background-repeat: no-repeat;
    /* 배경 이미지의 위치를 정하는 속성입니다 */
    background-position: center;
    /*  스크롤 여부를 정합니다 */
    /*  background-attachment: fixed; */
    /* 필터 적용 */
    /* filter: brightness(70%); */

    /*  margin collapse 때문에 적용 */
    padding: 1px;   
    position: relative;
}
.main-title{
    color: white;
    font-size: 50px;
    margin-top: 100px;
    /* text 가운데로 지정 */
    text-align: center;
    margin: 60px;
}
.sale-contect{
    color: aliceblue;
    font-size: 70px;
    font-weight: bold;
    text-align: center;
    margin: 10px;
}
.button-css{
    padding: 15px;    
    border-radius: 10px;
    font-size: 20px;
    color: white;
    font-weight: bold;
    background-color: yellowgreen;
    /* 테두리 선 없애기 */
    border: none;
    position: absolute;
    /* 아래 :  position: absolute 시용 시 가운데 정렬*/
    left: 0;
    right: 0;
    margin: auto;    
    width: 200px;
}



```
## 과제 박스 겹치게

```txt

처음에 과제가 실패 했는데 이유는 div 위치를 잘못 잡아서 이다. 

```

<img width="1364" alt="스크린샷 2024-04-08 오후 5 45 24" src="https://github.com/choiminjun94/TIL2024/assets/60457431/f1f6cfdd-bdea-4350-b992-5b6995f6f72c">


```html

<body style="margin: 0px;">
    <div class="main-background">
        <h4 class="main-title">Welcome To Our Mall</h4>
        <!-- 숙제 세일즈 문구 적용 (버튼 추가)-->
        <p class="sale-contect">Let's go meet the best quality shoes in the world </p>
        <button class="button-css"> Click Here </button>
    </div>
    <!-- 과제  -->
    <div class="homework">
        <h4>How we design our shoes</h1>
        <div>Lorem ipsum dolor sit amet, consectetur adipisicing elit.</div>
    </div>
</body>

```

```css

.homework{
    background-color: #eee;
    width: 700px;
    /* 가운데 정렬 */
    margin: auto;
    padding: 30px;
    text-align: center;
    position: relative;
    top: -50px;
} 

```
