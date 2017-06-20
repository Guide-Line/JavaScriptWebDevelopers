## 변수 와 스코프( 유효범위 )

#### 자바스크립트에서 변수를 어떻게 다루는지 봅니다, 변수가 스코프를 벗어났을때 


```javascript

        var vscope = 'global';
        function fscope(){
            alert(vscope);
        };
        fscope();

        var vscope = 'global';
        function fscope(){
            var vscope = 'local';
            alert('함수안 '+vscope);
        };
        fscope();
        alert('함수밖 '+vscope);
    
    
        예1)
            var vscope ="global";
            function fscope(){
                var vscope ="local";
            };
            alert(vscope); ??

        예2)
            var vscope ="global";
            function fscope(){
                var vscope ="local";
                vscope ="local";
            };
            alert(vscope); ??
    
    
    <효용>
        function a (){
            var i = 0; // 지역변수
        };
        for(var i = 0; i < 5; i++){
            a();
            document.write(i);
        };
        //0, 1 ,2 , 3, 4

        function a (){
            i = 0; // 전역변수
        };
        for(i = 0; i < 5; i++){
            a();
            document.write(i);
        };
        //무한반복
    
    <전역변수>
        ;넓은 의미에서 충돌을 막기위한 변수 생성
    
        MYAPP = {}
        MYAPP.calculator = {
            'left' : null,
            'right' : null
        };
        MYAPP.coordinate = {
            'left' : null,
            'right' : null
        };

        MYAPP.calculator.left = 10;
        MYAPP.calculator.right = 20;
        function sum(){
            return MYAPP.calculator.left + MYAPP.calculator.right;
        };
        document.write(sum());

        ;위처럼 전역변수 조차 작성하기 싫을경우
        전역변수가 없는 지역변수로만 작성되어있음.
        %익명함수
        (function(){

            MYAPP = {}
            MYAPP.calculator = {
                'left' : null,
                'right' : null
            }
            MYAPP.coordinate = {
                'left' : null,
                'right' : null
            }

            MYAPP.calculator.left = 10;
            MYAPP.calculator.right = 20;
            function sum(){
                return MYAPP.calculator.left + MYAPP.calculator.right;
            }
            document.write(sum());

        }())
        
        
    <유효범위 대상> 은 함수
            
        for(var i = 0; i < 1; i++){
            var name = 'coding everybody';
        }
        alert(name);
        
    
        java
        for(int i = 0; i < 10; i++){
            String name = "egoing";
        }
        System.out.println(name);
        
        
        자바스크립트의 지역변수는 함수에서만 유효하다.
        
        
        
    <정적유요범위> : 함수가 선언된 시점에서 유효범위를 갖는다.
    
        var i = 5;

        function a(){
            var i = 10;
            b();
        }

        function b(){
            document.write(i);
        }

        a(); ? 
    

```


