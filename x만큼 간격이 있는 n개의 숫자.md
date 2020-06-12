# x만큼 간격이 있는 n개의 숫자

### 1. 문제 설명

- 함수 solution은 정수 x와 자연수 n을 입력 받아, x부터 시작해 x씩 증가하는 숫자를 n개 지니는 리스트를 리턴해야 합니다. 다음 제한 조건을 보고, 조건을 만족하는 함수, solution을 완성해주세요.

*출처: 프로그래머스 코딩 테스트 연습,* https://programmers.co.kr/learn/challenge

### 2. 문제풀이

```javascript
function solution(x, n) {
    var answer = [];

    for(var i =1; i<n+1;i++){
        answer.push(i*x)
    }
    return answer;
}
```

- i를 for문으로 n번 실행한다. 
- 1부터 n까지 x를 곱한다.
- 그 값을 push해서 배열에 넣는다.



### 3. 시행착오

```javascript
function solution(x, n) {
    var answer = [];
    var result = 0;
        answer.push(x)
    for(var i=0;i<n;i++){
        result+=answer[0]
    }
    return result;
}
```



- var i = i로 해서 실행이 안됐다.
- for문 밖에 push를 해서 push가 한 번 밖에 들어가지 않았다.
- answer[0]번째가 위에 for문에 명시되어있는 n개 만큼 더해서 값이 result에 들어가질줄 알았는데 그렇게 되지 않았다.