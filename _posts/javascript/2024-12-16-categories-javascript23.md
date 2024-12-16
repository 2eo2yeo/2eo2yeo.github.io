---
title: "[JavaScript] 함수의 기초, 함수 정의 방법"
excerpt: "함수란? 함수 정의 방법"

categories:
  - javascript
tags:
  - [javascript, 자바스크립트기초]

permalink: /categories/javascript/23

toc: true
toc_sticky: true

date: 2024-12-16
last_modified_at: 2024-12-16
---

## 🦥 본문

<br>

### **함수 (Function)란?**

함수는 특정 작업들을 수행하는 코드의 블록이다. 이를 통해 코드를 재사용하고, 프로그램을 보다 효율적으로 관리할 수 있습니다. React와 같은 라이브러리에서는 주로 함수형 프로그래밍을 기반으로 하여, 함수의 역할이 더욱 중요하다.

<br>

### **구문**

```jsx
function 함수명(매개변수1, 매개변수2, ...) {실행로직}
```

- 함수 이름은 **camelCase** 표기법을 사용하며, 변수 이름 정의와 같은 규칙을 따른다.

---

<br>

### **함수 정의 방법**

1. **함수 선언식**
    - `function` 키워드를 사용하여 독립적으로 함수를 선언한다.
    - **함수 이름**만으로 호출할 수 있다. 함수 이름 뒤에 소괄호 `()`를 붙여 실행한다.
    - 함수 선언식으로 정의된 함수는 **호이스팅(hoisting)** 되어 코드의 어느 위치에서든 호출할 수 있다.

**→ 함수 선언식 예시**

```jsx
gugudan(); //함수 호출 가능

function gugudan() {
    console.log("3 * 1 = 3");
    console.log("3 * 2 = 6");
    console.log("3 * 3 = 9");
    console.log("3 * 4 = 12");
}
```

1.  **함수 표현식**
- 함수를 변수에 할당하는 방식으로 정의한다. 주로 `const`를 사용해 **중복 선언을 방지**한다.
- **변수 이름**으로 호출할 수 있다.
- 함수 표현식은 **호이스팅되지 않으므로**, 함수 선언 이후에만 호출할 수 있다

**→ 함수 표현식 예시**

```jsx
const gugudan = function() {
    console.log("3 * 1 = 3");
    console.log("3 * 2 = 6");
    console.log("3 * 3 = 9");
    console.log("3 * 4 = 12");
};
gugudan(); //함수 호출

```

---
<br>
<br>



