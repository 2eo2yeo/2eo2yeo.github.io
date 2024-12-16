---
title: "[JavaScript] 제어문 - 반복문 do...while"
excerpt: "반복문 중 do...while문에 대해서 알아보자"

categories:
  - javascript
tags:
  - [javascript, 자바스크립트기초]

permalink: /categories/javascript/22

toc: true
toc_sticky: true

date: 2024-11-29
last_modified_at: 2024-11-29
---

## 🦥 본문

<br>


### **`do...while` 문 이란?**

- **`do...while` 문**은 **조건을 확인하기 전에 코드 블록을 최소 한 번 실행**하는 반복문이다. 즉, 코드가 **무조건 한 번은 실행된 후** 조건식을 평가한다.
- 조건이 참(`true`)이면 루프가 계속 반복되고, 거짓(`false`)이면 종료된다. 한번은 실행하여야 하는 작업에 적합하다.

---

### `do...while` 문법

```jsx
do {
    // 실행문: 조건과 상관없이 무조건 한 번 실행됨
} while (조건식);
```

- **설명**: `do` 블록 안의 실행문이 **최소 한 번 되는 코드 블록**,
- **`while (조건식)`**: 실행문이 다시 반복될지를 결정하는 조건식.

---


### 예제: 메뉴 선택 시스템

```jsx
let flag = false;
let menu = 1;

do {
    // 메뉴 안내 메시지 출력: 조건과 상관없이 한 번 실행
    console.log(`1 : 🍕 \t 2 : 🌭 \t 0 : 종료`);
    console.log(`[사용법] : 키보드 숫자로 입력해주세요.`);
} while (flag); // flag가 false이므로 루프는 한 번만 실행

// 메뉴 선택 처리
if (menu === 1) {
    console.log(`선택하신 메뉴는 🍕 입니다.`);
    flag = false; // 루프 종료
} else if (menu === 2) {
    console.log(`선택하신 메뉴는 🌭 입니다.`);
    flag = false; // 루프 종료
} else if (menu === 0) {
    console.log(`선택을 종료합니다.`);
    flag = false; // 루프 종료
}
```

- **설명**:
    - **조건문**: `if-else if` 문을 사용해 `menu` 값에 따라 메시지를 출력함.
    - **메뉴 선택**:
        - `menu === 1`: 피자 메뉴 선택 → `선택하신 메뉴는 🍕 입니다.` 출력
        - `menu === 2`: 핫도그 메뉴 선택 → `선택하신 메뉴는 🌭 입니다.` 출력
        - `menu === 0`: 종료 선택 → `선택을 종료합니다.` 출력
    - **flag 변수 설정 -**  각 조건이 실행된 후 `flag`를 `false`로 설정하여 루프 종료를 보장함.
<br>
<br>



