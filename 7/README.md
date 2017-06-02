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



    -join메서드를 통해서 배열의 구분자를 변경할 수도 있다

    var colors = ["red","blue","green"]; 
    alert(colors.join(',')); // red,green,blue 
    alert(colors.join('||')); // red||green||blue
    
    
    
    -스택 메서드 push
    var colors = new Array(); 
    var count = colors.push("red","green") //데이터 2개 추가 
    alert(count); // 2 var item = colors.pop(); 
    alert(item); // "green" 
    alert(colors.length) // 1
    
    
    -큐 메서드 shift  unshift
    var colors = new Array(); 
    var count = colors.push("red","green") //데이터 2개 추가 
    alert(count); // 2 
    var item = colors.shift(); 
    alert(item); // "red" 
    alert(colors.length) // 1


    
    -정렬 메서드 reverse() ,  sort()
    //reverse var values = [1,2,3,4,5];
    values.reverse(); 
    alert(values); // 5,4,3,2,1 //sort 
    var values2 = [3,2,4,1,5]; 
    values2.sort(); alert(values2); // 1,2,3,4,5




    -조작메서드  concat() ,  slice()
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
    
    매개변수에 음수를 넘기면 해당 배열의 계수를 더한 값과 같다
    colors.slice(-4 , -2)  같다   colors.slice(1 , 3)
    
    
    
    -splice() 메서드 중요 : 배열중간에 데이터를 삽입
    
    3가지로 사용 ( 삭제시 , 삽입시 , 대체시)
    
    //삭제 
    var colors = ["red", "green", "blue"]; 
    var removed = colors.splice(0, 1); //첫번쨰 데이터 제거 
    console.log(colors); // green,blue 
    console.log(removed);//red 
    
    //삽입 
    removed = colors.splice(1, 0, "yellow", "orange");//인덱스에 1에 데이터 2개 추가 
    console.log(colors); //green,yellow,orange,blue 
    console.log(removed);//빈배열 
    
    //대체 removed = colors.splice(1, 1, "red", "purple"); //데이터 2개 추가 1개 제거 
    console.log(colors); // green,red,purple,orange,blue 
    console.log(removed);// yellow
    
    
    -위치 메서드  indexOf()  , lastIndexOf()
    :매개변수는 두개를 사용하며, 첫 번째 매개변수는 검색 할 데이터, 두번째 매개변수는 검색을 시작할 인덱스 입니다.
    데이터를 찾지 못했다면 -1를 반환합니다.

    var numbers = [1,2,3,4,5,2,4,3,1];
    console.log(numbers.indexOf(4));    //3
    console.log(numbers.lastIndexOf(4)); //6
    console.log(numbers.indexOf(4, 4)); //6
    console.log(numbers.lastIndexOf(4, 4)); //3
    
    -반복 메서드  every  , some , filter , map
    
    var numbers = [1,2,3,4,5,2,23];
    var everyResult = numbers.every(function(item , index , array){

        return(item > 2)
    });
    console.log(everyResult) // false : 반환값이 모두 true 여야 true

    var someResult = numbers.some(function(item , index , array){

        return(item > 2)
    });	    
    console.log(someResult) // true  : 반환값중에 하나라도 true 이면 true 값

    var filterResult = numbers.filter(function(item , index , array){

        return(item > 2)
    });
    console.log(filterResult) // [3, 4, 5, 23]  // 조건에맞는 값만 반환한다

    var mapResult = numbers.map(function(item , index , array){

        //return(item > 2)
        return item * 2;
    });
    console.log(mapResult) // [2, 4, 6, 8, 10, 4, 46] // 결과값을 새 배열에 저장하여 반환한다


*/

//Date 타입 
/*    
    객체생성 
    
    var now = new Date();
    
    날짜표시 메서드
    toDateString() : 날짜를 요일, 월, 일, 년 형식으로 표시
    toTimeString() : 날짜를 시, 분, 초, 타임존 형식으로 표시
    toLocaleDateString() : 날짜를 요일, 월, 일, 년 형식으로 표시
    toLocaleTimeString() : 날짜를 시, 분, 초, 타임존, 형식으로, 표시
    toUTCString() : 날짜를 UTC(협정 세계시)형식으로 표시


    날짜/시간 부속 메서드

    getDate() : 로컬 시간을 사용하여 일(월 기준) 값을 반환합니다.
    getDay() : 로컬 시간을 사용하여 일(주 기준) 값을 반환합니다.
    getFullYear() : 로컬 시간을 사용하여 연도 값을 반환합니다.
    getHours() : 로컬 시간을 사용하여 시간 값을 반환합니다.
    getMilliseconds() : 로컬 시간을 사용하여 밀리초 값을 반환합니다.
    getMinutes() : 로컬 시간을 사용하여 분 값을 반환합니다.
    getMonth() : 로컬 시간을 사용하여 월 값을 반환합니다.
    getSeconds() : 로컬 시간을 사용하여 초 값을 반환합니다.
    getTime() : Date 개체의 시간 값을 1970년 1월 1일 자정 이후로 밀리초 단위로 반환합니다.
    getTimezoneOffset() : 호스트 컴퓨터와 UTC(지역 표준시) 사이의 시간 차를 분으로 반환합니다.
    getUTCDate() : UTC를 사용하여 일(월 기준) 값을 반환합니다.
    getUTCDay() : UTC를 사용하여 일(주 기준) 값을 반환합니다.
    getUTCFullYear() : UTC를 사용하여 연도 값을 반환합니다.
    getUTCHours() : UTC를 사용하여 시간 값을 반환합니다.
    getUTCMilliseconds() : UTC를 사용하여 밀리초 값을 반환합니다.
    getUTCMinutes() : UTC를 사용하여 분 값을 반환합니다.
    getUTCMonth() : UTC를 사용하여 월 값을 반환합니다.
    getUTCSeconds() : UTC를 사용하여 초 값을 반환합니다.
    getVarDate() : Date 개체의 VT_DATE 값을 반환합니다.
    getYear() : 연도 값을 반환합니다.
    hasOwnProperty() : 개체에 지정된 이름을 가진 속성이 있는지 여부를 나타내는 부울 값을 반환합니다.
    isPrototypeOf() : 개체가 다른 개체의 프로토타입 체인에 있는지 여부를 나타내는 부울 값을 반환합니다.
    propertyIsEnumerable() : 지정된 속성이 개체의 일부인지와 열거할 수 있는지 여부를 나타내는 부울 값을 반환합니다.
    setDate() : 로컬 시간을 사용하여 숫자로 된 날짜(월 기준)를 설정합니다.
    setFullYear() : 로컬 시간을 사용하여 연도 값을 설정합니다.
    setHours() : 로컬 시간을 사용하여 시간 값을 설정합니다.
    setMilliseconds() : 로컬 시간을 사용하여 밀리초 값을 설정합니다.
    setMinutes() : 로컬 시간을 사용하여 분 값을 설정합니다.
    setMonth() : 로컬 시간을 사용하여 월 값을 설정합니다.
    setSeconds() : 로컬 시간을 사용하여 초 값을 설정합니다.
    setTime() : Date 개체의 날짜와 시간 값을 설정합니다.
    setUTCDate() : UTC를 사용하여 숫자로 된 날짜(월 기준)를 설정합니다.
    setUTCFullYear() : UTC를 사용하여 연도 값을 설정합니다.
    setUTCHours() : UTC를 사용하여 시간 값을 설정합니다.
    setUTCMilliseconds() : UTC를 사용하여 밀리초 값을 설정합니다.
    setUTCMinutes() : UTC를 사용하여 분 값을 설정합니다.
    setUTCMonth() : UTC를 사용하여 월 값을 설정합니다.
    setUTCSeconds() : UTC를 사용하여 초 값을 설정합니다.
    setYear() : 로컬 시간을 사용하여 연도 값을 설정합니다.
    toDateString() : 날짜를 문자열 값으로 반환합니다.
    toGMTString() : GMT(그리니치 표준시)를 사용하여 문자열로 변환된 날짜를 반환합니다.
    toISOString() : 날짜를 ISO 형식의 문자열 값으로 반환합니다.
    toJSON() : JSON serialization 이전에 개체 형식의 날짜를 변환하는 데 사용됩니다.
    toLocaleDateString() : 호스트 환경의 현재 로캘에 해당하는 문자열 값으로 날짜를 반환합니다.
    toLocaleString() : 현재 로캘을 사용하여 문자열로 변환된 개체를 반환합니다.
    toLocaleTimeString() : 호스트 환경의 현재 로캘에 해당하는 문자열 값으로 시간을 반환합니다.
    toString() : 개체를 나타내는 문자열을 반환합니다.
    toTimeString() : 시간을 문자열 값으로 반환합니다.
    toUTCString() : UTC를 사용하여 문자열로 변환된 날짜를 반환합니다.
    valueOf() : 지정한 개체의 원시 값을 반환합니다.
*/
//RegExp 타입  ( Regular Expression )
/*
    정규표현식이란 ?
    정규표현식의 사전적인 의미로는 특정한 규칙을 가진 문자열의 집합을 표현하는데 사용하는 형식 언어입니다. 
    주로 Programming Language나 Text Editor 등 에서 문자열의 검색과 치환을 위한 용도로 쓰이고 있습니다. 
    입력한 문자열에서 특정한 조건을 표현할 경우 일반적인 조건문으로는 다소 복잡할 수도 있지만, 
    정규표현식을 이용하면 매우 간단하게 표현 할 수 있습니다. 
    하지만 코드가 간단한 만큼 가독성이 떨어져서 표현식을 숙지하지 않으면 이해하기 힘들다는 문제점이 있습니다.


    var expression = /pattern/flags;
    
    


*/






```


