---
title : "자바스크립트 알고리즘 문제풀이 - 4"
excerpt : "1부터 N까지 합 출력하기"
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
문제 : 자연수 N이 입력되면 1부터 N까지의 합을 출력하는 프로그램을 작성하세요. 
입력예제1 : 6      
출력예제1 : 21     

입력예제2 : 10      
출력예제2 : 55    

<br><br>

1부터 n까지 반복해서 덧셈을 해야하기 때문에 for문을 이용했다.  


<br>

내가 푼 내용  

```
function mySolution(a){
    let answer=0;
    for(let i=1; i<=a; i++){
        answer+=i;
    }
    return answer;
}
```   

<br><br>   

정답코드를 보자...!   

```  
function solution(n){
    let answer=0;
    for(let i=1; i<=n; i++){
        answer=answer+i;
    }
    return answer;
}
```   

<br><br>   

이번에는 정답코드와 똑같다....!!!   
다른 부분은 연산자 부분 ㅎㅎ   
나같은 경우에는 어차피 answer라는 변수에 i 값만 누적해주면 된다고 생각해서   
간단하게 누적대입연산자 += 를 사용했다.  


<br><br>   





