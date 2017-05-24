## 변수(원시,참조)와 스코프 , 메모리

#### 자바스크립트에서 변수를 어떻게 다루는지 봅니다, 변수가 스코프를 벗어났을때 사용하던 메모리를 해제하는 가비지 컬렉션이 자바스크립트에서 어떻게 사용되는지 봅니다.


```javascript
	
//원시값과 참조값
/*
    원시값 : undefined, Null , Boolean , 숫자 , 문자열    
    참조값 : 메모리에 저장된 객체
    
    
    
    var person = new Object();
    person.name = "john";
    alert(person.name)' // john
    
    
    var name = "john";
    name.age = 27;
    alert(name.age); // undefined  
    
    동적으로 프로퍼티즈에 추가할수 있는값은 참조값 뿐이다.
    
    
    var num1 = 5;
    var num2 = num1;
    alert(num1)
    
    
    객체에도 아래처럼 복사가 가능 ...
    
    var obj1 = new Object();
    var obj2 = obj1;
    obj1.name ="john";
    alert(obj2.name); // john

*/

//함수에 매개변수 전달 : 변수 , 매개변수, 함수 
/*
    var count= 20;
    var result =  addTen(count);
    alert(count);
    alert(result);
    function  addTen(num){ // num 은  addTen 의 매개 변수,
        num += 10; // num 은 지역변수
        return num;
    };
    
*/


//실행 컨텍스트와 스코프
/*
    실행 컨텍스트(execution context:EC)는 짧게 ‘컨텍스트’라고 부른다.
    변수나 함수의 실행 컨텍스트는 다른 데이터에 접근할 수 있는지, 어떻게 행동하는지를 규정한다. 
    각 실행 컨텍스트에는 변수 객체(variable object:VO)가 연결되어 있으며 해당 컨텍스트에서 정의된 모든 변수와 함수는 이 객체에 존재한다. 
    이 객체를 코드에서 접근할 수는 없지만 이면에서 데이터를 다룰 때 이 객체를 이용한다.
    
    
    var color ="blue";
    
    function changeColor(){
        var anotherColor = "red";
        
        function swapColors(){
            var tempColor = anotherColor;
            anotherColor = color;
            color = tempColor;
            
            //color , anotherColor , tempColor 접근가능
        };
         
        //color , anotherColor 접근가능 tempColor 불가능
        swapColors(); 
    }
    // color 만 접근가능
    changeColor();
    
    
    
    
    function a(){
     var a = 1;        (A)
     function b(){
      console.log(a);  (B)
     }
     b();
    }
    a();
    
    위 실행 결과는 ???
*/




```


