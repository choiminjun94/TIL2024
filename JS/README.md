## 02)_JS Strat 

### getElementById

> JS로 HTML 조작하기 

``` txt

HTML의 id가 존재 시 JS를 사용하여 조작이 가능
조작시 에는  JS가 조작할 HTML의 ID를 사용하여 어떤것을 변경할 지만 입력 하면 된다. 

하기의 것을 보면서 설명 하면 

document.getElementById('hello').innerHTML='안뇽'
hello라는 id를 가진 html를 찾아서 innnerhtml를 사용 하여 안뇽이라고 입력 하는 것이다. 

금일 사용한 코드는 아래에 입력 함

```

``` html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <!-- JS로 HTML 조작 -->
    <h1 id="hello">안녕하세요</h1>
    <h1  id="id">JS 초보에요</h1>  
    <script>
   
        document.getElementById('hello').innerHTML='안뇽'
        document.getElementById('hello').style.color='red'

        document.getElementById('id').innerHTML = 'JS 고수에요'
        document.getElementById('id').style.color='pink'

        // 안녕하세요 폰트사이즈 16px로 바꾸기
       document.getElementById('hello').style.fontSize='16px';
    </script>
</body>
</html>

```
<img width="223" alt="스크린샷 2024-04-11 오후 9 31 54" src="https://github.com/choiminjun94/TIL2024/assets/60457431/dc7a3bc2-80e7-4bc6-8916-485b1bea3693">

### 동적 UI 만드는 스텝 (Alert box  만들기)

> Alert box 만들기

``` txt 

UI 만드는 Step 

1. HTML/CSS 미리 디자인 
2. 필요할 때 보여달라고 코드 작성

onclick는 안에 JS코드를 작성하면 버튼이 실행 된다. 
JS코드는 이전의 코드 처럼 document.getElementById를 사용하면 된다. 

버튼 클릭 시 알람창이라는  UI가 나오고 닫기를 클릭 시 다시 UI가 사라지는 코드를 작성

```

``` html 

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="../CSS/main.css">
</head>
<body>
    <!-- Alert박스 UI  만들가-->
    <div class="alert-box" id="alert">알림창 
        <button onclick="document.getElementById('alert').style.display='none'" class="close" id="close_alert">닫기</button>
    </div>
    <!-- onclick 안에 JS의 코드를 작성 -->
    <button onclick="document.getElementById('alert').style.display='block'">버튼</button>
    
    <script>
         
    </script>
</body>
</html>

```

```css 
.alert-box{
    background-color: aqua;
    padding: 20px;
    color: white;
    border-radius: 5px;

    /* 평소엔 디스플레이 감추기 */
    display: none;
}

.close{
    display: block;
}
```

