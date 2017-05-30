## 참조 타입

#### Object 타입 과 Array 타입 에 대해서 알아봅니다.


```javascript
	
//Object 타입
/*
    Object 타입은 두가지 방식으로 사용 할수있다.
    
    //1. new로 생성 
    var person = new Object(); 
    person.name = "kendrick"; 
    person.age = 28; 
    
    //2. 객체 리터럴 표기법 생성 
    var person = { 
        name : "kendrick", 
        age : 28 
    }
    //ex) 
    두가지를 섞어서 
    var person = {}; // new Object와 동일 
    person["name"] = "kendrick"; //점표기법 대신 대괄호 표기법 사용

*/

//Array 타입
/*
    
    첫 슬롯은 문자열, 두 번째 슬롯은 숫자, 세 번째는 객체 등 
    뭐든지 담을수있다.

    /1. new를 이용한 생성 
    var colors1 = new Array(); //빈 배열을 생성 
    var colors2 = new Array(20); //길이가 20인 배열을 생성 
    var colors3 = new Array("red", "blue", "gray"); //괄호 안 3개의 데이터를 가진 배열을 생성 
    
    //2. 배열 리터럴 표기법 
    var colors1 = ["red", "blue", "gray"]; // 문자열이 세 개 있는 배열 생성 
    var colors2 = []; //빈 배열 생성

    var colors = ["red", "blue", "green"]; 
    alert(colors.length); // 3 출력 //length임의 변경 
    colors.length = 2; //크기가 2로 됩니다. 
    alert(colors[2]); //undefined


*/

//배열(Array) 감지
/*
    객체인지 배열인지 확인하는 방법
    
    
    var colorA = [];
    var colorO = {};
    if (colorO instanceof Array){ 
        alert("배열입니다.");
    }else{
        alert("아닙니다")
    };
    
    허나 instanceof는 다른 곳에서 전달받은 배열의 경우 다른 생성자 함수를 가지기 때문에 정확히 판별이 되지 않는 문제가 있습니다.
    그런 문제를 우회하기 위해서 Array.isArray() 메서드를 제공하고 있습니다.
    아래와 같이 사용할 수 있습니다.
   
    if (Array.isArray(colorO)){ 

        alert("배열입니다.");
    }else{
        alert("아닙니다")
    };

*/

//배열 변환 메서드
/*
    객체에는 모두 toLocaleString(), toString(), valueOf() 메서드가 존재합니다.

    var colors = ["red","blue","green"]; 
    alert(colors.toString()); // red,blue,green 
    alert(colors.valueOf()); // red,blue,green 
    alert(colors); // red,blue,green


    join메서드를 통해서 배열의 구분자를 변경할 수도 있다

    var colors = ["red","blue","green"]; 
    alert(colors.join(',')); // red,green,blue 
    alert(colors.join('||')); // red||green||blue
    
    
    스택 메서드 push
    var colors = new Array(); 
    var count = colors.push("red","green") //데이터 2개 추가 
    alert(count); // 2 var item = colors.pop(); 
    alert(item); // "green" 
    alert(colors.length) // 1
    
    
    큐 메서드 shift  unshift
    var colors = new Array(); 
    var count = colors.push("red","green") //데이터 2개 추가 
    alert(count); // 2 
    var item = colors.shift(); 
    alert(item); // "red" 
    alert(colors.length) // 1


    
    정렬 메서드 reverse() ,  sort()
    //reverse var values = [1,2,3,4,5];
    values.reverse(); 
    alert(values); // 5,4,3,2,1 //sort 
    var values2 = [3,2,4,1,5]; 
    values2.sort(); alert(values2); // 1,2,3,4,5


    조작메서드  concat() ,  slice()
    var values = [1, 2, 3, 4, 5, 6]; 
    var values2 = values.concat(7, [8, 9]); 
    console.log(values2); //[1,2,3,4,5,6,7,8,9]
    변수나 , 배열의 형태로 넘겨도 가능
    
    
    var colors = ["red", "green", "blue", "yellow", "purple"]; 
    var colors2 = colors.slice(1); 
    var colors3 = colors.slice(1, 4); 
    alert(colors2); // green,blue,yellow,purple 
    alert(colors3); // green,blue,yellow
    
    # str.slice(beginIndex[, endIndex])
    # 매개 변수가 하나이면 해당 번째 부터 끝까지 가져옴
    # beginIndex 번째부터 endIndex의 바로 앞까지 가져옴
    
    부정적인 인덱스
    console.log(colors.slice(-2)) // ["yellow", "purple"]
    console.log(colors.slice(-3 , -1)) // ["blue", "yellow"]
    console.log(colors.slice(-4 , -2)) // ["green", "blue"]

*/








```


