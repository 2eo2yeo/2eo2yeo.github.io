---
title: "[JavaScript] 간단한 계산 로직 만들기 (합계, 최솟값)"
excerpt: "더하기, 최솟값 구하는 간단한 함수를 만들어보자"

categories:
  - javascript
tags:
  - [javascript, 자바스크립트기초]

permalink: /categories/javascript/25

toc: true
toc_sticky: true

date: 2024-12-16
last_modified_at: 2024-12-16
---

## 🦥 본문

<br>

### 1. 두 숫자의 합계를 출력하는 기본 로직

**기능:** 두 개의 숫자를 변수에 직접 할당하고 합계를 출력한다.

```jsx
// 두 숫자의 합계를 계산
let num1 = 10;  // 첫 번째 숫자
let num2 = 20;  // 두 번째 숫자
console.log(`sum ==> ${num1 + num2}`); // 출력: sum ==> 30

```
<br>

---


### 2. `add`함수 (합계)

 **기능** : 두 숫자를 매개변수로 받아 합계를 출력한다. 매개변수는 문자열이든 숫자이든 상관없으며, 내부에서 `parseInt()`를 사용해 숫자로 변환하여 계산한다.

- **함수 정의**

```jsx
function add(a, b) {
    let n1 = parseInt(a); // 첫 번째 숫자를 정수로 변환
    let n2 = parseInt(b); // 두 번째 숫자를 정수로 변환
    console.log(`sum ==> ${n1 + n2}`); // 두 숫자의 합계를 출력
}
```

- **사용 예제 (출력)**

```jsx
add(10, 20);         // 출력: sum ==> 30 (숫자 입력)
add('10232', '2232'); // 출력: sum ==> 12464 (문자열 입력)
add(100, '300');      // 출력: sum ==> 400 (혼합 입력)
```


<br>

---



### 3. `min` 함수 (최솟값 - 음수가 되지 않는 조건)

**기능:** 두 숫자의 차를 계산하되, 결과가 음수가 되지 않도록 제한합니다. `a`가 `b`보다 작을 경우 오류 메시지를 출력합니다.

- **함수 정의:**

```jsx
function min(a, b) {
    a = parseInt(a); // 첫 번째 숫자를 정수로 변환
    b = parseInt(b); // 두 번째 숫자를 정수로 변환

    if (a >= b) {
        console.log(`sum ==> ${a - b}`); // a가 b보다 크거나 같으면 차이를 출력
    } else {
        console.log(`a값은 b보다 커야 합니다.`); // 그렇지 않으면 오류 메시지 출력
    }
}
```

- **사용 예제(출력)**

```jsx
min(100, 20);         // 출력: sum ==> 80
min('100', '20');     // 출력: sum ==> 80 (문자열 입력)
min(10, 20);          // 출력: a값은 b보다 커야 합니다.
min('10', 'abc');     // 출력: a값은 b보다 커야 합니다. (abc는 NaN이 되어 비교 실패)

```
<br>
<br>



