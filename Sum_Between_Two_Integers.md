# 두 정수 사이의 합

### 1. 문제 설명

- 두 정수 a, b가 주어졌을 때 a와 b 사이에 속한 모든 정수의 합을 리턴하는 함수, solution을 완성하세요.
- 예를 들어 a = 3, b = 5인 경우, 3 + 4 + 5 = 12이므로 12를 리턴합니다
- a와 b가 같은 경우는 둘 중 아무 수나 리턴하세요.

*출처: 프로그래머스 코딩 테스트 연습,* https://programmers.co.kr/learn/challenge

### 2. 문제풀이

```javascript
function solution(a, b) {
        if(a===b){
            var answer=a;
        }else{
            if(a<b){
                var c = b
                for(var i=a;i<b;i++){
                    c+=i;
                    answer=c;
                }
            }else{
                var c =a
                for(var i=b;i<a;i++){
                    c+=i;
                    answer=c;
                }
            }
        }
    return answer;
}
```

- if문을 활요하여 a,b 두 값이 같을 때는 둘 중에 아무 값이나 내보낸다
- a와 b 값을 비교하여 작은 값을 i에 할당 하고 큰 값은 c에 할당 한다.
- for 문을 이용하여 c에 i값을 더해서 대입한다.