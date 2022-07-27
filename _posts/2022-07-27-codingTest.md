---
title : "자바스크립트 알고리즘 문제풀이 - 6"
excerpt : "홀수"
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
문제 : 대문자로 이루어진 영어단어가 입력되면 단어에 포함된 ‘A'를 모두 ’#‘으로 바꾸어 출력하는 프로그램을 작성하세요.   

입력예제1 : BANANA  
출력예제1 : B#N#N#    

<br><br>

입력받은 문자열을 하나씩 떼는 게 관건이었기 때문에,  
split으로 문자 하나씩 잘랐다.  
그리고 A일 때 #으로 바꾸고 문자들을 하나씩 누적해서 출력했다!  



<br>

내가 푼 내용  

```
function mySolution(date, arr){
    let answer="";
    let arr = str.split("");

    for(let i=0; i<arr.length; i++){
        if(arr[i] === "A"){
            arr[i] = "#";
        }
        answer += arr[i];
    }

    return answer;
}
```   

<br><br>   

정답코드를 보자...!   

```  
function solution(date, arr){
    let answer="";
    for(let x of str){
        if(x=='A') answer+='#';
        else answer+=x;
    }
    return answer;
}
```   

<br><br>   

문자열을 for문으로 바로 받아서 구현할 수 있다는 사실을 전혀 몰랐다...!!!  
새로운 사실을 알게됐다 ㅋㅋ  
그리고 나는 문자열을 #으로 바꾼 뒤, 그걸 다시 배열에 넣었는데 불필요한 과정이었다.  
어차피 문자 하나씩 누적해주는 형태이기 때문에 바로 answer에 누적해주면 되는 거였는데...ㅠㅠ  
불필요한 과정은 없는지 꼭꼭 확인하는 작업이 필요할 것 같다.  
그리고 아직 내가 모르는 것들이 정말 많구나 라고 생각이 들었다.  
꾸준히 공부해나가자....!!!  
<br><br>   





