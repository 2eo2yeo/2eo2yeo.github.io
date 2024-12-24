---
title: "[JavaScript] 화살표 함수 (Arrow)"
excerpt: "화살표 함수를 이용하여 간결하게 함수를 표현해보자"

categories:
  - javascript
tags:
  - [javascript, 자바스크립트기초]

permalink: /categories/javascript/29

toc: true
toc_sticky: true

date: 2024-12-24
last_modified_at: 2024-12-24
---

## 🦥 본문

<br>


일반 함수 표현식과 기능은 동일하나 좀 더 간결하게 표현하여 편리하게 사용이 가능하다.

### 형식

```jsx
// 일반 함수 표현식 
let function 함수명() {}

// 화살표 함수 표현식
let 함수명 = () => {}
```

---

### 예제1 - 화살표 함수 생성 및 일반 함수와의 비교

- 1+2 =3이 나오는 함수

```jsx
/* 일반 함수 정의 */

function add() {
    return 1+2; }

/* 일반 함수 표현식 */
let add2 = function () {
    return 1+2; }

/* 화살표 함수 표현식 */
let add3 = () => 1+2;

/* 함수 호출 */
console.log(add());  //  출력 : 3
console.log(add2());   //  출력 : 3
console.log(add3());   //  출력 : 3
```

- 실행문이 한줄일 경우 `{}` 중괄호와 return 키워드의 생략이 가능하다.

---

### 예제 2-1 ) 매개변수로 값을 받아 출력하는 화살표 함수 표현식

- 입력받은 숫자가 모두 0보다 크면 합을 구하는 로직

```jsx
let add5 = (a, b, c) => {
    if( a>0 && b>0 && c>0){
        console.log(a+b+c);
    }else{
        console.log(`${a}, ${b}, ${c} 는 0보다 커야함`);
    }
}

//함수 호출
add5(1,2,-3);    // 출력 :  1, 2, -3 는 0보다 커야함
```

- 세 개의 매개변수 `a`, `b`, `c`를 받아 조건에 따라 출력한다.
- 조건 :  모든 매개변수가 0보다 크면 (&& 연산자는 모든 조건이 true여야 실행) → a+b+c의 합을 출력, 그게 아니라면 ‘a,b,c는 0보다 커야함’ 이라는 메세지를 출력하라
- -3은 0보다 작으므로 else가 실행됨

---

### 예제 2-2 ) 매개변수로 값을 받아 출력하는 화살표 함수 표현식

- 값을 받아서 합산하고 출력하는 함수를 만들어라

```jsx
let add4 = (a, b) => a + b;

//함수 호출
console.log(add4(10, 20));   // 출력 : 30
```

- 두 개의 매개변수 `a`, `b`를 받아 그 합을 반환한다.

<br>
<br>



