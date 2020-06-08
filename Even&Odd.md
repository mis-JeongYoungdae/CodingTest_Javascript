# 짝수와 홀수

### 1. 문제 설명

![image-20200608093832125](C:\Users\JungJiYun\AppData\Roaming\Typora\typora-user-images\image-20200608093832125.png)

*출처: 프로그래머스 코딩 테스트 연습,* https://programmers.co.kr/learn/challenges



### 2. 문제풀이

```javascript
function solution(num) {
    var answer = '';
    if(num%2===0){
        answer="Even";
    }else{
        answer="Odd";
    }
    return answer;
}
```

- num 이라는 값이 들어왔을 때 그 넘을 2로 나눈 나머지와 비교한다
- 만약 0이 나오면 "Even"을 answer에 할당한다.
- 그렇지 않는 경우는 "Odd" 값을 answer에 할당한다.