## HTML 속의 자바스크립트

#### 페이지 에서 자바스크립트를 불러오는 다양한 방법을 설명해보고 <script> 요소와의 관계에 대해서 설명한다  


```javascript
	
//인라인 자바스크립트 
<script type="text/javascript">
	function Hellow(){
		alert("hi")
	}
</script>


//외부에서 불러오기 형태
<script type="text/javascript" src="text.js"></script>


//script 테그 위치
/*
	script 테그 위치는 <head> 요소 안에 쓰는것이 일반적이였음. 
	웹 페이지는 body 테그를 만나면 랜더링을 시작하기때문에 <head> 테그 사이에 js 내용이 많으면 
	웹 페이지에 흰 화면만 보여지는 경우가 발생할수있다.
	하여 아래처럼 body 가장 하단에 스크립트를 위치 페이지 로딩이 체감속도가 빠르다고 느껴질수있다.
*/
<!DOCTYPE>
<html>
<head>
    <title>html page</title>
</head>

<body>
    
    <script>
        ...
    </script>
</body>

</html>

//script 처리 지연 페이지 전체가 파싱후에 스크립트가 실해되도 상관없을때 사용
//xhtml 문서에서는 defer="defer" 로 사용합니다.

<!DOCTYPE>
<html>
<head>
	<title>html page</title>
    <script type="text/javascript" defer src="text.js"></script>
</head>

<body>
   
</body>

</html>


```





