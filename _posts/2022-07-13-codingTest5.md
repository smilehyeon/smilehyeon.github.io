---
title : "자바스크립트 알고리즘 문제풀이 - 5"
excerpt : "최솟값 구하기"
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
문제 : 7개의 수가 주어지면 그 숫자 중 가장 작은 수를 출력하는 프로그램을 작성하세요.  

입력예제1 : 5 3 7 11 2 15 17       
출력예제1 : 2     

<br><br>

최솟값을 구해주는 함수를 이용했다.  
또한, 입력받은 수들은 배열 형태로 받기 때문에,  
es6에서 새로 추가된 문법인 Spread operator를 사용하였다.  


<br>

내가 푼 내용  

```
function mySolution(arr){
    let answer = Math.min(...arr);
    return answer;
}
```   

<br><br>   

정답코드를 보자...!   

```  
function solution(arr){
    let answer, min=Number.MAX_SAFE_INTEGER;
    for(let i=0; i<arr.length; i++){
        if(arr[i]<min) min=arr[i];
    }
    answer=min;
    return answer;
}
```   

<br><br>   

처음보는 녀석이 있다.  
바로 Number.MAX_SAFE_INTEGER  
이녀석의 정체는 무엇일까?  
이녀석은 JavaScript에서 안전한 최대 정수값을 나타낸다고 한다.  
정수를 정확하고 올바르게 비교할 수 있는 안전함 때문에 사용한다고 한다.  
알고리즘에서는 코드를 간단하게 하는 것도 중요하지만, 안전함 문제도 중요하다는 것을 명심해야겠다.  
<br><br>   





