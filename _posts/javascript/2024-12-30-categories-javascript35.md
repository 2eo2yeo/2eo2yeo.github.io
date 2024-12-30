---
title: "[JavaScript] 간단한 계산기 기능 구현 (HTML, 자바스크립트 사용)"
excerpt: "HTML, 자바스크립트로 간단한 계산기 기능을 구현해보자"

categories:
  - javascript
tags:
  - [javascript, 자바스크립트]

permalink: /categories/javascript/35

toc: true
toc_sticky: true

date: 2024-12-30
last_modified_at: 2024-12-30
---

## 🦥 본문

<br>
HTML과 JavaScript를 사용하여 기본적인 계산기 기능을 구현한 예제이다. 
입력값을 받아 실행할 연산에 해당한 버튼을 누르면 간단한 사칙연산(+,-,*,/,%) 과 유효성 검사를 수행하며, 콘솔에 결과를 출력할 수 있게 하도록 하겠다.

## HTML 파일 구조

### `<script>~</script>` 부분

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculator</title>
	    <!-- 1. 자바스크립트 파일 불러오기 --> 
    <script src="2_calculator.js"></script>
    <script>
			    //2. 데이터 입력시 유효성 체크 진행
        function dataInput(op) {
            let a = document.querySelector("#number1"); //첫번째 숫자
            let b = document.querySelector("#number2"); //두번째 숫자
            
            if(a.value === ""){
                alert("첫번째 숫자를 입력해주세요");
                a.focus();
            } else if(b.value === "") {
                alert("두번째 숫자를 입력해주세요");
                b.focus();
            } else { //계산 함수 호출
                calculator(parseInt(a.value), parseInt(b.value), op);
            }

        }
    </script>
</head>
... 
```

1. "2_calculator.js"라는 이름의 외부 자바스크립트 파일을 전역 스코프에 불러온다.
2. dataInput 힘수는 `op`라는 하나의 매개변수를 받는다 이는 아래의 button 클릭시에 연산자가 전달되어 넘어오는 값이다. 이 `op`값은 다시 `calculator` 함수로 전달된다.
3. 유효성 체크와 데이터처리 코드를 html 파일 내부에 script 태그를 이용하여  삽입함
    - **queryselector로 DOM요소 접근**
        - `#number1`과 `#number2`로 입력 필드 값에 접근한 값을 각각 변수 a, b에 할당하여 코드의 간결성을 높인다.
    - **유효성 검사 (if문)**
        - 첫번째와 두번째 숫자가 입력되지 않은 경우 `alert`로 메시지를 출력하고, 해당 필드에 포커스를 준다.
        - 위의 입력값이 모두 유효한 경우 `calculator` 함수를 호출하고 숫자 값과 연산자(op)**를 전달한다.
        - parseInt를 사용하여 정수로 바꿔준 데이터를 보낸다.

---

### 화면 출력, 버튼 클릭 부분

```html
<body>
    <h1>계산기</h1>
    <form action="#">
        <ul>
            <li>
		           
                <label for="">number1</label>
                <input type="text" id="number1">  <!-- 첫 번째 숫자 입력 필드 -->
            </li>
            <li>
                <label for="">number2</label>
                <input type="text" id="number2"> <!-- 두 번째 숫자 입력 필드 -->
            </li>
            <li>
		             <!-- 각 버튼 클릭 시 특정 연산자를 전달 -->
                <button type="button" onclick="dataInput('+')"> ➕ </button>
                <button type="button" onclick="dataInput('-')"> ➖ </button>
                <button type="button" onclick="dataInput('*')"> ✖ </button>
                <button type="button" onclick="dataInput('/')"> ➗ </button>
                <button type="button" onclick="dataInput('%')"> % </button>
            </li>
        </ul>
        <div>
            <span>실행결과 : </span>
            <span></span>
        </div>
    </form>
</body>
</html>
```

- 버튼을 클릭하면 **onclick 속성**에 정의된 함수가 실행되며, 해당 버튼의 연산자를 `op`로 전달한다.
- 각 버튼은 연산자(`+`, `-`, `*`, `/`, `%`)를 html 파일 내의 `dataInput` 함수에 op라는 매개변수로 전달한다. 최종적으로는 `calculator` 함수로 넘겨진다.

---


## 자바스크립트 파일 구조 "2_calculator.js”

### 계산 로직 구현

```jsx
function calculator(a, b, op) {
    a = parseInt(a); // 넘어온 a를 정수로 변환
    b = parseInt(b); // 넘어온 b를 정수로 변환
    
    switch(op) {
        case '+' : console.log(a + b); break;
        case '-' : console.log(a - b); break;
        case '*' : console.log(a * b); break;
        case '/' : console.log(a / b); break;
        case '%' : console.log(a % b); break;
        default : console.log('처리할 수 없는 연산자 입니다.');        
    }
}
```

- 파라미터 a, b로 input에 입력된 두개의 숫자를 받고 op는 클릭한 연산자 값을 받음
- switch문을 사용해서 op값을 확인하고 해당하는 연산을 수행한다
    - `op`가 `'+'`인 경우 `a + b`를 계산.
    - `op`가 `'*'`인 경우 `a * b`를 계산.
- 연산 결과를 `console.log`를 통해 출력한다.

<br>
<br>



