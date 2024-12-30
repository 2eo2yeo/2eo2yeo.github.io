---
title: "[JavaScript] console.clear 메서드"
excerpt: "콘솔에 기록된 메세지를 삭제하기"

categories:
  - javascript
tags:
  - [javascript, 자바스크립트]

permalink: /categories/javascript/32

toc: true
toc_sticky: true

date: 2024-12-30
last_modified_at: 2024-12-30
---

## 🦥 본문

<br>

### **`console.clear()` 메서드**

브라우저 개발자 도구(Console)에 기록된 모든 메시지를 삭제하는 메서드이다.

해당 메서드 사용 이전에 작성된 로그 메세지를 제거하여 **새로운 로그만을 확인하고 싶을 때 유용**

하다.

### **사용법**

```jsx
console.clear();

```

- **설명**: 호출 시 콘솔에 출력된 모든 로그를 즉시 삭제한다.
- **호출 결과**: 콘솔 창이 초기화된다.

---

### 활용 예제

```jsx
console.log("첫 번째 메시지");
console.log("두 번째 메시지");

console.clear(); // 콘솔 초기화
console.log("새로운 메시지"); // 출력 : '새로운 메시지' 

```

- '새로운 메시지' 만 화면상에 출력된다.
<br>
<br>



