---
title : "프로그래머스 level1 - 3"
excerpt : "성격유형 검사하기"
categories : 
    - codingTest
tags : 
    - codingTest
---


<br><br> 

즐거운 휴가를 마치고...!  
다시 시작하자!!!  

---
[문제설명 클릭](https://school.programmers.co.kr/learn/courses/30/lessons/118666?language=javascript#)  

<br><br>
   


내가 푼 내용  

```
function solution(survey, choices) {
    let answer = '';
    let type = new Map();
    let typeArr = ["RT", "CF", "JM", "AN"];
    
    Array("R","T","C","F","J","M","A","N").forEach(x=>type.set(x,0));

    survey.forEach((s, i) => {
        let score = choices[i]-4; // 선택 점수
        if(score < 0){
            type.set(s[0], type.get(s[0]) + Math.abs(score));
        }else if(score > 0){
            type.set(s[1], type.get(s[1]) + score);
        }
    });

    for(let e of typeArr){
        answer += (type.get(e[0]) >= type.get(e[1]) ? e[0] : e[1]);
    }

    return answer;
}
```   

잠을 못자서 그런지 유독 헤맸다...ㅠㅠㅠ  
특히 score에서 -4를 해놓고선 점수 누적하는 부분에서 실수가 있었는데  
그걸 못발견해서 30분을 잡아먹었다ㅠ_ㅠ  
생각해보니 음수는 양수로 변환해야했....ㅎㅎㅎㅎ  
어쩐지 정확성 테스트에서 자꾸 떨어져서 왜 그러지 하고 한참을 고민했다  
역시.... 컴퓨터가 나보다 정확하다.  


<br><br>   

다른 사람들의 정답 코드  

 ```
function solution(survey, choices) {
    const MBTI = {};
    const types = ["RT","CF","JM","AN"];

    types.forEach((type) =>
        type.split('').forEach((char) => MBTI[char] = 0)
    )

    choices.forEach((choice, index) => {
        const [disagree, agree] = survey[index];

        MBTI[choice > 4 ? agree : disagree] += Math.abs(choice - 4);
    });

    return types.map(([a, b]) => MBTI[b] > MBTI[a] ? b : a).join("");
}
```   

<br><br>   

나온지 얼마 안된 문제여서 그런지 정답 코드들이 많은 편은 아니었다 ㅎㅎ  
나와 동일하게 -4를 해주고 양수로 변환해서 풀었다.  
그렇지만 내 코드보다 깔끔하고, 훨씬 가독성이 좋아서 참고해야겠다.  
<br><br>   





