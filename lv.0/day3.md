# 코딩테스트 연습 > 코딩 기초 트레이닝 > Day3

## 1. 문자열 섞기
길이가 같은 두 문자열 str1과 str2가 주어집니다.
두 문자열의 각 문자가 앞에서부터 서로 번갈아가면서 한 번씩 등장하는 문자열을 만들어 return 하는 solution 함수를 완성해 주세요.
* str1:"aaaaa"	
* str2: "bbbbb"
* result: "ababababab"
```
function solution(str1, str2) {
 return [...str1].map((str, i)=> str + str2[i]).join("")
}
```
```
function solution(str1, str2) {
    let answer = '';
    for (let i = 0; i < str1.length; i ++) {
        answer += str1[i] + str2[i]
    }
    return answer;
}
```

## 2. 문자 리스트를 문자열로 반환하기
문자들이 담겨있는 배열 arr가 주어집니다. arr의 원소들을 순서대로 이어 붙인 문자열을 return 하는 solution함수를 작성해 주세요.
* arr:	["a","b","c"]
* result: "abc"
```
function solution(arr) {
    var answer = arr.join('');
    return answer;
}
```

## 3. 문자열 곱하기
문자열 my_string과 정수 k가 주어질 때, my_string을 k번 반복한 문자열을 return 하는 solution 함수를 작성해 주세요.
* my_string:"string"
* k:3
* result:"stringstringstring"
```
function solution(my_string, k) {
    let answer = '';
    answer = my_string.repeat(k)
    return answer;
}
```

## 4. 더 크게 합치기
연산 ⊕는 두 정수에 대한 연산으로 두 정수를 붙여서 쓴 값을 반환합니다. 예를 들면 다음과 같습니다.
* 12 ⊕ 3 = 123
* 3 ⊕ 12 = 312
양의 정수 a와 b가 주어졌을 때, a ⊕ b와 b ⊕ a 중 더 큰 값을 return 하는 solution 함수를 완성해 주세요.
단, a ⊕ b와 b ⊕ a가 같다면 a ⊕ b를 return 합니다.

* a ⊕ b = 991 이고, b ⊕ a = 919 입니다. 둘 중 더 큰 값은 991 이므로 991을 return 합니다.
```
function solution(a, b) {
    let answer1 = a.toString()+b.toString()
    let answer2 = b.toString()+a.toString()
    if(parseInt(answer1)>=parseInt(answer2)){
        return parseInt(answer1)
    } else {
        return parseInt(answer2)
    }
}
```
```
function solution(a, b) {
    return Math.max(Number(`${a}${b}`), Number(`${b}${a}`))
}
```

## 5. 두 수의 연산값 비교하기
	연산 ⊕는 두 정수에 대한 연산으로 두 정수를 붙여서 쓴 값을 반환합니다. 예를 들면 다음과 같습니다.
* 12 ⊕ 3 = 123
* 3 ⊕ 12 = 312
양의 정수 a와 b가 주어졌을 때, a ⊕ b와 2 * a * b 중 더 큰 값을 return하는 solution 함수를 완성해 주세요.
단, a ⊕ b와 2 * a * b가 같으면 a ⊕ b를 return 합니다.
```
function solution(a, b) {
    let answer1 = parseInt(a.toString()+b.toString());
    let answer2 = 2*a*b
    return Math.max(answer1, answer2)
}
```
```
function solution(a, b) {
    let num1 = parseInt(a+""+b+"");
    let num2 = 2*a*b;
    return num1 > num2 ? num1 : num2;
}
``
