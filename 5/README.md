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
    
    
*/

//for-in 문
/*
    
    
*/







```


#### expression
    필수 사항 루프를 반복하기 전마다 점검하는 부울 식입니다. expression이 true이면 루프가 실행됩니다. expression이 false이면 루프가 종료됩니다.
#### statements
    선택 사항입니다. expression이 true인 경우 실행할 하나 이상의 문입니다.







