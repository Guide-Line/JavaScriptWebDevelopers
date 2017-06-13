## 객체 

#### 배열은 아이템의 식별자로 숫자로 활용하였다. 숫자가 아닌 문자로 하고싶다면 객체를 사용해야한다.



```javascript
	
    1) 객체의 생성
    
        var grades = {'egoing': 10, 'k8805': 6, 'sorialgi': 80};
        
        ( or ) 
        
        var grades = {};
        grades['egoing'] = 10;
        grades['k8805'] = 6;
        grades['sorialgi'] = 80;
        
        ( or )
        
        var grades = new Object();
        grades['egoing'] = 10;
        grades['k8805'] = 6;
        grades['sorialgi'] = 80;
        
        
    
    2) 데이터를 꺼내는 방법
   
        var grades = {'egoing': 10, 'k8805': 6, 'sorialgi': 80};
        
        alert(grades['sorialgi']);
        
        ( or )
        
        alert(grades.sorialgi);
        
        
    3) 객체의 반복작업
        
        기존배열과 비교 설명 
        var grades = [10, 6, 80];  // 0 , 1 , 2
        
        
        
        배열과 다르게 순서가 없고 key 값이 있다.
        var grades = {'egoing': 10, 'k8805': 6, 'sorialgi': 80};
        for(key in grades) {
            document.write("key : "+key+" value : "+grades[key]+"<br />");
        };
        
        key :   egoing value : 10
        key :   k8805 value : 6
        key :   sorialgi value : 80
        
        
        
        
        
    4) 객체 지향 프로그래밍
        
         var grades = {
            'list': {'egoing': 10, 'k8805': 6, 'sorialgi': 80}           
        };
        alert(grades['list'])
        alert(grades['list']['egoing'])
        
        
        
        var grades = {
            'list': {'egoing': 10, 'k8805': 6, 'sorialgi': 80},
            'show' : function(){
            
                for( name in this.list){
                    console.log(name + " , " + this.list[name])
                
                }
                console.log(this.list);
            }
        };
        grades['show']();
        
        
   
        
        
```


