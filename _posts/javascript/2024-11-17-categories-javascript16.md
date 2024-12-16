---
title: "[JavaScript] 제어문 - 조건문 Switch"
excerpt: "조건문 Switch의 개념과 사용법에 대해서 알아보자"

categories:
  - javascript
tags:
  - [javascript, 자바스크립트기초]

permalink: /categories/javascript/16

toc: true
toc_sticky: true

date: 2024-11-17
last_modified_at: 2024-11-17
---

## 🦥 본문

<br>

- 조건식과 비교조건식이 일치하면 동작을 행한다

<br>

### **제어문 - 조건문: `switch` 문**

`switch` 문은 하나의 조건(숫자, 문자 등)에 따라 여러 경우(case) 중에서 하나를 선택해 실행할 때 사용한다. 각 `case`에 실행문을 정의하며, `break`를 사용해 `switch` 문을 종료시킨다. `default`는 **모든 경우에 해당되지 않을 때** 실행되는 코드 블록이다.

---

### **특징**

- 각 `case`가 끝날 때 **`break` 키워드**를 설치하여, 조건에 맞는 `case`가 나올 경우 `switch` 문을 빠져나와야 한다. `break`를 사용하지 않으면 다음 `case`가 모두 실행 된다.
- **`default`**: 모든 `case`와 일치하지 않을 때 실행되는 코드 블록. 선택 사항이지만, 모든 경우를 대비해 사용하는 것이 좋다.

---


### **구문**

```jsx
switch(조건식-숫자,문자 다 가능) {
    case 숫자, 문자 값1 (비교조건식):
            실행문;
            break;
    case 숫자, 문자 값2 (비교조건식) :
            실행문;
            break;
    case 반복~~~
    default : 
        실행문;

```

---


### **예제 1: 요일 선택**

```jsx
// 0: 월요일, 1: 화요일, 2: 수요일 
// 선택하는 숫자를 뒤의 요일로 출력하여라 
// 모두 해당안될 경우 사용법을 출력

let useage = `[0]월요일, [1]화요일, [2]수요일`;
let day = 1;  // 
let resultDay = undefined;

switch(day) {
    case 0:
        resultDay = "월요일"; break;
    case 1:
        resultDay = "화요일"; break;
    case 2:
        resultDay = "수요일"; break;
    default:
        console.log(`사용법: ${useage}`);
}
if (!(resultDay === undefined)) {
    console.log(`선택한 요일은 [${resultDay}] 입니다`);   //화요일이 출력됨
}
```

- **설명**: `day` 값에 따라 요일을 선택해 `resultDay`에 할당하고, 조건에 맞지 않으면 `default` 실행문이 작동한다.

---


### **예제 2: 짝수와 홀수 구분**

```jsx
// 임의의 숫자를 입력받아 짝수이면 빨간사과, 홀수이면 초록사과 출력
let number = 101;
let result = undefined;

switch (number % 2) {
    case 0:
        result = '🍎';  // 짝수일 경우
        break;
    case 1:
        result = '🍏';  // 홀수일 경우
        break;
    default:
        result = '해당 과일 없음';
}

console.log(result);
```

- **설명**: `number % 2` 연산 결과로 짝수(`0`)일 때는 빨간 사과, 홀수(`1`)일 때는 초록 사과가 출력된다.
- 위 코드 예시의 경우 if문을 쓰는 것이 더 낫다.  디폴트가 나올 확률이 없기 때문에 switch문을 쓰면 비효율적임

```jsx
/* if문으로 작성*/
let number = 100;
switch(number % 2) {
    case 0 :
        result = '🍎';
        break;
    case 1 :
        result = '🍏';
        break;
    default : 
        result = '해당 과일 없음';
}
console.log(result);
```

<br>
<br>



