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
    

*/



```


