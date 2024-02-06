# HTML & CSS
## 240205 
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

## 240206
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
