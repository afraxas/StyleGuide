coding guideline
===========

[toc]

#HTML Guideline

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

### ```input<input>```
-	Type이 text인 경우(type – id – title – value – accesskey)
````
<input type=“text” id=“user_id” title =“사용자ID” value =“아이디를 입력하세요” accesskey =“1”>
````
-	Type이 radio, checkbox인 경우(type – name – id – checked)

````
<input type=“radio” name=“vt_align” id =“align_left” checked =“checked” >
<label for=“align_lft”>왼쪽정렬</label>
````
-	type이 file인 경우(type)
````
<input type=“file”>
````
-	Type이 image인 경우(type – src – alt)
````
<input type=“image” src=“img/btn_confirm.gif” alt=“확인”/>
````

-	Type이 button, reset, submit인 경우(type)
````
<input type=“button”>
````

### ```select<select>```
-	동일한 스타일의 박스의 너비값이 다르게 선택적으로 style이용하여 width값 제어
````
<select (id=“ ”) (src=“ ”) styel=“width:100px;”> </script>
````


### 특수문자 코드 변환

-	Entity로 변환하지 않은 특수문자는 오류코드로 판정된다.
-	W3C에서 HTML문서 작성시 특수문자는 반드시 엔티티 코드로 변환할 것을 권고 하고 있다.
-	ex> 꺽쇠(`<,>`),따움표(`“,”`)를 속성으로 인식 할 수 있다


| character | Entity | Name Description|
|-------|:---:|-----------:|
|“	|&quot;		|Quatation mark			|
|&	|&amp;		|Ampersand				 |
|<	|&lt;		|Less-than				 |
|>	|&gt;		|Greater-than			 |
|Ⓒ	|&copy;		|Copyright				 |
|®	|&reg;		|Registered trademark	 |
|™	|&trade;	|Trademark				 |
|×	|&times;	|Multiplication			 |
|÷	|&divide;	|Division				 |


- HTML 4
````html
<!DOCTYPE html>
<head>
    <meta charset="utf-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <title></title>
    <meta name="description" content="">
</head>
<body>
</body>
</html>
````
-JSP
````JSP

<!DOCTYPE html>
<head>
    <meta charset="utf-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <title></title>
    <meta name="description" content="">
</head>
<body>
</body>
</html>
````

#	CSS Guideline

##	기본규칙
### 들여쓰기
-	CSS코드를 작성할 때는 들여쓰기는 하지 않는다
````css
#content{border:1px solid #000}
#content.class{color:#000}
````

###	공백
-	쉼표가 구분되는 선택자의 공백은 제거 한다.
-	속성 간 공백 및 속성 값 사이에 공백으로 구분한다.
-	괄호 좌, 우 여백 공백을 제거 한다.

````css
a:hover,a:active,a:focus{text-decoration:underline}
.class p{color:000; line-height:18px}
.class p{color:#000;}
````

### 빈줄
-	의미 있는 객체를 구분하기 위하여 코드 그룹 간 1줄씩 빈 줄을 넣어 구분해 준다
````css
.class1{border:1px solid #000}
.class2 img{border:1px solid #000}
.class2{border:1px solid #000}
.class2 img{border:1px solid #000}}
````

### 줄바꿈
-	선택자, 속성, 속성 값 사이의 줄 바꿈을 하지 않는다
````css
.class1,.class2,.class3{width:100px; color:#000}
````

##	속성선언규칙
###	속성 선언 순서
-	레이아웃과 관련하여 높은 것부터 시작한다.
````css
.sheet01{display:none; overflow:hidden; position:absolute; left:10px; top:15px;
border:solid 1px #000; font-weight:bold;}
.sheet02{position:absolute; left:10px; height:10px; margin:0;
border:solid 1px #000; font-weight:bold}
````

-	레이아웃 -> 보더/배경-> 폰트 -> 기타
-	약식속성 사용 권장 – border, background

````css
.border_style{border:1px solid dotted #000}
````
-	•‘font’ 약식속성은 사용하지 않는다.
````css
.font{font-weight:bold; font-size:12px; font-family:dotum}
````


| category | prefix |
|-------|:---|:
|display		|	화면에 표시되는 속성을 제어
|overflow		|일정한 공간에서 글들이 넘칠때 쓰는 속성
|float			|전체의 흐름에따라 속성들을 정의한다.
|postion		|	위치를 지정해 주는 속성
|z-index		|	속성의 순서 지정해 준다.
|width&height	|크기에 대한 다양한 속성을 지원
|margin&padding	|간격을 지정해 주는 속성
|border			|라인의 크기,스타일을 지정해 주는 속성
|background		|배경에 다양한 속성을 선언
|font			|폰트에 대한 모든 스타일을 지정
|letter-spacing	|글자 사이의 간격을 지정한다.
|etc			|	기타 속성들

````css
    .exmp {
        display: none;
        overflow: . . .;
        float: . . .;
        ....
        letter-spacing : . .;
    }
````

##	주석(작성자표기)

###	적용방법
-	```</* 주석 */>```

```css
/* common */
Body,p,h1,h2,h3,ol,li,dl,dt,dd,table,th,td,form,{margin:0; padding:0;}
/* layout */
#wrap{…}
#header{…}
/* 테이블 스타일 */
.table_tit01{border-top:1px solid #fff}
/* 마이페이지 :: 20130412이수진수정 */
.my_page{width:300px}
````
-	주석은 “/* */”을 변경하지 않고 사용한다.
-	속성의 성격별로 첫 줄에 주석으로 설명
-	주석기호와 주석 내용 사이에 공백 한 칸이 있어야 한다.
-	주석 내용은 한 줄로 간략하게 표현한다.
-	css를 수정할 경우 수정한 사람의 이름,날짜를 표기 한다.

##	브라우저 호환성/핵(Hack) 사용

###	브라우저 호환성이란?
-	동일한 컨텐츠를 브라우저에서 가급적 동일한 화면을 보여주는 것이다

###	핵(Hack)
-	브라우저의 구현 차이나 버그를 이용하여 특정 브라우저만을 대상으로 적용하는 방법
>	상황에 따라서 최소한으로 사용한다.

##	공통표준파일

````css
@charset "utf-8";
/* common */
body,p,h1,h2,h3,h4,h5,h6,ol,li,dl,dt,dd,table,th,td,form,fieldset,legend,input,textarea,button,select{margin:0;padding:0}
body,input,texttarea,select,button,table{font-family:'돋움', Dotum, AppleGothic, sans-serif;font-size:12px}
img,fieldset{border:0}
ul,ol{list-style:none}
em,address{font-style:normal}
a{text-decoration:none}
a:hover,a:active,a:focus{text-decoration:underline}
````
-	CSS를 새로 작성할 때 기본으로 한다.
-	초기화 문장은 변경이 불가하다.


#	Naming Guideline

##	이미지 네이밍
###	이미지(img)이름 지정 하기
-	의미_성격(액션)_숫자
``btn_write_on_01.gif``
-	이미지 명은 소문자로만 사용한다.
-	3단계로 구성한다.
-	구성은 생략 될 수 있으나 위치는 변경하지 않는다.
-	공백 대신 언더스코어(_)를 사용한다.
-	순서가 필요한 이미지 경우

##	Id/class naming
##	예약어

| category | prefix |Detail|
|-------|:---|:---|:
|Background		|bg			|배경 이미지
|Button			|btn		|	버튼 이미지
|TopMenu			|menu		|상단 메뉴 이미지
|LeftMenu		|leftmenu	|왼쪽 메뉴 이미지
|Tab				|tab		|	탭 이미지
|Bullet			|bullet		|의미를 갖지 않고 텍스트와
|Banner			|banner		|배너 이미지
|Line			|line		|라인 이미지
|Icon			|icon		|의미를 갖고 있는 이미지
|Title			|tit		|	타이틀 이미지
|Sample			|sample		|예시, 테스트 용 이미지
|Copyright		|copyright	|카피라이터 이미지


###	Id
-	*#*예약어
````css
#wrap{margin:0}
````
-	지정된 예약어 사용 권장 한다.
-	Id는 스타일로 지정하지 않는다..
-	예약어가 없으면, 의미를 갖도록 규정한다.
-	레이아웃 id의 네이밍은 조합하여 사용할 수 없다.
-	팝업 문서의 레이아웃 예약어 앞에 ‘pop_’를 같이 사용한다

###	레이아웃 예약어

| Id | Detail| 
|-------|:---|:
|#wrap		|전체 감싸는 영역				 |
|#header		|상단 부분					|
|#content	|	컨텐츠 영역				   |
|#left		|왼쪽 영역(베너, 메뉴 부분)	  |
|#right		|오른쪽 영역(베너, 메뉴		   |
|#footer		|하단 카피라이터 부분	   |

````html
<div id=“#wrap”>
    <div id=“header”></div>
    <div id=“content”></div>
    <div id=“footer”></div>
</div>
````









