---
title : "프로그래머스 level1 - 2 (스택/큐)"
excerpt : "같은 숫자는 싫어.."
categories : 
    - codingTest
tags : 
    - codingTest
---


<br><br> 

프로그래머스에 있는 레벨별 문제도 하나씩 풀어보기로 했다 ㅎㅎgg    

---
[문제설명 클릭](https://school.programmers.co.kr/learn/courses/30/lessons/12906)  

<br><br>
   


내가 푼 내용  

```
function solution(arr) {
    var answer = [];
    for (let i = 0; i < arr.length; i++) {
        if (arr[i] != answer[answer.length - 1]) {
            answer.push(arr[i]);
        }
    }
    return answer;
}
```   

arr의 각 배열의 값과 answer의 마지막에 push 한 값을 비교한다.  
answer에는 연속적인 숫자는 단 하나만 담았기 때문에, 마지막에 담긴 값을 비교해야한다.  
비교했을 때, answer의 마지막 값과 다르다면 당연히 연속적이지 않은 숫자이므로 push하고  
같다면 연속적인 숫자이므로 push  하지 않는다.  
이 과정을 arr의 크기만큼 반복하면 된다!  
<br><br>   

다른 사람들의 정답 코드  

 ```
function solution(arr) {
    return arr.filter((val,index) => val != arr[index+1]);
}
```   

<br><br>   

오호홋...    
이렇게나 간단한 방법이 있었다니...!!!!!  
filter에 대해서 자세히 알지 못하기 때문에, 사용할 생각을 못하고 있었다 ㅠ_ㅜ  
filter는 해석 그대로, 특정 조건을 만족하는 새로운 배열을 필요로 할 때 사용한다.  
배열의 값을 순차적으로 접근하여, callbackfn을 통해 true인 애들만 신규배열로 만든다.  
새로운 것을 배웠으니, 다음에 사용할 일이 있으면 꼭 사용을 해봐야겠다!  
[filter 참고](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Global_Objects/Array/filter)
<br><br>   





