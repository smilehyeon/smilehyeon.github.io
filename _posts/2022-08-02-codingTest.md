---
title : "자바스크립트 알고리즘 문제풀이 - 12"
excerpt : "대문자로 통일"
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
문제 : 대문자와 소문자가 같이 존재하는 문자열을 입력받아 대문자로 모두 통일하여 문자열을 출력하는 프로그램을 작성하세요.  
 

입력예제1 : ItisTimeToStudy      
출력예제1 : ITISTIMETOSTUDY       

<br><br>
 
문자를 대문자로 바꾸어주는 toUpperCase()를 사용하여 대문자로 바꿔주었다!    



<br>

내가 푼 내용  

```
function mySolution(str, char){
    let answer = str.toUpperCase();
    return answer;
}
```   

<br><br>   
정답코드!!  

 ```
function mySolution(str, char){
    let answer = "";

    for(let x of str){
        let num=x.charCodeAt();
        if(num>=97 && num<=122) answer+=String.fromCharCode(num-32);
        else answer+=x;

        //if(x===x.toLowerCase()) answer+=x.toUpperCase();
        //else answer+=x;
    }

    return answer;
}
```   

<br><br>   

정답 코드를 보니, 문자를 하나씩 잘라서 대문자인지 소문자인지 비교한 다음에   
대문자일 경우에는 그냥 누적, 소문자일 경우에는 대문자로 바꾼 뒤에 누적했다.  
fromCharCode가 뭔가 싶어서 검색했더니,  
아스키 코드를 문자열로 바꿔주는 거라고 한다!!!  
오늘도 새로운 지식 Get,,,,  
<br><br>   





