---
title : "자바스크립트 알고리즘 문제풀이 - 3"
excerpt : "연필 개수"
categories : 
    - codingTest
tags : 
    - codingTest
---


<br><br> 

코딩테스트를 대비하여 문제를 한개씩 풀어보는 게 좋을 것 같아서 인프런 강의를 구매했다.  
매일은 아니더라도 꾸준히 공부해서 실력을 키워나가야지...!  
Lst's GO...!  

---
문제 : 연필 1 다스는 12자루입니다. 학생 1인당 연필을 1자루씩 나누어 준다고 할 때 N명이 학생수를 입력하면 필요한 연필의 다스 수를 계산하는 프로그램을 작성하세요.  
입력예제1 : 25      
출력예제1 : 3     

입력예제2 : 178      
출력예제2 : 15    

<br><br>

보통 나눗셈을 할때는 몫과 나머지를 같이 구한다.  
12로 학생 수를 나눴을 때, 나머지가 0이면 딱 맞게 떨어진다는 것이고  
나머지가 생긴다면 한다스가 더 필요하다는 소리다.  
그래서 나머지가 0보다 클 경우에 몫에 1을 더해주었다.  


<br>

내가 푼 내용  

```
function mySolution(student){
    let answer = parseInt(student / 12);
    if((student % 12) > 0){
        answer = answer + 1;
    }
    return answer;
}
```   

<br><br>   

정답코드를 보자...!   

```  
function solution(n){
    let answer;
    answer=Math.ceil(n/12);
    return answer;
}
```   

<br><br>   

정답을 보자마자 허탈해서 웃음이 나왔다.. ㅠㅠ  
아 함수를 쓸 생각을 못했다니...!!  
굳이 문제에 함수를 쓰지 말라는 조건이 없으면, 
언제든지 함수를 써도 된다는 걸 바보같이 간과하고 있었다ㅠ_ㅠ  
문제에도 방법이 있다는 것을... 잊지말자... ㅠㅠ  


<br><br>   

참고로 Math.ceil()에 대해서도 알아보잡..!  
Math.ceil 은 소수값이 존재할 때 값을 올리는 역활을 하는 함수이다.
올림이랑 같은 역할이라고 보면 된다.    
비슷한 애들로는 내림 역할을 하는 Math.floor, 반올림 역할을 하는 Math.round 가 있다.  
다음에 비슷한 문제가 나오면 잊지말고 써먹잡!!!  




