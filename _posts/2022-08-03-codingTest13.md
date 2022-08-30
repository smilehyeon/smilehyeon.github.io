---
title : "프로그래머스 level1 - 1"
excerpt : "신고 결과 받기"
categories : 
    - codingTest
tags : 
    - codingTest
---


<br><br> 

프로그래머스에 있는 레벨별 문제도 하나씩 풀어보기로 했다 ㅎㅎ  

---
[문제설명 클릭](https://school.programmers.co.kr/learn/courses/30/lessons/92334) 

<br><br>
   


처음 푼 내용  

```
function solution(id_list, report, k) {
    var answer = new Array(id_list.length).fill(0);
    var reportCnt = new Array(id_list.length).fill(0); //신고횟수
    var mailCnt = new Array(id_list.length).fill(0); //메일횟수
    let newReport = [...new Set(report)]; //중복제거
    var banId = []; //정지회원

    for (let i = 0; i < newReport.length; i++) {
        var reportArr = newReport[i].split(' ');
        reportCnt[id_list.indexOf(reportArr[1])] += 1; //신고당한 회원의 신고횟수 올려줌
        if (reportCnt[id_list.indexOf(reportArr[1])] >= k) { //신고횟수가 2회 이상이면 정지회원에 등록
            banId.push(id_list[i]);
        }
    }

    for (let i = 0; i < newReport.length; i++) {
        var reportArr = newReport[i].split(' ');
        var reportUsr = newReport[i].split(' ')[0]; //신고하는 회원
        var reportBanUsr = newReport[i].split(' ')[1]; //신고당한 회원
        if (banId.includes(reportBanUsr)) { //신고당한 회원이 정지회원에 있다면, 메일 발송한다.  
            answer[id_list.indexOf(reportUsr)] += 1;
        }
    }
    return answer;
}
```   

<br><br>   
위의 내용 대로 풀었는데...  
시간이 초과되어서 실패했다..  
그 이유는 바로 for문에 있었다.  

 ```
function solution(id_list, report, k) {
    var answer = new Array(id_list.length).fill(0);
    var reportCnt =  new Array(id_list.length).fill(0); 
    let newReport = [...new Set(report)]; 
    var banId = []; 
    
    for(let x of newReport){
        var reportArr = x.split(" ");
        var idIdx = id_list.indexOf(reportArr[1])
        reportCnt[idIdx] += 1;
        
        if(reportCnt[idIdx] >= k){
            banId.push(id_list[idIdx]);
        }
    }
    
    for (let x of newReport) {
            var reportUsr = x.split(' ')[0]; 
            var reportBanUsr = x.split(' ')[1]; 

            if (banId.includes(reportBanUsr)) {
                answer[id_list.indexOf(reportUsr)] += 1;
            }
        }
    
    return answer;
}
```   

<br><br>   

그래서 이렇게 수정했더니 해결됐다....!!!  
일반적인 for문을 돌릴 때, 보통 배열의 크기만큼 크기도 지정하고..  
배열 인덱스를 정해놓고 그때마다 접근하기도 한다.  
그런데 그런 과정에서 시간을 잡아먹는다고 한다.  
그래서 for..of 문으로 바꾸었더니 해결되었다...!!!!  
코드를 짤 때 for..of 사용을 생활화할 수 있도록 노력해야겠다.  
<br><br>   





