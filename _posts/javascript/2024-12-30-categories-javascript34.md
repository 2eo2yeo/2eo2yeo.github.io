---
title: "[JavaScript] DOM, getElementById(), onclick, 유효성검사"
excerpt: "HTML 태그에 접근해보자"

categories:
  - javascript
tags:
  - [javascript, 자바스크립트]

permalink: /categories/javascript/34

toc: true
toc_sticky: true

date: 2024-12-30
last_modified_at: 2024-12-30
---

## 🦥 본문

<br>

### DOM (Document Object Model)

: HTML 문서를 자바스크립트가 조작(핸들링)할 수 있도록 객체 구조로 변환한 것이다.

---

### 1. `getElementById()` 사용법

- **역할**: 주어진 문자열과 일치하는 [`id`](https://developer.mozilla.org/ko/docs/Web/API/Element/id) 속성을 가진 요소를 찾고, 이를 나타내는 [`Element`](https://developer.mozilla.org/en-US/docs/Web/API/Element) 객체를 반환한다.
    - id는 문서내에서 유일해야 함을 주의
    - **querySelector를 사용해도 됨(거의 동일한 기능)**
- **구문**: `document.getElementById("id값")`
- **예시**
    
    ```html
    <script>
    	let a = document.getElementById("number1").value; 
    						/* ID'number1' 요소의 값(value)을 가져옴 */
    </script>
    
    <body>						
    	<input type="text" id="number1">
    </body>
    ```
    
- **설명**: `id="number1"`인 입력 필드의 값을 가져와 변수 `a`에 저장.

---

### 2. `onclick` 사용법

- **역할**:  html에서 이벤트가 발생했을 때 자바스크립트 함수를 실행한다.
- **구문**: `<요소 onclick="함수이름()">`
- **예시**
    
    ```html
    <button type="button" onclick="dataInput('+')"> ➕ </button>
    ```
    
- **설명**: 버튼을 클릭하면 `dataInput('+')` 함수가 호출된다.

---

### 3. 유효성 검사

```jsx
function dataInput(op) {
    let a = document.getElementById("number1").value;
    let b = document.getElementById("number2").value;

    if (a === "") {
        alert("첫번째 숫자를 입력해주세요");
        document.getElementById("number1").focus(); // 커서 이동
    } else if (b === "") {
        alert("두번째 숫자를 입력해주세요");
        document.getElementById("number2").focus(); // 커서 이동
    } else {
        calculator(parseInt(a), parseInt(b), op); // 연산 수행
    }
}
```

 : 유효성 검사는 **입력값이 비어 있는지 확인**하고 잘못된 입력을 방지하는 과정이다.

- **예시**

```jsx
if (a === "") {
    alert("첫번째 숫자를 입력해주세요");
    document.getElementById("number1").focus(); 
																			// focus -> 커서 이동
} else if (b === "") {
    alert("두번째 숫자를 입력해주세요");
    document.getElementById("number2").focus();
} else {
    calculator(parseInt(a), parseInt(b), op); // 연산 수행
}
```

- 설명
    
    **if (a === "")**: 첫 번째 입력값이 비어 있으면 경고 메시지를 띄운다.
    
    **else if (b === "")**: 두 번째 입력값이 비어 있으면 경고 메시지를 띄운다.


<br>
<br>



