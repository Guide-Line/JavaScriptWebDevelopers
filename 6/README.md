## 함수 

#### 함수(function)란 하나의 로직을 재실행 할 수 있도록 하는 것으로 코드의 재사용성을 높여준다.



```javascript
	
    <함수의 형식>

    function 함수명( [인자...[,인자]] ){
       코드
       return 반환값
    };

    <함수의 정의와 호출>
    
    함수는 function 뒤에 함수의 이름이 오고, 소괄호가 따라온다. 소괄호에 인자라는 값이 차례로 들어오는데 이 값은 함수를 호출할 때 함수의 로직으로 전달될 변수다. 인자는 생략 할 수 있다. 함수를 호출 했을 때 실행하게 될 부분이 중괄호 안쪽에 온다.

    다음 예제를 보자. 이 함수의 이름은 numbering이고, 내용은 0부터 9까지를 화면에 출력한다.

  
    function numbering(){
        i = 0;
        while(i < 10){
            document.write(i);
            i += 1;
        }   
    }
    
    numbering();
    위의 예제 제일 하단에 아래 구문에 의해서 numbering이라는 이름의 함수가 호출되고 있는 것이다.

    numbering();// 0123456789
    
    
    <함수가 없다면> : 
    
    0부터 9까지 출력하는 애플리케이션을 만들었다. 그런데 0부터 9까지를 5번 출력해야 한다면 어떻게 해야할까? 
    
    var i = 0;
    while(i < 10){
        document.write(i);
        i += 1;
    }
    var i = 0;
    while(i < 10){
        document.write(i);
        i += 1;
    }
    var i = 0;
    while(i < 10){
        document.write(i);
        i += 1;
    }
    var i = 0;
    while(i < 10){
        document.write(i);
        i += 1;
    }
    var i = 0;
    while(i < 10){
        document.write(i);
        i += 1;
    }
    
    <입력과 출력>
    
    ;출력
    함수의 핵심은 입력과 출력이다. 입력된 값을 연산해서 출력하는 것이 함수의 기본적인 역할.
    
    function get_member1(){
        return 'egoing';
    }

    function get_member2(){
        return 'k8805';
    }

    alert(get_member1()); // egoing
    alert(get_member2()); // k8805
 
    function get_member(){
        return 'egoing';
        return 'k8805';
        return 'sorialgi';
    };
    k8805와 sorialgi는 출력하지 않았다. 왜 그럴까? 
    그것은 return 'egoing'을 실행한 후에 함수가 종료되었기 때문이다. return 'k8805' 이하는 어떠한 경우도 실행되지 않는다.

    
    
    ;입력
    인자(argument)는 함수로 유입되는 입력 값을 의미하는데, 
    어떤 값을 인자로 전달하느냐에 따라서 함수가 반환하는 값이나 메소드의 동작방법을 다르게 할 수 있다.
    
    
    function get_argument(arg){
        return arg;
    }

    alert(get_argument(1));
    alert(get_argument(2));
    
    ;복수 인자 
    function get_arguments(arg1, arg2){
        return arg1 + arg2
    }

    alert(get_arguments(10, 20));
    alert(get_arguments(20, 30));
    
    
    ;함수를 정의하는 다른방법    
    var numbering = function (){
        i = 0;
        while(i < 10){
            document.write(i);
            i += 1;
        }   
    }
    numbering();
   
    

```


