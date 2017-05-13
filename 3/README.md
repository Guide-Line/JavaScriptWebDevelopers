## 언어의 기초

#### 문법 내장연산자와 관련된 타입변환에 대해 소개


```javascript
	
//식별자
/*
    란 ? 변수나 함수 , 프로퍼티 , 함수 매개변수의 이름이고 , 한개이상의 문자로 표기
    ECMAScript 는 관습적으로 카멜케이스로 씁니다. 이는 첫번째 글자는 소문자로 쓰고 단어가 바뀔때 대문자로 쓰는 방법
    예 ) myCar , firstSecond , doSomethingImportant
*/

//문장
/*
    var sum = a + b  //세미콜론이 없어도 유효하지만 권장하지않음 
    var sum = a + b; //권장함    
    
    압축 => var sum = a + bvar sum = a + b;
    위 문장을 압축한다고 했을때 발생하는 에러는 중요한 문제라고 볼수있다.
    언제나 명확하게 세미콜론을 써서 문장을 종료하는것을 권장
*/

//if문 
/*
    if(test)
        alert(test);  // 유효하지만 에러의 원인이 되므로 ..
        
        
    if(test){
        alert(test);  // 권장함
    }
    
    코드블록 사용으로 의도를 좀더 명확하게 하고 수정시 에러발생도 줄일수 있겠다.
*/

//키워드 
/*    
    break case catch class const continue debugger default delete do  else export extends finally for
    function if  import in instanceof new return super switch this throw try typeof var void while with yield
    
*/

//예약어
/*
    ECMA-262 제3판
    bstract  boolean byte char class const debugger double  enum export extends final float goto implements import
    int interface long native package private protected public short static super synchronized throws transient volatile
*/





```





