# 자연수 뒤집어 배열로 만들기

### 1. 문제 설명

- 자연수 n을 뒤집어 각 자리 숫자를 원소로 가지는 배열 형태로 리턴해주세요. 예를들어 n이 12345이면 [5,4,3,2,1]을 리턴합니다.

*출처: 프로그래머스 코딩 테스트 연습,* https://programmers.co.kr/learn/challenge

### 2. 문제풀이

```javascript
function solution(n) {
    var answer = [];
    var Char=String(n);
    answer.unshift(Char);
    answer=Char.split("").map(Number);
    answer=answer.reverse();
    return answer;
}
```

- 변수 Char에 문자열로 변환한 'n'을 넣는다.
- split함수를 이용해서 문자열을 하나씩 나누고 map을 이용해서 각 요소들을 숫자형으로 바꾼다.
- reverse함수를 사용해서 배열을 반대로 바꾼다.