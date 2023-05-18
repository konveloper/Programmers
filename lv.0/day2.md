
# 코딩테스트 연습 > 코딩 기초 트레이닝 > Day2

## 1. 		덧셈식 출력하기
두 정수 a, b가 주어질 때 다음과 같은 형태의 계산식을 출력하는 코드를 작성해 보세요.
* 입력<br>
4 5
* 출력<br>
4 + 5 = 9

```
rl.on('line', function (line) {
    input = line.split(' ');
}).on('close', function () {
    console.log(Number(input[0]) + " + " + Number(input[1]) +
" = " + (Number(input[0]) + Number(input[1])));
});
```

## 2. 문자열 붙여서 출력하기
두 개의 문자열 str1, str2가 공백으로 구분되어 입력으로 주어집니다. 입출력 예와 같이 str1과 str2을 이어서 출력하는 코드를 작성해 보세요.
* 입력<br>
Hello World!
* 출력<br>
HelloWorld!

```
rl.on('line', function (line) {
    input = line.split(' ');
}).on('close', function () {
    str1 = input[0];
    str2 = input[1];
    let str = str1+str2
    console.log(str.trim())
});
```

## 3. 		문자열 돌리기
문자열 str이 주어집니다. 문자열을 시계방향으로 90도 돌려서 아래 입출력 예와 같이 출력하는 코드를 작성해 보세요.
```
    str = input[0];
    let arr = [...str]
    for (let i=0;i<arr.length;i++){
        console.log(arr[i])
}
```
```
    str = input[0];
    for(let i of str){
        console.log(i)
    }
```
```
    str = input[0].split('');
    for (let i = 0; i < str.length; i += 1) {
        console.log(str[i]);
    }
```

## 4. 홀짝 구분하기
자연수 n이 입력으로 주어졌을 때 만약 n이 짝수이면 "n is even"을, 홀수이면 "n is odd"를 출력하는 코드를 작성해 보세요.
```
    num = Number(input[0]);
        if(num%2===0){
            console.log(`${num} is even`)
        } else {
		console.log(`${num} is odd`)
        }
```
```
    n = Number(input[0]);
    console.log(n%2===0? `${n} is even`:`${n} is odd`)

```

## 5. 문자열 겹쳐쓰기
문자열 my_string, overwrite_string과 정수 s가 주어집니다. 문자열 my_string의 인덱스 s부터 overwrite_string의 길이만큼을 문자열 overwrite_string으로 바꾼 문자열을 return 하는 solution 함수를 작성해 주세요.		
* my_string	: "He11oWor1d"
* overwrite_string:	"lloWorl"	
* s	: 2
* result : "HelloWorld"
* my_string에서 인덱스 2부터 overwrite_string의 길이만큼에 해당하는 부분은 "11oWor1"이고 이를 "lloWorl"로 바꾼 "HelloWorld"를 return 합니다.

```
function solution(my_string, overwrite_string, s) {
    let str = [...my_string]
    str.splice(s, overwrite_string.length, overwrite_string)
    return str.join("");
}
```
