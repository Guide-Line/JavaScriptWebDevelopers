## 배열 

#### 배열(array)이란 연관된 데이터를 모아서 통으로 관리하기 위해서 사용하는 데이터 타입이다. 



```javascript
	
    1) 배열의 생성
    
        var member = ['egoing', 'k8805', 'sorialgi']
    
    2) 데이터를 꺼내는 방법
   
        var member = ['egoing', 'k8805', 'sorialgi']
        alert(member[0]);
        alert(member[1]);
        alert(member[2]);
        
        
    3) 배열이 없다면? 
    
        function get_member1(){
            return 'egoing';
        }
        document.write(get_member1());

        function get_member2(){
            return 'k8805';
        }
        document.write(get_member2());


        function get_member3(){
            return 'sorialgi'
        }
        document.write(get_member3());
    
        입력값은 여러개 출력은 한개
        
        function get_members(){
            return ['egoing', 'k8805', 'sorialgi'];
        }
        var members = get_members();
        document.write(members[0]);
        document.write(members[1]);
        document.write(members[2]);
        
        이처럼 연관된 부분을 편하게 다룰수 있다.
        
        
    4) 배열의 사용 ( 반복문과의 만남 ) : 복수의 데이터를 효율적으로 관리하기 위함
        
        	
        function get_members(){
            return ['egoing', 'k8805', 'sorialgi'];
        }
        members = get_members();
        // members.length는 배열에 담긴 값의 숫자를 알려준다. 
        for(i = 0; i < members.length; i++){
            // members[i].toUpperCase()는 members[i]에 담긴 문자를 대문자로 변환해준다.
            document.write(members[i].toUpperCase());   
            document.write('<br />');
        }
        
    5) 배열의 크기 
    
        var arr = [1, 2, 3, 4, 5];
        alert(arr.length);
        
        
    6) 배열의 조작 
        
        추가)
        
        push는 인자로 전달된 값을 배열(li)에 추가하는 명령
        var li = ['a', 'b', 'c', 'd', 'e'];
        li.push('f');
        alert(li);
        
        concat은 인자로 전달된 값을 추가하는 명령
        var li = ['a', 'b', 'c', 'd', 'e'];
        li = li.concat(['f', 'g']);
        alert(li);
        
        unshift는 인자로 전달한 값을 배열의 첫번째 원소로 추가하고 배열의 기존 값들의 색인을 1씩 증가
        var li = ['a', 'b', 'c', 'd', 'e'];
        li.unshift('z');
        alert(li);
        
        splice는 첫번째 인자에 해당하는 원소부터 두번째 인자에 해당하는 원소의 숫자만큼의 값을 배열로부터 제거한 후에 리턴
        var li = ['a', 'b', 'c', 'd', 'e'];
        li.splice(2, 0, 'B');
        alert(li);
        
        제거)
        
        배열의 첫번째 원소를 제거하는 방법
        var li = ['a', 'b', 'c', 'd', 'e'];
        li.shift();
        alert(li);
        
        배열 끝점의 원소를 배열 li에서 제거
        var li = ['a', 'b', 'c', 'd', 'e'];
        li.pop();
        alert(li);
        
        
        정렬)
        
        순서대로 정렬
        var li = ['c', 'e', 'a', 'b', 'd'];
        li.sort();
        alert(li);
        
        역순정렬
        var li = ['c', 'e', 'a', 'b', 'd'];
        li.reverse();
        alert(li);
        
        
```


