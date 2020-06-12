# 정수 내림차순으로 배치하기

### 1. 문제 설명

- 함수 solution은 정수 n을 매개변수로 입력받습니다. n의 각 자릿수를 큰것부터 작은 순으로 정렬한 새로운 정수를 리턴해주세요. 예를들어 n이 118372면 873211을 리턴하면 됩니다.

*출처: 프로그래머스 코딩 테스트 연습,* https://programmers.co.kr/learn/challenge

### 2. 문제풀이

```javascript
function solution(n) {
    /*
    var answer = [];
    var answer2 = [];
    var Char=String(n);
    answer.unshift(Char);
    answer=Char.split("").map(Number);
    var l = answer.length;
    for(var i=0;i<l;i++){
        var max = Math.max.apply(null, answer);
        answer.splice(answer.indexOf(max),1);
        Char=String(max)
        answer2.push(Char);
        var answer3=answer2.join('');
        answer3=parseInt(answer3)
    }
    return answer3;*/
    return (Number)(String(n).split("").sort().reverse().join(""));
}
```

- 정수 'n'을 문자열로 변환하고 split함수를 이용해서 각각 쪼갠다.
- reverse()함수를 이용해서 쪼갠 문자들을 반대로 뒤집고 join함수를 이용해서 문자열을 합친다
- 끝으로 Number를 이용해서 정수형으로 다시 변환한다.
- 주석 처리된 코드로도 작동은 된다. 다만 더 쉬운 방법이 있기 때문에 위의 설명을 참고한다.