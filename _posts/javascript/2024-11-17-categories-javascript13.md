---
title: "[JavaScript] 연산자 - (산술, 모듈러, 접합, 증감, 대입, 비교)"
excerpt: "연산자의 종류와 사용법에 대해 알아보자"

categories:
  - javascript
tags:
  - [javascript, 자바스크립트기초]

permalink: /categories/javascript/13

toc: true
toc_sticky: true

date: 2024-11-17
last_modified_at: 2024-11-17
---

## 🦥 본문

<br>
<br>

*제로초님 강의를 참고하였습니다.


## 논리 연산자


<br>

### AND 연산자 : `&&`

- **두 논리식이 모두 참일 때만** `true`를 반환한다.

| (논리식1) | 연산자 | (논리식2) | 결과값 |
|-----------|--------|-----------|--------|
| `true`    | `&&`   | `true`    | `true` |
| `true`    | `&&`   | `false`   | `false`|
| `false`   | `&&`   | `true`    | `false`|
| `false`   | `&&`   | `false`   | `false`|

<br>

### OR 연산자 : `||`

- **두 조건 중 하나라도 참이면** `true`를 반환한다.

| (논리식1) | 연산자 | (논리식2) | 결과값 |
|-----------|--------|-----------|--------|
| `true`    | `||`   | `true`    | `true` |
| `true`    | `||`   | `false`   | `true` |
| `false`   | `||`   | `true`    | `true` |
| `false`   | `||`   | `false`   | `false`|

<br>

### 부정 연산자

| 종류  | 설명                                              |
|-------|---------------------------------------------------|
| `!`   | 논리 부정 (`true` → `false`, `false` → `true`)    |
| `!!`  | 이중 부정 (Boolean 값으로 변환할 때 사용)         |

```jsx
let flag = true;
console.log(flag);   // true
console.log(!flag);  // false: 논리 부정 연산자
console.log(!!flag); // true: 이중 부정으로 다시 true
```

### boolean 값으로 변형시 false가 되는 값들

!! 이중부정 연산자를 사용하여 불리언 값으로 변형시 대부분의 값은 true가 되지만 false가 되는 값들이 있다.

1. **!!false**
2. **!! ' ' - 빈문자형**
3. **!! 0**
4. **!! NaN**

---
<br>
<br>

## 숏서킷 연산 (Short-Circuit Evaluation)

- **모든 프로그래밍 언어에 적용**된다.
- 특정 조건을 빨리 판단하기 위해 연산 순서를 최적화한다.

<br>

### AND 연산자 `&&`의 숏서킷

- **false가 앞에 있으면** 바로 `false`로 판단해 효율적이다. (둘다 조건을 충족해야함)

```jsx
let number = 11;
if ((number < 10) && (number > 0)) {
    // `false` 먼저 평가되면 전체가 `false`로 바로 판단
    console.log(`number는 사용 가능한 숫자[${number}]입니다.`);
} else {
    console.log(`number를 다시 입력해주세요.`);
}

```
<br>

### OR 연산자 `||`의 숏서킷

- **true가 앞에 있으면** 바로 `true`로 판단해 효율적이다. (하나만 충족해도 됨)

```jsx
let number2 = 11;
if ((number2 > 0) || (number2 < 0)) {
    // `true` 먼저 평가되면 전체가 `true`로 바로 판단
    console.log(`number2는 사용 가능한 숫자[${number2}]입니다.`);
} else {
    console.log(`number2를 다시 입력해주세요.`);
}

```

---

<br>

### 요약

- **AND 연산자 `&&`**: 둘 다 참일 때만 `true`. **false**가 앞에 있으면 빠르게 `false`로 판단.
- **OR 연산자 `||`**: 하나라도 참이면 `true`. **true**가 앞에 있으면 빠르게 `true`로 판단.
- **효율적 코드 작성**: 불필요한 연산을 줄이기 위해 **AND 연산자에서는 false를**, **OR 연산자에서는 true를** 먼저 배치하는 것이 좋다.

<br>
<br>



