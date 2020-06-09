# 약수의 합

### 1. 문제 설명

- 정수 n을 입력받아 n의 약수를 모두 더한 값을 리턴하는 함수, solution을 완성해주세요.
- `n`은 0 이상 3000이하인 정수입니다.

*출처: 프로그래머스 코딩 테스트 연습,* https://programmers.co.kr/learn/challenge

### 2. 문제풀이

```javascript
function solution(n) {
    var answer = 0;
    for(var i=0;i<=3000;i++){
        if(n%i===0){
            answer+=i;
            if(n===0){
                answer=0;
            }
        }
    }
    return answer;
}
```

- n은 0보다 크고 3000보다는 작거나 같다
- i의 조건을 3000보다 작거나 같게 조건을 부여한다.
- n을 i로 나눈 나머지가 0인 경우 i는 n의 약수로 보며 그 값들을 더한다.