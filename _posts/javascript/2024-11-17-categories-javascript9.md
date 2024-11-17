---
title: "[JavaScript] 참조타입(Reference) - Array, Object의 개념"
excerpt: "참조 타입 중 Array와 object의 기본적인 개념에 대해 알아보자"

categories:
  - javascript
tags:
  - [javascript, 자바스크립트기초]

permalink: /categories/javascript/9

toc: true
toc_sticky: true

date: 2024-11-17
last_modified_at: 2024-11-17
---

## 🦥 본문

<br>
<br>


- 큰 데이터를 저장할 때 [], {} 사이에 담아서 활용한다. 이 괄호 사이 데이터들은 heap에 저장된다.

<br>

### Array `(배열: [ ])`

- **개념**: 여러 데이터를 콤마(,)로 구분하여 **`[]` 사이에 담는 데이터 구조**이다.
- **인덱스**: 배열 요소에 접근할 때 사용하는 **순서 번호**로, **0부터 시작**한다

```jsx
let numberList = [1, 2, 3, 4, 5];
console.log(numberList);     // [1, 2, 3, 4, 5] 출력
console.log(numberList[0]);  // 1이 출력
console.log(numberList[5]);  // Undefined 출력 (5번째 요소는 없음)
console.log(numberList[4]);  // 5가 출력

```

<br>

### 객체(object)  `{ }`

- **개념**: 데이터를 **키-값 쌍**으로 저장하는 데이터 구조.
- **구조**: `let obj = { 키: 값 };`
    - 객체는 속성(Property) 과 메서드(Method)로 구성된다.
- **개별 속성 호출 방법**:
    - **점 연산자 (`.`)**: `객체명.속성명`
    - **대괄호 연산자 (`[]`)**: `객체명["속성명"]` (속성명을 **문자열**로 작성)
- 배열과의 차이
    - 배열이 값만 나열되어 있는 것과 다르게 객체는 키와 값으로 이루어져 있다.

```jsx
let apple = "null";
apple = {
    name: 'apple',
    color: 'red',
    display: '🍎'
};

console.log(apple);    //모든 정보를 출력 apple, red , 🍎
console.log(apple.display);   //display 호출 // 출력 🍎
console.log(apple.color);   //color 호출 // 출력 red

console.log(apple["display"]);  //대괄호연산자 //출력 🍎
console.log(apple.color);  // 점 연산자   // 출력 red 

```

<br>
<br>



