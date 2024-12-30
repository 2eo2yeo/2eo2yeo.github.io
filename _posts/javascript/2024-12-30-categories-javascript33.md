---
title: "[JavaScript] DOM요소 접근법 - querySelector와 getElementById 차이"
excerpt: "querySelector와 getElementById의 차이에 대해서 알아보자"

categories:
  - javascript
tags:
  - [javascript, 자바스크립트]

permalink: /categories/javascript/33

toc: true
toc_sticky: true

date: 2024-12-30
last_modified_at: 2024-12-30
---

## 🦥 본문

<br>

두 메서드는 동일한 기능을 수행하나 약간의 차이가 있다.

### **`getElementById`와 `querySelector`의 차이**

- `getElementById`는 **ID 속성**을 기반으로 요소에 접근하는 방법이다.
    - 더 단순하지만 ID 외의 선택자를 사용할 수 없다.
    - 고정된 ID로 DOM에 접근할 경우 빠르고 효율적이다.
- `querySelector`는 **CSS 선택자**를 기반으로 요소에 접근하는 방법이다.
    - ID, 클래스, 태그 등 다양한 선택자로 접근할 수있어서 더 유연하다.
    - ID 외에도 클래스를 포함하거나 보다 세부적인 선택이 필요한 경우 사용한다

---

### 사용예시

- id=”number1” 이라는 input태그에 접근할 때

```jsx

document.getElementById("number1").value;
// id만 사용가능하므로 #선택자 사용x

document.querySelector("#number1"); 
```

<br>
<br>



