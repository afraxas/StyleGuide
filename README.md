#coding guideline

[toc]

##기본규칙
### 구조화
-	css를 사용하지 않는 환경에서도 읽을 수 있도록 구조화 하여 작성한다.

<label class="bad">//bad</label>

```html
<ul>
<span>회사소개</span>
<span>솔루션</span>
<span>Security</span>
<span>Availability</span>
<span>Compliance</span>
<span>Protext</span>
<span>사이버홍보실</span>
<span>복리후생</span>
<span>고객지원</span>
</ul>
```

<label class="good">//good</label>
```
<ul>
    <li>회사소개</li>
    <li>솔루션
        <ul>
            <li>Security</li>
            <li>Availability</li>
            <li>Compliance</li>
            <li>Protext</li>
        </ul>
    </li>
    <li>사이버홍보실</li>
    <li>복리후생</li>
    <li>고객지원</li>
</ul>
```


###소문자 사용
-	DTD를 제외한 모든 엘리먼트와 애트리뷰트는 소문자로 작성한다.
###빈줄

``` html
<head>
내용..
</head>
<!--빈줄 -->
<body>
내용..
</body>
```


###종료 테그 선언
-	모든 테그는 종료 테그를 선언해 준다.

````
<div id=footer>
    <address><img src="images/secums/footer.gif"></address>
</div>
````

###예외적인 종료 테그 선언
-	독립적으로 사용하는 테그에는 ‘ /’로 종료를 표시해 준다.
```
<area shape="rect" coords="0,0,82,126" alt="Sun" href="sun.htm" />
```

```<area> <base> <br> <col> <command> <embed> <hr> <img> <input> <keygen>
```<link> <meta> <param> <source>


### 주석
-	```<!– 주석내용 -->내용 <!– //주석내용 -->```
-	주석 기호는 ```<!-- -->```를 변경하지 않고 사용한다.
-	주석기호와 내용 사이에는 공백 한 칸 삽입한다.
-	주석 내용 사이에는 줄 바꿈을 허용하지 않는다.
-	시작과 종료 주석 내용은 동일해야 한다.
-	코드와 주석은 줄로 분리해서 사용한다.
````
<!-- 케이스 별 클래스 변화 -->
내용…
<!-- //케이스 별 클래스 변화 -->
<!-- 코드 숨김
내용…. -- >
````


## 구성요소 작성
### 기본규칙
-	class, style을 선언할 때는 제일 뒷 부분에 선언한다.
````
<input type=“text” id=“user_id” title=“사용자ID” class=“input_txt” style=”width:100px”>
````

###	```head<head>```
-	meta, title, link, script, style 순서로 선언한다
````
<head>
    <meta http-equiv=“Content-Type” content=“text/html;charset=utf-8”>
    <title>속보 :: 뉴스</title>
    <link rel=“stylesheet” type=“text/css” href=“css/default.css”>
    <script type=“text/javascript” src=“js/default.js”></script>
    <style type=”text/css”>
        /* 스타일 적용 */
    </style>
</head>
````

###	```link<link>```
-	rel, type, href 순서로 선언한다.
````
<link rel=“stylesheet” type=“text/css” href=“css/default.css”>
````



###	```script<script>```
-	type, src 순서로 선언한다.
````
<script type=“text/javascript” src=“js/default.js”></script>
````
-	페이지 별 부가 기능을 추가해야 하는 경우 각 페이지 하단에 따로 스크립트를 적용한다.


###	```img<img>```
-	src, width, height, title, alt, usemap 순서로 선언한다.
````
<img src=“logo.gif” width=“30” height=“10” title=“고객센터” alt=“고객센터” usemap=“#help”>
````

















