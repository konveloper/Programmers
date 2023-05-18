# 코딩테스트 연습 > 코딩 기초 트레이닝 > Day 1
## 1. 문자열 출력하기
문자열 str이 주어질 때, str을 출력하는 코드를 작성해 보세요.
str에는 공백이 없으며, 첫째 줄에 한 줄로만 주어집니다.
```
str = input[0].trim();
```

## 2. a와 b 출력하기
정수 a와 b가 주어집니다. 각 수를 입력받아 입출력 예와 같은 형식으로 출력하는 코드를 작성해 보세요.
* 입력 <br>
4 5
* 출력<br>
a = 4<br>
b = 5
```
rl.on('line', function (line) {
    input = line.split(' ');
}).on('close', function () {
    console.log("a = " + Number(input[0]));
        console.log("b = " + Number(input[1]));
});
```

## 3. 문자열 반복해서 출력하기
문자열 str과 정수 n이 주어집니다.
str이 n번 반복된 문자열을 만들어 출력하는 코드를 작성해 보세요.
```
rl.on('line', function (line) {
    input = line.split(' ');
}).on('close', function () {
    str = input[0];
    n = Number(input[1]);
    console.log(str.repeat(n));
});
```

## 4. 대소문자 바꿔서 출력하기
영어 알파벳으로 이루어진 문자열 str이 주어집니다. 각 알파벳을 대문자는 소문자로 소문자는 대문자로 변환해서 출력하는 코드를 작성해 보세요.
```
rl.on('line', function (line) {
    input = [line];
}).on('close',function(){
    str = input[0];
    let answer = ''
    for(let i of str) {
        if(str[i].toUpperCase()===str[i]){
            answer += str[i].toLowerCase()
        } else {
            answer += str[i].toUpperCase()
        }
    }
    console.log(answer)
});
```
str 길이만큼 반복문을 돌렸을 때 str의 i번째 글자가 대문자라면 소문자로 소문자라면 대문자로

## 5.다음과 같이 출력하도록 코드를 작성해 주세요.
`!@#$%^&*(\'"<>?:;`
```    
console.log('!@#$%^&*(\\\'"<>?:;')
```
특수문자는 \나 백틱(`)을 사용해서 처리해줘야 하는데 이스케이프 처리라고 한다. \를 사용하는 방법은 특수문자 앞에 \를 넣어주면 된다.
