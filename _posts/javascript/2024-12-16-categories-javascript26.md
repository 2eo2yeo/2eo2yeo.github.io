---
title: "[JavaScript] 함수의 매개변수와 인자"
excerpt: "함수의 매개변수와 인자에 대해서 알아보자"

categories:
  - javascript
tags:
  - [javascript, 자바스크립트기초]

permalink: /categories/javascript/26

toc: true
toc_sticky: true

date: 2024-12-16
last_modified_at: 2024-12-16
---

## 🦥 본문

<br>
### **매개변수(**Parameter, 파라미터)

- 함수가 호출 될 때 값을 받을  자리 표시자.
- 함수 정의 시 괄호 안에 작성되며, 함수가 어떤 값을 받을지 미리 약속하는 개념 (자리 표시를 해주는 개념)
- 예: `function add(a, b)`에서 `a`와 `b`가 파라미터이다..
    
---

### **인자 (**Argument)

- 함수를 호출할 때 **실제로 전달되는 값**
- 매개변수에 값 전달 시에 배열, 객체 어떤 것으로 전달해도 상관없다.
- 파라미터에 **순서대로 매핑**되어 함수 안에서 사용된다.
- 인수는 함수의 매개변수에 대응되는 값으로 **함수 실행 시 매개변수로 전달된다.**
- 예: `add(5, 200)`에서 `5`와 `200`이 인자이다.

---

### 매개변수와 인자 예시

```jsx
function add(a, b) {
    return a + b;
}

let sum = add(5, 200); // 5와 200이 각각 a와 b에 매핑
console.log(`sum = ${sum}`); // 출력: sum = 205
```

---

### 파라미터와 인자의 매핑

1. 인자는 함수 정의에 있는 파라미터의 순서에 맞게 매핑되기 때문에 **자리 순서가 중요하다.**
    
    ```jsx
    function add(a, b) {
        return a + b;
    }
    
    let sum = add(5, 200); // 5와 200이 각각 a와 b에 매핑
    console.log(`sum = ${sum}`); // 출력: sum = 205
    ```
    
    ex.  `a`  ⇒`5`   와 `b`  ⇒ `200` 으로 매핑 해야 함수가 올바르게 작동한다.
    

1. 함수 호출 시, **정의된 형태에 맞는 형식(타입과 개수)의 인수**를 전달해야한다.
    
    ```jsx
    // 올바른 사용
    function add(a, b) { // 두 개의 매개변수 정의
        console.log(a + b);
    }
    
    add(10, 20); // 출력: 30 (숫자 두 개 전달)
    
    //잘못된 사용
    function add(a, b) {
        console.log(a + b);
    }
    
    add(10);       // NaN (b가 undefined로 계산됨)
    add('10', 20); // "1020" (문자열과 숫자가 더해짐)
    
    ```
    
    - 올바른 사용 : 매개변수와 인수의 개수와 타입이 일치
    - 잘못된 사용: 매개변수와 인수의 개수 또는 타입이 일치하지 않으면 의도하지 않은 결과가 발생할 수 있다.


<br>
<br>



