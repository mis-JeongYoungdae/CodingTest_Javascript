평균 구하기

### 1. 문제 설명

- 정수를 담고 있는 배열 arr의 평균값을 return하는 함수, solution을 완성해보세요.
- arr은 길이 1 이상, 100 이하인 배열입니다.
- arr의 원소는 -10,000 이상 10,000 이하인 정수입니다.

*출처: 프로그래머스 코딩 테스트 연습,* https://programmers.co.kr/learn/challenge

### 2. 문제풀이

```javascript
function solution(arr) {
    var answer = 0;
    const numbers=arr.map(number=>parseInt(number))
    let sum=0
    numbers.forEach(num=>{
        sum += num
        answer=sum/arr.length;
    })
    return answer;
}
```

- arr.map을 이용해서 배열에 있는 값을 parseInt로 정수로 변환한다
- 그 값들을 forEach를 이용해서 sum이라는 변수에 각각의 배열들을 더하는 작업을 한다
- 그 값에 배열의 길이를 나눠서 평균값을 구한다.