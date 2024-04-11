## JS Strat 

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
    <!-- Alert박스 UI  만들가-->
    <h1 id="hello">안녕하세요</h1>
    <h1  id="id">JS 초보에요</h1>  
    <!-- JS로 HTML 조작 -->
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