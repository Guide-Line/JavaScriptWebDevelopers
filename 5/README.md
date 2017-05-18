## 조건문 , 함수

#### 변수다루는 법 , 변수가 스코프를 벗어났을때 사용하던 메모리를 해제시키는 방


```javascript
	
//if 문
/*
    if(expression){
        statement1
    }else{
        statement2
    };
    
    위 조건에는 어떠한 표현식도 가능
    
    
    if(i > 25){
        alert("25보다 크다");
    }else{
        alert("25보다 작다");
    };
    
    ;유효하지만 아래처럼 코드블록을 사용하자
    if(조건) 값 else if (조건2) 값 else 값
    
    if(i>25){
        alert("25보다 크다");
    }else if(i<10){
        alert("i 가 10보다작을때);
    }else{
        alert("0 부터 24까지);
    };

*/

//do-while 문
/*
    do{
        statements
    }while(expression)
    
    
    var i = 0;
    do {
        console.log(i + " ");
        i++;
    } while (i < 10);

    // Output: 0 1 2 3 4 5 6 7 8 9
    
    
*/

//while 문
/*
    지정된 조건이 false 일때 까지 일련의 문을 실행한다.
    
    while (expression) {
        statements 
    } 
    
    var i = 0;
    var j = 10;
    while (i < 100) {
        if (i == j)
            break;
        i++;
    }
    console.log(i);  // 10
    
*/

//for 문
/*
  for(var i=0; i<10; i++){
    statment
  };
  
  ;for 루프는 보통 루프를 지정한 수만큼 실행할 경우에 사용합니다. for 루프를 사용하면 손쉽게 배열을 반복하고 순차적으로 처리할 수 있습니다.
  ;루프를 실행하기 전에 조건식을 테스트하므로 for 문은 0번 이상 실행됩니다.
  ;for 루프 문 블록의 임의 줄에서 break 문을 사용하여 루프를 종료하거나, continue 문을 사용하여 제어를 루프의 다음 반복으로 이동할 수 있습니다. ( 밑에서 다시 다루자 )
  
  var count = 10;
  for(var i=0; i<count; i++){
    console.log(i);    // 0 1 2 3 4 .... 9
  };
  alert(i); // 10
  
  
  ;;무한루프
  for(;;){
    doSomething;
  }
  
  보는 바와같이 while문과 동일한 기능을 한다.
    
*/

//for-in 문
/*
    // Initialize the array.
    var arr = ["지환","동국","왕섭"];

    var s = "";
    for (var obj in arr) {
     
       s += obj + ": " + arr[obj]
    }
     console.log(s)
  

    // Output:
    //   0: 지환
    //   1: 동국
    //   2: 왕섭   
    
    
    주의. for in 문이 가르키는 변수가 null 이나 undefined 라면 에러를 내고 해당 본문을 실행하지 않게 됨.
    
*/

//break 문 과 continue문
/*

    루프 내부 코드 실행을 조절하는 구문이다.

    ;5번째 루프중 break 문을 만나 해당 루프를빠져나가 는 모습니다.
    var num = 0;
    for(var i=1; i<10; i++){
        if(i%5 == 0){
            break;        
        };
        console.log(i) //  1 2 3 4 ... 9
        num ++;
    };
    console.log(num) // 4
    
    ;continue 때문에 한번은 증가시키지 않아 값이 8이되었다.
    var num = 0;
    for(var i=1; i<10; i++){
        if(i%5 == 0){
            continue;        
        };
        //console.log(i) //  1 2 3 4 ... 9
        num ++;
    };
    console.log(num) // 8
    
    주의 . 루프문은  최적화 해줘야하는 반복문인데 전체적인 성능에 영향을 끼친다. 루프성능에 악영향을 끼치는 continue문은 권장할수 없고
    
    또한 개발자의 의도 파악도 불분명,  디버그및 유지보수시에도 문제가 생길수 있다.
    
    유명개발자는 리팩토링을 통해 continue 제거후 테스트시 성능향상이 되지않은적이 없다고 말했다. 
    
*/

//switch 문
/*
    switch (i) {
        case 25 :
            alert("25");
            break;
        case 26 :
            alert("26");
            break;
        case 27 :
            alert("27");
            break;
        case 28 :
            alert("28");
            break;
        default :
            alert("other")
    };
    
    default 절을 사용하면 expression과 일치하는 레이블 값이 없을 경우 실행할 문을 제공할 수 있습니다
    
    
    label 값이 expression과 같으면 해당 statementlist를 실행합니다.
    
    break 문을 만나거나 switch 문이 끝날 때까지 실행을 계속합니다.따라서 break 문을 사용하지 않으면 여러 label 블록이 실행됩니다.
    
    expression과 일치하는 label이 없으면 default 사례로 이동합니다. default 사례도 없으면 마지막 단계로 이동합니다.
*/


//함수
/*
    기본
    function sayHi(){
        alert('sayHi');
    }
    sayHi() // sayHi 호출
    
    함수는 기본적으로 arguments 라는 객체를 가지고 있다.
    
    arguments는 기본적으로 배열의 형태를 띄고있고 접근은 arguments[0]  arguments[1] 이런형태를 띈다.
    
    함수의 매개변수는 숫자 , 문자 , 객체 어떤것이 들어와도 상관없다.
    
    function howManyArgs(){
        alert(arguments.length);
    };
    howManyArgs("하나" , "둘" , "셋");
    howManyArgs(1,2)
    howManyArgs(null , undefined ,null , undefined )
    
    과제)
    .빈함수를 하나 만들고
    .매개변수를 1개 넘겼을 경우에 10을 더하고
    .매개변수를 2개 넘겼을 경우에는 두개의 매개변수를 더하세요
    
    
*/


```


#### expression
    필수 사항 루프를 반복하기 전마다 점검하는 부울 식입니다. expression이 true이면 루프가 실행됩니다. expression이 false이면 루프가 종료됩니다.
#### statements
    선택 사항입니다. expression이 true인 경우 실행할 하나 이상의 문입니다.







