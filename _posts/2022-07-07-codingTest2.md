---
title : "자바스크립트 알고리즘 문제풀이 - 2"
excerpt : "삼각형 만들기"
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
문제 : 길이가 서로 다른 A, B, C 세 개의 막대 길이가 주어지면 이 세 막대로 삼각형을 만들 수 있으면 “YES"를 출력하고, 만들 수 없으면 ”NO"를 출력한다.  
입력예제1 : 6 7 11    
출력예제1 : YES   

입력예제2 : 13 33 17    
출력예제2 : NO   

<br><br>

삼각형의 조건에 대해서 먼저 알아보자.  
세 변의 길이를 알고있을 때, 삼각형이 되려면 가장 큰 변의 길이가 나머지 두 변의 길이 합보다 짧아야한다.  
가장 큰 값을 먼저 구한 뒤, 세 변의 합에서 큰 값을 빼면 나머지 두 변의 길이 합이 된다.  
두 변의 길이 합과 큰 값을 비교만 하면 답이 나온다.  

<br>

내가 푼 내용  

```
function solution(a, b, c){
  let answer;
  let max;
  
  if(a>b){
      max = a;
  }else{
      max = b;
  }
  if(c > max){
      max = c;
  }

  if((a+b+c)-max > max){
      answer = "YES";
  }else{
      answer = "NO";
  }
  return answer;
}
```   

<br><br>   

정답코드를 보자...!   

```  
let answer="YES", max;
let tot=a+b+c;
if(a>b) max=a;
else max=b;
if(c>max) max=c;
if(tot-max<=max) answer="NO"; 
return answer;
```   

<br><br>   

이번에는 얼추 비슷했던 것 같다.   
어차피 들어오는 숫자는 형식이 정해져있고, YES 아니면 NO이니까   
초기에 YES로 설정해두는 것도 좋은 방법인 것 같다.   
굳이 else문을 추가해줄 필요가 없으니 말이다.   
그리고 변수를 ```let answer, max;``` 와 같은 형태로 구현할 수 있는 것도 몰랐다.   
단순한 JS 사용법인데도 모르고 있었다니..ㅠㅠㅠ   
아직 많은 공부가 필요하다는 걸 깨닫는 하루다...  


<br><br>   





