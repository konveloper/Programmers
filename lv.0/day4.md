# 코딩테스트 연습 > 코딩 기초 트레이닝 > Day4

## 1. n의 배수
정수 num과 n이 매개 변수로 주어질 때, num이 n의 배수이면 1을 return n의 배수가 아니라면 0을 return하도록 solution 함수를 완성해주세요.
```
function solution(num, n) {
    if(num%n===0){
        return 1
    } else {
        return 0
    }
}
```
```
function solution(num, n) {
    return num%n===0?1:0;
}
```

## 2. 공배수
정수 number와 n, m이 주어집니다. number가 n의 배수이면서 m의 배수이면 1을 아니라면 0을 return하도록 solution 함수를 완성해주세요.
```
function solution(number, n, m) {
    return number%n===0 && number%m===0 ? 1 : 0
}
```

## 3. 홀짝에 따라 다른 값 반환하기
양의 정수 n이 매개변수로 주어질 때, n이 홀수라면 n 이하의 홀수인 모든 양의 정수의 합을 return 하고 n이 짝수라면 n 이하의 짝수인 모든 양의 정수의 제곱의 합을 return 하는 solution 함수를 작성해 주세요.
```
      function solution(n) {
        if (n % 2 === 1) {
          let arrOdd = [];
          for (let i = 1; i <= n; i += 2) {
            arrOdd.push(i);
          }
          let sumOdd = 0;
          arrOdd.forEach(function (item) {
            sumOdd += item;
          });
          return sumOdd;
        } else {
          let arrEven = [];
          for (let i = 2; i <= n; i += 2) {
            arrEven.push(i);
          }
          let powerEven = 0;
          for (let num of arrEven) {
            powerEven += num * num;
          }
          return powerEven;
        }
      }

```

## 4. 조건 문자열
문자열에 따라 다음과 같이 두 수의 크기를 비교하려고 합니다.
* 두 수가 n과 m이라면
    * ">", "=" : n >= m
    * "<", "=" : n <= m
    * ">", "!" : n > m
    * "<", "!" : n < m
두 문자열 ineq와 eq가 주어집니다. ineq는 "<"와 ">"중 하나고, eq는 "="와 "!"중 하나입니다. 그리고 두 정수 n과 m이 주어질 때, n과 m이 ineq와 eq의 조건에 맞으면 1을 아니면 0을 return하도록 solution 함수를 완성해주세요.
		

## 5. flag에 따라 다른 값 반환하기
두 정수 a, b와 boolean 변수 flag가 매개변수로 주어질 때, flag가 true면 a + b를 false면 a - b를 return 하는 solution 함수를 작성해 주세요.
```
function solution(a, b, flag) {
    if(flag === true) {
        return a + b
    } else return a - b
}
```
```
function solution(a, b, flag) {
    return flag ? a + b : a - b;
}
```
