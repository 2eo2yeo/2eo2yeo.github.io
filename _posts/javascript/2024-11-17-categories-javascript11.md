---
title: "[JavaScript] 표현식(Expression)과 문(Statement)"
excerpt: "표현식과, 문의 차이에 대해서 알아보자"

categories:
  - javascript
tags:
  - [javascript, 자바스크립트기초]

permalink: /categories/javascript/11

toc: true
toc_sticky: true

date: 2024-11-17
last_modified_at: 2024-11-17
---

## 🦥 본문

<br>
<br>

### 1. 선언문 (Statement)

선언문은 **변수를 선언하거나** 특정 동작을 수행하는 구문이다. 값이 반환되지 않고, 주로 변수나 구조를 정의하는 데 사용된다.

```jsx
let a;  // 선언문 (변수 a를 선언하고 끝냄)
let b = 100;  // 표현식 (변수 b를 선언하고 100을 할당)
let c = undefined;  // 선언문 (내용이 정해지지 않아서 비워놓겠다)
let d = null;  // 선언문 (일부러 비워놓는다고 선언)

```

---


<br>

### 2. 표현식 (Expression)

표현식은 값을 생성하거나 반환하는 코드로, **계산된 결과가 값으로 평가**된다. 이를 통해 자바스크립트는 계산된 값을 제공하거나 특정 값을 할당한다.

```jsx
1; // 숫자 리터럴 표현식 (숫자 값 1을 생성)
'hong'; // 문자 리터럴 표현식 (문자열 'hong'을 생성)
1 + 1; // 산술 연산 표현식 (1과 1을 더한 결과 2를 반환)
함수명(); // 함수 호출 표현식 (함수를 실행하고 그 결과 값을 반환)
c = 100; // 할당 표현식 (변수 c에 100을 할당)

```

- **설명**: 표현식은 값으로 평가되며, 계산된 결과가 반환된다. 예를 들어, `1 + 1`은 `2`로 평가된다.
- **리터럴** : 값 자체를 나타내는 표현

<br>
<br>



