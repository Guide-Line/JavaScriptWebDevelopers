## 변수 , 타입 , 연산자

#### 변수다루는 법 , 변수가 스코프를 벗어났을때 사용하던 메모리를 해제시키는 방


```javascript
	
//변수
/*
    var message; // message 변수가 선언되며 어떠한 값이라도 담을수있다.
    
    var message = "hi"; // hi값 저장   
    message = 100; // 유효하지만 권장 하지않는다.
    //문자 - > 숫자
    
    
    function test(){
        var msg ="hi"; //전역변수
    };
    test();
    alert(msg);//에러  : 내부함수 접근불가
    
    
    //쉼표를 이용하여 여러개의 변수선언가능
    var msg="hi" ,
        man="y",
        age=33;
    
*/

//변수 데이터 타입
/*
    에는 undefined , Null , Boolean , 숫자 , 문자열 등
    
    - typeof 연산자 사용
    
    var msg  = "some string";
    alert(typeof msg) // string
    alert(typeof(msg)) //string
    alert(typeof 100) // number

    #함수는 객체(object)로 간주
    
    
    - undefined 타입        
    
    var 를써서 변수를 정의했지만 초기화 하지않았다면 undefined 가 반환됩니다.
    
    var msg;
    alert(msg == undefined); //true
    
    #변수에 undefined 를 지정하지않는다.
    
    alert(msg); // undefined
    alert(age); // ?
    
    - null 타입
    
    var car = null;
    alert(typeof car); //object
    
    명시적으로 car 라는 변수를 아래 코드처럼 사용할수있다.
    
    if(car != null){
        //
    };
    
    undefined 는 null 에서 파생했으므로 표면적으로는 동일한 것으로 정의한다.
    
    alert(null == undefined); // ture
    alert(null === undefined); // ?
    
    위 값이 true 인것은 암시적으로 타입을 변경하였기때문이다.
    
    - 불리언 타입 ( 표참고 )
    
    해당 타입은 true , false 두개의 값만 가진다.
    
    var msg ="hi";
    var msgBoolean = Boolean(msg);
    alert(msgBoolean) // true
    
    if(msg){
      alert("value is true");   // ?
    };
    
    
    - 숫자 타입
    
    var intNum = 55; // 정수  가장많이 쓰는 형태
    var octalNum = 070; //8진법으로쓴 56
    
    부동소숫점숫자 ( 반드시 소숫점이있는 형태 )
    
    var num1 = 1.1;
    var num2 = 0.1;
    var num3 = .1; // 유효하지만 권장하지 않음
    
    
    #부동 소숫점은 정수에 비에 메모리를 2배 가량쓴다 하여 
     대단히 작거나 클경우에 "e-" 지수표기법을 쓰기도한다.
     
     var num4 = 3.125e7; // 31,250,000   3.125에 10에7자승 곱한값
     var num5 = 3e-7; 0.0000003;
    
    
    - NaN 
    
    숫자형 값 중에 NaN 값이있는데, 이 값은 숫자로 변환할 것으로 의도한 조작이 실해했을때 반환하는 값이다.
    
    NaN/10; // NaN   
    NaN/0;  // NaN
    alert(NaN == NaN); // false
    
    위에서 보여주는 고유 특성으로  ECMAScript 에서는 isNaN() 함수를 따로 제공한다 
    
    :숫자가 아닌가요
    alert(isNaN(NaN)); // true
    alert(isNaN(10)); // false 10은 숫자입니다.
    alert(isNaN("10")); // false 숫자 10으로 바꿀수있습니다.
    alert(isNaN("blue")); // true 숫자로바꿀수 없습니다.
    alert(isNaN(true)); // false 숫자 1로 바꿀 수있습니다.
    
    
    - 숫자 변환 
    : Number()  , parseInt()  , parseFloat()  3가지
    
     var num1 = Number("hi");     // NaN
     var num1 = Number("");       // 0
     var num1 = Number("00011");  // 11  
     var num1 = Number(true)      // 1;   
     
     ;정수로 값을 반환하며 가장 많이 사용
     var num1 = parseInt("1234blue");   // 1234
     var num1 = parseInt("");           // NaN
     var num1 = parseInt("0xA");        // 16진수 10
     var num1 = parseInt(22.5);         // 정수는 부동 소숫점이 없으므로 22
     var num1 = parseInt("70");         // 70
     var num1 = parseInt("0xf");        // 16진수 15
     
     
     var num1 = parseInt("313" ,10);    // 10진수로 명시할수 있다.
     
     #항상 진법 매개변수를 명시해서 에러를 예방하는게 좋다.
     
     
     var num1 = parseFloat("1234blue");   // 1234    
     var num1 = parseFloat("0xA");        // 0
     var num1 = parseFloat(22.5);         // 22.5
     var num1 = parseFloat("0908.5");     // 908.5
     var num1 = parseFloat("3.125e7");    // 31250000
     
     
     #연산자 과제 ( 아래 연산자 들을 쭉 한번 보세요 )
     
        -대입 연산자
        -비교 연산자
        -산술 연산자
        -비트단위 연산자
        -논리 연산자
        -문자열 연산자
        -조건 (삼항) 연산자
        -콤마 연산자
        -단항 연산자
        -관계 연산자
        
        
     참고 : https://developer.mozilla.org/ko/docs/Web/JavaScript/Guide/Expressions_and_Operators   
     
   
     

*/






```


###불리언 타입 표
|데잍터타입|true로변환되는값|false로변환되는값|
|:---|:---|:---|
|불리언|true|false|
|문자열|비어있지않은 문자열 모두|""(빈문자열)|
|숫자|0이 아닌 모든 숫자 포함|0 , NAN|
|객체|모든객체|null|
|Undefined|해당없음|undefined|











