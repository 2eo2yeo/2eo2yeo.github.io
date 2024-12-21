---
title: "[JavaScript] for문 예제2 - 구구단, 프루츠타워 매개변수 활용하여 원하는 만큼 출력하기"
excerpt: "구구단 한단, 원하는 단만 지정, 프루츠타워 삼각형 모양으로 원하는 층만큼 출력해보자"

categories:
  - javascript
tags:
  - [javascript, 자바스크립트기초]

permalink: /categories/javascript/28

toc: true
toc_sticky: true

date: 2024-12-21
last_modified_at: 2024-12-21
---

## 🦥 본문

<br>

### 구구단 원하는 단만 출력

```jsx
function singleGugudan(dan) {
    for(let row=1; row<=9; row++) {
        console.log(`${dan} ✖ ${row} = ${dan * row}`);
    }
}

//구구단 3단 출력
singleGugudan(3);  
```

- 해당 함수는 dan 이라는 매개변수를 받는다. dan은 출력하려는 구구단의 단(숫자) 이다.
- for반복문 → row 초기값 1부터 시작하여 9단까지 증가시킨다.
- 각 반복에서 row는 곱해지는 숫자이다.
- `console.log`는 현재 실행 중인 `dan`과 `row`의 곱셈 결과를 텍스트로 출력한다.
- 템플릿 리터럴(```)을 사용해 동적인 문자열로 나타낸다.
- 출력결과

```jsx
//출력 결과 

3 ✖ 1 = 3
3 ✖ 2 = 6
3 ✖ 3 = 9
...
3 ✖ 9 = 27
```

---

### 구구단  시작 ~ 끝나는 단 선택하여 출력

```jsx
function selectGugudan(start, end) {
    for(let row=1; row<=9; row++) {
        let output = '';
        for(let col=start; col<=end; col++) {
            output += `${col} ✖ ${row} = ${row * col}\t`;
        }
        console.log(output);
    }
}

//구구단 7~9단 출력
selectGugudan(7,9);
```

- 해당 함수는 두개의 매개변수를 받는다.
    - start : 출력 시작 단, end : 출력 끝 단
- `for(let row=1; row<=9; row++){}`
    - 바깥 for문
    - row는 1부터 시작하여 1~9까지 반복되며 곱해지는 수이다.
- `let output = '';`
    - 빈문자열로 초기화 (문자열 데이터를 누적하여 결과를 만들기 위함)
- `for(let col=start; col<=end; col++) {...}`
    - col의 기초값은 start이고, start부터 end까지 반복한다.
- `{ output += ${col} ✖ ${row} = ${row * col}\t;}`
    - 안쪽  for문의 결과를 문자열로 만들어서 output 에 추가한다
    - `output` 에는 `row`에 대해 `start` 단부터 `end` 단까지의 계산 결과가 포함된다.
- `console.log(output);`
    - 각 줄(`row`)마다 누적된 계산 결과를 한줄씩 출력하기 위해서 바깥 for문 끝에 log를 찍음
- 출력결과

```jsx
7 ✖ 1 = 7    8 ✖ 1 = 8    9 ✖ 1 = 9    
7 ✖ 2 = 14   8 ✖ 2 = 16   9 ✖ 2 = 18   
7 ✖ 3 = 21   8 ✖ 3 = 24   9 ✖ 3 = 27   
7 ✖ 4 = 28   8 ✖ 4 = 32   9 ✖ 4 = 36   
7 ✖ 5 = 35   8 ✖ 5 = 40   9 ✖ 5 = 45   
7 ✖ 6 = 42   8 ✖ 6 = 48   9 ✖ 6 = 54   
7 ✖ 7 = 49   8 ✖ 7 = 56   9 ✖ 7 = 63   
7 ✖ 8 = 56   8 ✖ 8 = 64   9 ✖ 8 = 72   
7 ✖ 9 = 63   8 ✖ 9 = 72   9 ✖ 9 = 81   

```

---

### 프루츠 타워 삼각형 모양으로 출력

```jsx
export function fruitsTower(emoji, floor) {
    for(let row=1; row<=floor; row++) {
        let output = '';
        for(let col=1; col<=row; col++) {
            output += emoji;
        }
        console.log(output);
    }
}

//오렌지 이모지로 10층 탑 쌓기
fruitsTower('🍊', 10);
```

- fruitsTower 함수는 두개의 매개 변수를 받는다
    - `emoji`: 출력할 이모지 , `floor`: 탑의 층 수.
- `for(let row=1; row<=floor; row++) {...}` - 바깥for문
    - row는 몇 번째 층을 출력하는지 나타낸다.
    - row는 1부터 시작하여 floor 까지 증가한다.
    - `row`에 대해 출력되는 이모지의 개수는 현재 층 번호와 동일하다.
- `let output = '';`
    - output을 문자열로 초기화
- `for(let col=1; col<=row; col++) {...}` - 안쪽 for문
    - col은 현재 층에서 출력될 이모지의 갯수이다.
    - 
- `output += emoji;`
    - `output` 문자열에 `emoji`를 누적하여 출력하겠다.
- `console.log(output);`
    - `output` 문자열에는 `emoji`가 누적되어 있으며, 각 층마다 완성된 문자열을 콘솔에 출력한다.
- 출력 결과

```jsx
🍊
🍊🍊
🍊🍊🍊
🍊🍊🍊🍊
🍊🍊🍊🍊🍊
🍊🍊🍊🍊🍊🍊
🍊🍊🍊🍊🍊🍊🍊
🍊🍊🍊🍊🍊🍊🍊🍊
🍊🍊🍊🍊🍊🍊🍊🍊🍊
🍊🍊🍊🍊🍊🍊🍊🍊🍊🍊
```
<br>
<br>



