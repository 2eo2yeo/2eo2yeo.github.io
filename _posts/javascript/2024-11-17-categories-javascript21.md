---
title: "[JavaScript] 제어문 - 반복문 while"
excerpt: "반복문 중  while문에 대해서 알아보자"

categories:
  - javascript
tags:
  - [javascript, 자바스크립트기초]

permalink: /categories/javascript/21

toc: true
toc_sticky: true

date: 2024-11-29
last_modified_at: 2024-11-29
---

## 🦥 본문

<br>


### **`while` 문**

- `while` 문은 **조건식이 `true`일 동안** 코드를 계속 반복해서 실행하는 반복문이다. **종료 조건**을 명확히 설정하지 않으면 무한 루프에 빠질 수 있기 때문에, 반복문 내에서 조건이 `false`가 될 수 있도록 제어해 주어야 한다.
- `while`문은 **종료 시점을 알 수 없는 반복 작업**에 적합하다.

---
<br>


### **`while` 문 문법**

```jsx
while (조건식) {
    실행문;
}
```

- **조건식**: 반복을 계속할지 멈출지를 결정한다. 조건이 `true`이면 실행문이 반복되고, `false`가 되면 반복이 종료된다.

---
<br>

### **예제 1: `for` 문과 `while` 문 비교 (결과 동일)**

1. **`for` 문 사용**:
    
    ```jsx
    for (let i = 1; i <= 5; i++) {
        if (i === 3) break;  // `i`가 3일 때 반복문 종료
        console.log(`i = ${i}`);
    }
    ```
    
    - **출력 결과**: `i = 1`, `i = 2`
    - **설명**: `i`가 3이 되면 `break` 문이 실행되어 반복문이 종료된다.
    
2. **`while` 문 사용**:
    
    ```jsx
    let count = 1;
    while (count <= 5) {
        if (count === 3) break;  // `count`가 3일 때 반복문 종료
        console.log(`count = ${count}`);
        count++;  // `count`를 1씩 증가시켜 조건 변경
    }
    ```
    
    - **출력 결과**: `count = 1`, `count = 2`
    - **설명**: `count`가 3이 되면 `break` 문이 실행되어 `while` 문이 종료된다. 여기서 `count++`는 `count`를 1씩 증가시키는 역할을 한다.

---
<br>

### **예제 2: 메뉴 선택 프로그램**

```jsx
let flag = true;
let menu = 0;

while (flag) {
    console.log(`1: 🍕 \t 2: 🌭 \t 0: 종료`);
    if (menu === 1) {
        console.log(`선택하신 메뉴는 🍕 입니다.`);
        flag = false;  // 반복 종료
    } else if (menu === 2) {
        console.log(`선택하신 메뉴는 🌭 입니다.`);
        flag = false;  // 반복 종료
    } else if (menu === 0) {
        console.log(`선택을 종료합니다`);
        flag = false;  // 반복 종료
    }
}
```

- **설명**:
    - `flag` 변수는 반복을 제어하는 **논리 플래그**로, `true`일 동안 `while` 문이 실행된다. `flag` 같은 변수를 사용해 반복을 유동적으로 제어할 수 있다.
    - 메뉴가 선택되면 `flag`를 `false`로 설정하여 **반복문을 종료**한다.

<br>
<br>



