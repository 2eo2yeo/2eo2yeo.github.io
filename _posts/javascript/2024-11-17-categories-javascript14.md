---
title: "[JavaScript] 삼항연산자"
excerpt: "삼항연산자의 정의와 사용법"

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


### **삼항 연산자란?**

삼항 연산자는 **조건에 따라 값을 선택**할 때 사용하는 **짧고 간단한 조건문**이다. `if-else`문을 간단하게 대체할 수 있으며, **한 줄로 표현**할 수 있기 때문에 코드가 더 깔끔해진다. react에서 많이 사용된다.**복잡한 조건**에서는 가독성이 떨어질 수 있으므로, 단순한 조건에서 사용하는 것이 좋다.

---

<br>

### **구문**

```jsx
(조건식) ? 참일 때의 값 : 거짓일 때의 값;
```

- **조건식**: 평가되는 식으로, `true` 또는 `false`를 반환한다,  식이 끝나면 `?`를 붙임
- **참일 때의 값**: 조건식이 `true`일 경우 실행되거나 반환되는 값, 끝나는 부분에 `:` 를 붙임
- **거짓일 때의 값**: 조건식이 `false`일 경우 실행되거나 반환되는 값. 끝나는 부분에`;`를 붙임

---

<br>

### **특징**

- 삼항 연산자는 **문이 아닌 식**이다. 따라서 **바로 값을 변수에 할당하거나 반환이 가능**
- `if` 문과 달리, 삼항 연산자는 값 자체를 반환하기 때문에 **변수에 할당하거나 함수의 인자로 사용**하기에 효율적이다.

---

<br>

### **예제**

1. **단순한 삼항 연산자 사용**
    
    ```jsx
    let fruit = "apple";
    (fruit === "apple") ? console.log('🍎') : console.log(fruit);
    ```
    
    - `fruit`가 `"apple"`일 경우, `🍎`를 출력하고, 그렇지 않으면 `fruit` 값을 출력한다.
2. **값을 변수에 저장하기**
    
    ```jsx
    let display = (fruit === "apple") ? '🍎' : fruit;
    console.log(display);  // '🍎' 또는 fruit 값 출력
    
    ```
    
    - 삼항 연산자의 결과를 `display`에 저장해두고, 나중에 사용하거나 출력할 수 있다.

---

<br>

### if문을 삼항연산자로 변형 하기

- **삼항 연산자**: 한 줄로 값을 반환하며, 변수에 바로 할당 가능.
- **if 문**: 여러 줄로 작성할 수 있고, 별도의 출력이나 동작을 설정할 수 있다.

```jsx
//if문으로 작성 
let fruit = "apple";
if (fruit === "apple") {
    console.log('🍎');
} else {
    console.log(fruit);
}

// 위 코드를 삼항연산자로 작성
(fruit === "apple") ? console.log('🍎') : console.log(fruit);

```

<br>
<br>



