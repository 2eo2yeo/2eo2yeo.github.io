---
title: "[JavaScript] 내장함수(Built-in)와 사용자 지정함수"
excerpt: "주요 내장함수와 사용자 지정함수에 대해서 알아보자"

categories:
  - javascript
tags:
  - [javascript, 자바스크립트기초]

permalink: /categories/javascript/24

toc: true
toc_sticky: true

date: 2024-12-16
last_modified_at: 2024-12-16
---

## 🦥 본문

<br>

### **내장 함수 (Built-in Functions)**

JavaScript는 자주 사용하는 기능들을 미리 함수로 정의해 놓았으며, 

**내장 함수**는 선언 없이 바로 호출해 사용할 수 있다.

---

### **주요 내장 함수**

| 함수                | 설명                 | 예제                          |
|---------------------|----------------------|-------------------------------|
| `parseInt()`        | 문자열을 **정수**로 변환  | `parseInt("123abc") → 123`    |
| `parseFloat()`      | 문자열을 **실수**로 변환  | `parseFloat("123.45") → 123.45` |
| `Number()`          | 값을 **숫자형**으로 변환  | `Number("123") → 123`         |
| `String()`          | 값을 **문자열**로 변환  | `String(123) → "123"`         |
| `Math.random()`     | 0과 1 사이의 **난수** 생성 | `Math.random() → 0.5678`      |
| `Math.round()`      | 숫자를 **반올림**         | `Math.round(4.6) → 5`         |
| `Math.ceil()`       | 숫자를 **올림**           | `Math.ceil(4.1) → 5`          |
| `Math.floor()`      | 숫자를 **내림**           | `Math.floor(4.9) → 4`         |
| `Date()`            | **현재 날짜와 시간** 반환 | `new Date() → 현재 날짜와 시간` |

---

### **사용자 정의 함수**

- 내장 함수 외에도, 개발자가 원하는 작업을 수행하기 위해 **사용자 정의 함수**를 만들 수 있다.
- function 키워드를 이용하여 로직을 만드는 형태이다

```jsx
function add(x, y) {
    return x + y;
}
console.log(add(2, 3));  // 출력: 5

```

---

### **즉시 실행 함수 (IIFE)**

- **즉시 실행 함수**는 정의되자마자 바로 실행되는 함수이다.

```jsx
(function () {
    console.log("즉시 실행 함수입니다!");
})();
// 출력: 즉시 실행 함수입니다!

```

<br>
<br>



