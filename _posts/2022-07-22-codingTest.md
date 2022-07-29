---
title : "자바스크립트 알고리즘 문제풀이 - 7"
excerpt : "10부제"
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
문제 : 주어진 날짜와 자동차의 일의 자리 숫자를 보고 10부제를 위반하는 차량의 대수를 출력합니다.

입력예제1 : 3(날짜) / 25 23 11 47 53 17 33 (자동차 번호)  
출력예제1 : 3  

<br><br>

이번에는 내가 푼 내용과 정답 코드가 똑같았다...!!!  
근데 내가 풀면서 생각한 방법이 두가지였기 때문에  
정답코드와 다르게 생각했던 방법으로 적어야겠다.  

우선, 주어지는 숫자를 문자열로 바꾸게 되면  
자동차 번호 중 마지막 문자만 잘라내면 우리가 필요로 하는 자동차의 일의 자리 숫자가 된다.  
그 숫자와 주어진 날짜를 비교만 하면 끝!!  


<br>

내가 푼 내용  

```
function mySolution(date, arr){
    let answer=0;
    for(let i of arr){
        if (i.toString().slice(-1)===date){
            answer++;
        }
    }
    return answer;
}
```   

<br><br>   

정답코드를 보자...!   

```  
function solution(date, arr){
    let answer=0;
    for(let x of arr){
        if(x%10==date) answer++;
    }
    return answer;
}
```   

<br><br>   

이번에는 향상된 for문을 써서 했다 (뿌듯)  
주어진 차량 번호를 10으로 나누고 그 나머지를 구하면,   
나머지가 바로 차량의 마지막 번호가 된다.  
나머지와 날짜를 비교하기만 하면 된다.  
<br><br>   





