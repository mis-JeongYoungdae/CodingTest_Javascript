# 정수 제곱근 판별

### 1. 문제 설명

- 임의의 양의 정수 n에 대해, n이 어떤 양의 정수 x의 제곱인지 아닌지 판단하려 합니다.
  n이 양의 정수 x의 제곱이라면 x+1의 제곱을 리턴하고, n이 양의 정수 x의 제곱이 아니라면 -1을 리턴하는 함수를 완성하세요.
- n은 1이상, 50000000000000 이하인 양의 정수입니다.

*출처: 프로그래머스 코딩 테스트 연습,* https://programmers.co.kr/learn/challenge

### 2. 문제풀이

```javascript
function solution(n) {
    var answer = 0;
    var c=Math.sqrt(n);
    var j=Number.isInteger(c);
    if(j===true){
        answer=(c+1)*(c+1);
    }else{
        answer=-1;
    }
    return answer;
}
```

- Math.sqrt()는 인자값의 제곱근을 구해주는 함수이다.
- Number.isInteger()는 값이 정수인지 아닌지를 판별해서 결과값으로 true or false를 갖는다.