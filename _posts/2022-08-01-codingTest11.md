---
title : "자바스크립트 알고리즘 문제풀이 - 11"
excerpt : "대문자 찾기"
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
문제 : 한 개의 문자열을 입력받아 해당 문자열에 알파벳 대문자가 몇 개 있는지 알아내는 프로그램을 작성하세요.  
 

입력예제1 : KoreaTimeGood      
출력예제1 : 3      

<br><br>

for문으로 문자열을 한글자씩 뽑아서, 그 문자의 대문자 형태와 동일하면 결과 변수에 1씩 누적을 해주었다.  
문자를 대문자로 바꾸어주는 toUpperCase()를 사용했당!!  



<br>

내가 푼 내용  

```
function mySolution(str, char){
    let answer = 0;

    for (let i of str) {
        if (i === i.toUpperCase()) {
            answer++;
        }
    }

    return answer;
}
```   

<br><br>   
 오늘 정답코드와 동일하게 풀었다 우하하  
 그런데, 저 방법 말고도 아스키 코드를 활용한 풀이법도 있어서 적어볼까 한답  

 ```
function mySolution(str, char){
    let answer = 0;

    for (let i of str) {
        let num=x.charCodeAt();
        if(num>=65 && num<=90) answer++;
    }

    return answer;
}
```   

<br><br>   

역시.. 문제를 푸는 데엔 정해진 답이 없다는 것을 느끼게 되는 하루다.  
아스키 코드를 활용하는 것은 생각하지도 않았는데!!!!  
아스키 코드를 평소에 외울 일이 없었다는 것도 한몫 하겠다...ㅠㅠ  
그렇지만 대문자, 소문자 알파벳의 아스키 코드정도는 활용도가 많으니 외워두는 것도 좋을 것 같다!!!  
대문자 알파벳의 아스키 코드 : 65 ~ 90  
소문자 알파벳의 아스키 코드 : 97 ~ 122
<br><br>   





