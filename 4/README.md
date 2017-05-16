## 변수와 스코프, 메모리

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

//데이터 타입
/*
    에는 undefined , Null , Boolean , 숫자 , 문자열 등
    
    - typeof 연산자 사용
    
    var msg  = "some string";
    alert(typeof msg) // string
    alert(typeof(msg)) //string
    alert(typeof 100) // number

    #함수는 객체(object)로 간주
    
    
    -undefined 타입
    
    var 를써서 변수를 정의했지만 초기화 하지않았다면 undefined 가 반환됩니다.
    
    var msg;
    alert(msg == undefined); //true
    
    #변수에 undefined 를 지정하지않는다.
    
    alert(msg); // undefined
    alert(age); // ?
    

*/






```





