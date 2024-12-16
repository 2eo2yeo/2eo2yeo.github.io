---
title: "[JavaScript] return - 함수에서 값 반환하기"
excerpt: "함수를 생성하고 다른 곳에서 사용할 수 있도록 값 반환"

categories:
  - javascript
tags:
  - [javascript, 자바스크립트기초]

permalink: /categories/javascript/27

toc: true
toc_sticky: true

date: 2024-12-16
last_modified_at: 2024-12-16
---

## 🦥 본문

<br>

### `return` 키워드란?

`return`은 함수가 작업을 끝낸 후 **결과 값을 반환하며 종료**할 때 사용하는 키워드다.

함수가 `return`을 만나면, 그 순간 실행을 멈추고 **값을 호출한 곳으로 반환**한다.

> 💡 return 키워드가 있어야 함수가 값을 돌려줄 수 있고, 이 값을 다른 곳에서 활용할 수 있다.
> 
> 
> . 예를 들어, 다른 변수에 저장하거나, 다른 함수의 인자로 활용하는 등이다.
> 

---

### 반환과 출력의 차이

| 구분   | 설명                                                                 |
|--------|----------------------------------------------------------------------|
| 출력   | `console.log()`는 단지 값을 **화면에 보여주는 용도**로 사용한다.      |
| 반환   | `return`은 값을 실제로 함수 외부로 반환하여, 다른 코드에서 **활용**하거나 **저장**할 수 있게 한다. |


---

### 코드 예제 1: 간단한 숫자 계산

```jsx
function add(a, b) {
    return parseInt(a) + parseInt(b); // 값을 반환하고 함수 종료
}

let result = add(1, 2); // 반환된 값 3이 result에 저장됨
console.log(`result = ${result}`); // 출력: result = 3

```

- 설명:
    - **`add` 함수 정의**: 두 숫자를 더한 값을 반환한다.
    - **`return` 사용**: 더한 값을 반환하며, 함수 실행이 종료된다.
    - **값 활용**: 반환된 값 `3`은 `result` 변수에 저장되어 이후 사용 가능하다.

---

### 코드 예제 2: 객체 생성 후 반환

```jsx
function createObject(name, age) {
    let obj = {
        name: name, // 키: name, 값: 파라미터 name
        age: age    // 키: age, 값: 파라미터 age
    };
    return obj; // 생성된 객체를 반환
}

let resultObj = createObject("홍길동", 30); // 함수 호출
console.log(resultObj);        // 출력: { name: "홍길동", age: 30 }
console.log(resultObj.name);   // 출력: 홍길동
console.log(resultObj.age);    // 출력: 30

```

- **설명**:
    - `creatObject` 함수는 객체 `obj`를 반환합니다. 반환된 객체의 주소값이 `resultObj`에 저장된다.
    - `creatObject` 은 호이스팅 되어 ( 자바스크립트가 함수 선언을 메모리에 미리 올려놓았기 때문에) 코드 내 어디서든 호출할 수 있다

<br>
<br>



