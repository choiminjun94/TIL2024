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

![test](https://github.com/choiminjun94/TIL2024/assets/60457431/d391eda1-cca5-44cb-a9e4-f5a3de19e2fc)


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

### function 문법 사용법 

> function 이란

```txt 

1. 긴코드를 짧은 단어로 축약하기  
2. 코드 재사용에 좋음

function 선언하기 

function function명 (){} 


```

> function 사용 예시 (이전 동적 UI 만들기에 function을 선언) 

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
        <button onclick="alertClose()" class="close" id="close_alert">닫기</button>
    </div>
    <!-- onclick 안에 JS의 코드를 작성 -->
    <!-- function 입력 -->
    <button onclick="alertOpen()">버튼</button>
    
    <script>

        function alertOpen(){
            document.getElementById('alert').style.display='block'
            console.log("알림창 커기");
        }

        function alertClose(){
            document.getElementById('alert').style.display='none'
            console.log("알람창 끄기");
        }
    </script>
</body>
</html>

```

### function 파리미터 문법


``` txt 
파라미터 사용

function function명( 파라미터 ){}
파라미터에  함수를 업데이트 할수 있다. 예를들면 현재 display = 자리에 block이라고 직접적으로 입력치 않고 파리미터를 입력 하는 것이다. 

또한 함수를 하나를 가지고 2종류의 코드를 실행 할수 있다.

```

> 파라미터 사용 예시를 밑에 정리 (함수 1개로 2종류의 코드 실행)

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
        <button onclick="alertOpen('none')" class="close" id="close_alert">닫기</button>
    </div>
    <!-- onclick 안에 JS의 코드를 작성 -->
    <!-- function 입력 -->
    <button onclick="alertOpen('block')">버튼</button>
    
    <script>
        
        function alertOpen(파리미터_테스트){
            document.getElementById('alert').style.display=파리미터_테스트
            console.log("알림창 커기");
        }
    </script>
</body>
</html>

```
> 버튼1 클릭 시 아이디 입력 이라는 창 나오기 
> 버튼2 클릭 시 비번 입력 이라는 창 나오기

![test2](https://github.com/choiminjun94/TIL2024/assets/60457431/1d87e037-7804-49cf-b0d0-9a85b2e99628)


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
    <div class="alert-box" id="alert">
        <p id="test">알림창</p> 
        <button onclick="alertClose()">닫기</button>
    </div>

    <!-- 버튼1 클릭 시 아이디 입력 하세요 -->
    <button onclick="아이디_입력()">버튼1</button>

    <!-- 버튼1 클릭 시 비번 입력 하세요 -->
    <button onclick="비번_입력()">버튼2</button>

    <script>
    
        function 아이디_입력(){
            document.getElementById('test').innerHTML ='아이디 입력'
            document.getElementById('alert').style.display='block'
        }

        function 비번_입력(){
            document.getElementById('test').innerHTML ='비번 입력'
            document.getElementById('alert').style.display='block'
        }
        
        function alertClose(){
            document.getElementById('alert').style.display='none';
        }

    </script>
</body>
</html>

```

> 위에 과제를 파리미터를 사용하여 개발
> 매우 좋은 예시 이다. 

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
    <div class="alert-box" id="alert">
        <p id="test">알림창</p> 
        <button onclick="alertClose()">닫기</button>
    </div>

    <!-- 파리미터 사용하여 개발  -->
    <!-- 버튼1 클릭 시 아이디 입력 하세요 -->
    <!-- 버튼2 클릭 시 비번 입력 하세요 -->

    <button onclick="파라미터_공부('제목입력','block')">버튼1</button>
    <button onclick="파라미터_공부('비번 입력', 'block')">버튼2</button>

    <script>
        function alertClose(){
            document.getElementById('alert').style.display='none';
        }
        function 파라미터_공부(파라미터_공부1, 파라미터_공부2){
            document.getElementById('test').innerHTML=파라미터_공부1
            document.getElementById('alert').style.display=파라미터_공부2
        }
    </script>
</body>
</html>

```
### JS 이벤트리스너 

> getElementsByClassName

```txt 

만약에 id가 없을시에는 class을 이용 할수 있는다 
그때에는 getElementsByClassName를 사용한다. 
주의 할 점은 클래스는 여러군데에서 사용할 수 있으닌 조심 해야한다. 그에 반해 id는 하나이다. 
동일명 class가 여러개일 시 특정 class를 사용하기 위해서는 인덱싱 이란것을 사용해야 한다. 

getElementsByClassName를 사용 시 인덱싱 사용하는 방법은 하기에 정리 하겠다. 
getElementsByClassName('title1')[0]

```
> 이벤트 리스너 

```txt 

이벤트가 발생 했을때 그 처리를 담당하는 함수이다. 

addEventListener(파라미터 2개가 필요) 
설명 : getElementById의 아이디를 클릭시 function (콜백 함수) 실행
콜백 함수는 코드를 순차적으로 실행 할때 가끔 보임

event란 행위를 이벤트라고 한다. 감시자의 역할을 수행 하는
 
addEventListener 이벤트 종류 
url : https://yoonjong-park.tistory.com/entry/addEventListener-이벤트리스너-종류

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
    <div class="alert-box" id="alert">
        <p class="title1" id="test">알림창</p> 

        <button id="close">닫기</button>
    </div>

    <button onclick="아이디_입력()">버튼1</button>

    <!-- 버튼1 클릭 시 비번 입력 하세요 -->
    <button onclick="비번_입력()">버튼2</button>


    <script>
        function alertClose(){
            document.getElementById('alert').style.display='none';
        }
        // 이벤트리스너 사용 
        // Line 351에서 실행 
        function 아이디_입력(){
            document.getElementById('close').addEventListener('click', function(){
                document.getElementById('alert').style.display= 'none';
            });

            function alertClose(구멍){
                document.getElementById('alert').style.display= 구멍;
            }
            document.getElementsByClassName('title1')[0].innerHTML ='아이디 입력'
            document.getElementById('alert').style.display='block'
        }

        function 비번_입력(){
            document.getElementById('test').innerHTML ='비번 입력'
            document.getElementById('alert').style.display='block'
        }
    </script>
</body>
</html>


```
### 서브메뉴 만들어보기와 classList 다루기

> 부트스트랩 설치 

```txt 

부트스트랩 url :  https://getbootstrap.kr/docs/5.1/getting-started/introduction/

버전 선택

스타터 템플릿 복붙 

```

```html 

<!doctype html>
<html lang="en">
  <head>
    <!-- Required meta tags -->
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">

    <!-- Bootstrap CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-1BmE4kWBq78iYhFldvKuhfTAU6auU8tT94WrHftjDbrCEXSU1oBoqyl2QvZ6jIW3" crossorigin="anonymous">
    <link rel="stylesheet" href="../CSS/main.css">
    <title>Hello, world!</title>
  </head>
  <body>
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-ka7Sk0Gln4gmtz2MlQnikT1wXgYsOg+OMhuP+IlRH9sENBO0LRn5q+8nbTov4+1p" crossorigin="anonymous"></script>
    
    
    <nav class="navbar navbar-light bg-light">
        <div class="container-fluid">
          <span class="navbar-brand">Navbar</span>
          <button class="navbar-toggler" type="button">
            <span class="navbar-toggler-icon"></span>
          </button>
        </div>
    </nav> 
    <!-- 클래스 탈부착  -->
    <!-- 이미 작성한 클래스에서 띄어쓰기를 한 이후 작성 -->

    <!-- 애니메이션 추가 쉬움 -->
    <!-- 나중에 재사용 편리 -->
    <ul class="list-group" id="test1" >
        <li class="list-group-item">An item</li>
        <li class="list-group-item">A second item</li>
        <li class="list-group-item">A third item</li>
        <li class="list-group-item">A fourth item</li>
        <li class="list-group-item">And a fifth one</li>
    </ul>
  </body>

  <script>

    // querySelector 안에 css 셀럭터를 넣어서 내가 원하는 요소를 추가 가능
    // 클래스를 표현 시 .을 찍기에 .을 추가
    // id를 표현 하고 싶을 때는 #을 추가 

    // 특징 중 가장 위에 것만 찾아줌
    // 다 찾아주기 위해선 querySelectorAll을 입력
    // 특정 것을 쓰기 위해선 인덱싱을 하면 된다. 
    document.querySelector('.list-group')
    // document.querySelector('.#test1')


    document.getElementsByClassName('navbar-toggler')[0].addEventListener('click', function(){
        // ul의 클래스 뒤에 show라는 클래스를 추가! 
        // 모르는 것 이기에 구글링 해서 찾아서 넣어야 함

        // toggle show가 존재 시 제거, 존재치 않을 시 추가
        document.getElementsByClassName('list-group')[0].classList.toggle('show');
    })
  </script>
</html>

```