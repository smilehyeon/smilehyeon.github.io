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
문제 : 7개의 자연수가 주어질 때, 이들 중 홀수인 자연수들을 모두 골라 그 합을 구하고, 고른 홀수들 중 최소값을 찾는 프로그램을 작성하세요  

입력예제1 : 12 77 38 41 53 92 85 ( 주어지는 자연수는 100보다 작다. 홀수가 한 개 이상 반드시 존재한다.)  
출력예제1 : 256(합) 41(최솟값)  

<br><br>

홀수는 2로 나누었을 때 나머지가 1인 수를 구하면 되고,  
최솟값은 저번에 배웠던 Number.MAX_SAFE_INTEGER 를 활용해보기로 했다.  
수들을 배열로 받는다고 했을 때, 값 하나씩 비교하려면 for문을 이용해야 한다.  


<br>

내가 푼 내용  

```
function mySolution(a){
    let answer = new Object;
    let min=Number.MAX_SAFE_INTEGER, sum=0;

    for(let i=0; i<arr.length; i++){
        if (arr[i]%2 == 0){ //홀수 판별
            sum+=arr[i];
            if(arr[i]<min){ //최솟값
                min = arr[i];
            }
        }
    }
    answer.sum = sum;
    answer.min = min;

    return answer;
}
```   

<br><br>   

정답코드를 보자...!   

```  
function solution(n){
    let answer = new Object;
    let sum=0, min=1000;
    for(let x of arr){
        if(x%2===1){
            sum+=x;
            if(x<min) min=x;
        }
    }
    answer.sum = sum;
    answer.min = min;   
    return answer;
}
```   

<br><br>   

전제조건에서 자연수는 100보다 작은 수라고 명시를 해놨기 때문인지,  
이번에는 초기값을 1000으로 두고 한 것 같다. ㅎㅎ  
그리고 가장 다른 점은 for문...!  
나는 항상 기본 형태의 for문에 익숙한데,  
향상된 for문을 사용할 수 있다는 것을 간과했다....  
사실 특정 구간까지 반복할 필요가 없는 이상, 향상된 for문이 훨씬 간단하고 쓰기도 편한데...  
앞으로 향상된 for문 사용하는 것에 익숙해져야 할 것 같다 ㅠ_ㅠ  
또, 다른 점이 하나 있다. 바로 값 비교하는 구문!  
정확한 값을 비교할 때는 ===을 써야하는데,  
이것 역시 ==에 익숙해져서 생긴 결과인 것 같다.  
더 나은 것, 새로운 것들을 알게 됐다면 익숙하지 않더라도 의식적으로 쓰도록 노력해야겠다. 꼭 !!!  
**익숙함에 속아 안주하지 말자!**  
<br><br>   





