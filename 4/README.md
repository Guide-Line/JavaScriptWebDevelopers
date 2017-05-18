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
   
     

*/





```


### 불리언 타입 표

|데잍터타입|true로변환되는값|false로변환되는값|
|:---|:---|:---|
|불리언|true|false|
|문자열|비어있지않은 문자열 모두|""(빈문자열)|
|숫자|0이 아닌 모든 숫자 포함|0 , NAN|
|객체|모든객체|null|
|Undefined|해당없음|undefined|



### 대입연산자

|이름|복합대입연산자|뜻|
|:---|:---|:---|
|대입 연산|	x = y|	x = y
|덧셈 대입|	x += y|	x = x + y
|뺄셈 대입|	x -= y	|x = x - y
|곱셈 대입|	x *= y	|x = x * y
|나눗셈 대입|	x /= y	|x = x / y
|나머지 연산 대입|	x %= y	|x = x % y
|왼쪽 이동 연산 대입|	x <<= y	|x = x << y
|오른쪽 이동 연산 대입|x >>= y	|x = x >> y
|부호 없는 오른쪽 이동 연산 대입|	x >>>= y	|x = x >>> y
|비트 단위 논리곱 연산 대입|	x &= y	|x = x & y
|비트 단위 배타적 논리합 연산 대입|	x ^= y	|x = x ^ y

### 비교연산자

|연산자|설명|참을 반환하는 예제|
|:---|:---|:---|
|같은 (==)	|피연산자들이 같으면 참을 반환합니다.	|3 == var3 ,  "3" == var3 ,   3 == '3' |
|다른 (!=)	|피연산자들이 다르면 참을 반환합니다.	|var1 != 4 ,   var2 != "3"|
|엄격한 같은 (===)	|피연산자들이 같고 피연산자들의 같은 형태인 경우 참을 반환합니다. Object.is 와 자바스크립트에서의 같음 을 참고하세요.	|3 === var3|
|엄격한 다른 (!==)	|피연산자들이 다르거나 형태가 다른 경우 참을 반환합니다.	|var3 !== "3" , 3 !== '3' |
|~보다 큰 (>)	|좌변의 피연산자 보다 우변의 피연산자가 크면 참을 반환합니다.	|var2 > var1 , "12" > 2 |
|~보다 크거나 같음 (>=)	|좌변의 피연산자 보다 우변의 피연산자가 크거나 같으면 참을 반환합니다.	|var2 >= var1 ,  var3 >= 1 |
|~보다 작음 (<)	|좌변의 피연산자 보다 우변의 피연산자가 작으면 참을 반환합니다.	|var1 < var2 , "2" < 12 |
|~보다 작거나 같음 (<=)	|좌변의 피연산자 보다 우변의 피연산자가 작거나 같으면 참을 반환합니다.	|var1 <= var2 , var2 <= 5|

### 산술 연산자

|연산자|설명|예제|
|:---|:---|:---|
|나머지 연산자 (%)	|이항 연산자입니다. 두 피연산자를 나눈후 나머지를 반환합니다.	|12 % 5 returns 2.|
|증가 연산자 (++)	|단항 연산자입니다. 피연산자에 1을 더합니다. 만약 연산자를 피연산자 앞(++x)에 사용하면, 피연산자에 1을 더한 값을 반환합니다.; 만약 연산자를 피연산자 뒤(x++)에 사용하면, 피연산자에 1을 더하기 전 값을 반환합니다.	|If x is 3, then ++x sets x to 4 and returns 4, whereas x++ returns 3 and, only then, sets x to 4.|
|감소 연산자 (--)	|단항 연산자입니다. 피연산자로 부터 1을 뺍니다. 반환값은 증가 연산자와 유사합니다.	|If x is 3, then --x sets x to 2 and returns 2, whereas x-- returns 3 and, only then, sets x to 2.|
|단항 부정 연산자 (-)	|단항 연산자 입니다. 피연산자의 반대값(부호 바뀐값)을 반환합니다.	|If x is 3, then -x returns -3.|
|숫자화 연산자 (+)	|단항연산자 입니다. 피연산자가 숫자값이 아니라면 피연산자를 숫자로 변환하기를 시도합니다.	|+"3" returns 3.  , +true returns 1. |

### 논리 연산자

```javascript

논리 곱 (&&)    :  expr1 && expr2   두개의 연산자가 true 일때만 true 를 반환합니다.
논리 합 (||)    :  expr1 && expr2   두개의 연산자중 하나라도 true 이면 true 를 반환합니다.
논리 부정 (!)    :  !expr1  피연산자가 true 로 변환될수 있으면 false을 반환 합니다.
/*
    var a1 =  true && true;     // t && t returns true
    var a2 =  true && false;    // t && f returns false
    var a3 = false && true;     // f && t returns false
    var a4 = false && (3 == 4); // f && f returns false
    var a5 = "Cat" && "Dog";    // t && t returns Dog
    var a6 = false && "Cat";    // f && t returns false
    var a7 = "Cat" && false;    // t && f returns false
    
    
    var o1 =  true || true;     // t || t returns true
    var o2 = false || true;     // f || t returns true
    var o3 =  true || false;    // t || f returns true
    var o4 = false || (3 == 4); // f || f returns false
    var o5 = "Cat" || "Dog";    // t || t returns Cat
    var o6 = false || "Cat";    // f || t returns Cat
    var o7 = "Cat" || false;    // t || f returns Cat
    
    
    
    var n1 = !true;  // !t returns false
    var n2 = !false; // !f returns true
    var n3 = !"Cat"; // !t returns false

*/

```

### 조건 연산자

조건 ? 값1 : 값2

var status = (age >= 18) ? "adult" : "minor";

;;이 구문은 age 변수가 18보다 같거나 클때 "adult" 값을 status 변수에 대입합니다. 그렇지 않은 경우, 이 구문은 "minor"값을 status변수에 대입합니다.




































