---
title: "[JavaScript] 참조타입(Reference) - Array, Object의 개념"
excerpt: "참조 타입 중 Array와 object의 기본적인 개념에 대해 알아보자"

categories:
  - javascript
tags:
  - [javascript, 자바스크립트기초]

permalink: /categories/javascript/10

toc: true
toc_sticky: true

date: 2024-11-17
last_modified_at: 2024-11-17
---

## 🦥 본문

<br>
<br>

## typeof: 데이터 타입 확인

- `typeof`는 자바스크립트에서 **값의 데이터  자료형 타입을 반환**하는 연산자이다. 다양한 데이터 타입을 구분할 때 유용하게 사용된다.
- 사용법 : typeof 뒤에 표현식을 쓰면 자료형 타입으로 반환이 가능하다.

---

<br>

### typeof: 데이터 타입 확인 정리

| 데이터 타입                | 예시 코드               | `typeof` 반환 값        |
|---------------------------|------------------------|------------------------|
| 숫자 (Number)             | `typeof 42`            | `"number"`             |
| 문자열 (String)           | `typeof "Hello"`       | `"string"`             |
| 불리언 (Boolean)          | `typeof true`          | `"boolean"`            |
| 객체 (Object)             | `typeof { key: "value" }` | `"object"`         |
| 배열 (Array)              | `typeof [1, 2, 3]`     | `"object"`             |
| 함수 (Function)           | `typeof function() {}` | `"function"`           |
| 정의되지 않음 (Undefined) | `typeof undefined`     | `"undefined"`          |


---

<br>

### 예시 코드

```jsx
/* 변수 선언 */
let x = 10; // 숫자형
let xx = 10; // 숫자형
let y = "10"; // 문자형
let obj = { name: '홍길동' }; // 객체

/* 데이터 타입 비교 */
console.log(x, typeof x); // 10, "number"
console.log(y, typeof y); // "10", "string"
console.log(x == y); // true, 값만 비교 (10 == "10")
console.log(x === y); // false, 값과 타입 비교 (10 !== "10")
console.log(xx, typeof xx); // 10, "number"
console.log(x === xx); // true, 값과 타입 모두 동일
console.log(obj === xx); // false, 객체와 숫자 비교
console.log(obj, typeof y); // { name: '홍길동' }, "string"

```
<br>
<br>



