---
title: "[JavaScript] break문으로 반복문 제어"
excerpt: "break를 사용하여 반복문에서 빠져나오기"

categories:
  - javascript
tags:
  - [javascript, 자바스크립트기초]

permalink: /categories/javascript/20

toc: true
toc_sticky: true

date: 2024-11-29
last_modified_at: 2024-11-29
---

## 🦥 본문

<br>


### `break` 이란?

- **`break` 문**은 switch 문이나, 반복문(예: `for`, `while`, `do...while`)에서 **즉시 루프를 종료**하는 데 사용된다
- 조건이 만족되면, 루프의 나머지 부분을 실행하지 않고 바로 반복문을 빠져나온다.

---

<br>

### 예제: `for` 문에서 `break` 사용

```jsx
for (let i = 1; i <= 6; i++) {
    if (i === 3) {
        break; // `i`가 3일 때 루프를 즉시 종료
    }
    console.log(`i = ${i}`);
}
```

- **설명**:
    - `i`는 1부터 6까지 증가하며 루프가 실행된다.
    - `if (i === 3)`: `i`가 3일 때 조건이 참이 되며, `break`가 실행된다.
    - **`break`** : 루프를 즉시 종료하고, 이후의 반복은 실행되지 않는다.
- **출력 결과**: `1`과 `2`만 출력되고 `i`가 3일 때 루프가 종료된다.

<br>
<br>



