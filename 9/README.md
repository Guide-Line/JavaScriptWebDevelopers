## 값으로서 함수와 콜백

#### 자바스크립트 함수를 값처럼 사용하는 예를 보자


```javascript
    
    
    1) 
        -아래와같이 object  안에서 아래와같이 사용될수도있다.
        
        function a(){}


        a = {
            b:function(){   <--메소드
            }
        };

        인자로도 전달이 가능하다.

        function cal(func, num){
            return func(num)
        };

        function increase(num){
            return num+1
        };

        function decrease(num){
            return num-1
        };

        alert(cal(increase, 1));
        alert(cal(decrease, 1));
    
    
    2) 
        -함수의 리턴값으로도 사용이 가능하다.
    
        function cal(mode){
            var funcs = {
                'plus' : function(left, right){return left + right},
                'minus' : function(left, right){return left - right}
            }
            return funcs[mode];
        };
        alert(cal('plus')(2,1));
        alert(cal('minus')(2,1));  
        
        -배열값으로도 사용이가능하다.
        
        var process = [
            function(input){ return input + 10;},  
            function(input){ return input * input;}, 
            function(input){ return input / 2;}  
        ];
        var input = 1;
        for(var i = 0; i < process.length; i++){
            input = process[i](input);
        }
        alert(input);  60.5
        
        
    3)  
    
        -콜백
        
        function sortNumber(a,b){
            // 위의 예제와 비교해서 a와 b의 순서를 바꾸면 정렬순서가 반대가 된다.            
            
            if( a> b ){
                return 1;
            }else if(){
                return -1;
            }else{
                return 0;
            }
            
            //return a-b;
        }
        var numbers = [20, 10, 9,8,7,6,5,4,3,2,1];
        alert(numbers.sort(sortNumber)); // array, [20,10,9,8,7,6,5,4,3,2,1]
        
        하여 sortNumber 는 콜백 함수 즉 값으로 서 사용할수 있다.
        
        
        
    4)
        
        - 비동기 처리 : 설명
            (순서대로 처리 동기적 처리)
        datasource.json.js
        {"title":"study","author":"jdk"}


        $.get('./datasource.json.js', function(result){
            console.log(result);
        }, 'json');
        
        
        %코드 중간에 alert 가있다고 생각해 볼수도 있다.
        

```


