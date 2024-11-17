---
title: "[JavaScript] 연산자 - (산술, 모듈러, 접합, 증감, 대입, 비교)"
excerpt: "연산자의 종류와 사용법에 대해 알아보자"

categories:
  - javascript
tags:
  - [javascript, 자바스크립트기초]

permalink: /categories/javascript/12

toc: true
toc_sticky: true

date: 2024-11-17
last_modified_at: 2024-11-17
---

## 🦥 본문

<br>
<br>

### 사칙연산자

- **`+`, `-` ,`*` , `/`, `%`, `**`**
- 기본적인 사칙연산을 위한 연산자이다

```jsx
console.log(3 + 5);  // 덧셈
console.log(3 - 5);  // 뺄셈
console.log(3 * 5);  // 곱셈
console.log(3 / 5);  // 나눗셈
console.log(3 % 5);  // 모듈러(나머지) 연산자
console.log(3 ** 5); // 거듭제곱
```

<br>

### 모듈러 연산자 `%`

- **나머지 값을 계산**하여 홀짝 여부 등을 판단할 때 사용된다.

```jsx

let a = 100;
console.log(a % 2); // a를 2로 나누어 짝수면 0, 홀수면 1이 출력됩니다.

```

<br>

### 접합연산자 `+`

- 숫자나 문자열을 **이어주는 역할**을 합니다.
- **문자열**로 시작하면 `+`는 **접합 연산자**로 작동합니다.

```jsx

console.log(10 + 20); // 30
console.log("sum : " + 10 + 20); // "sum : 1020"
console.log("sum : " + (10 + 20)); // "sum : 30" (괄호가 우선순위를 가짐)
console.log(`sum : ${10 + 20}`); // "sum : 30" 
                    //(템플릿 리터럴 사용 - 위의 코드보다 일반적)

```

<br>

### 증감연산자

| **연산자**   |  **설명**  |
| -------------| ----------|
| `++`         | 1씩 증가   |
| `--`         | 1씩 감소   |

```jsx
let a = 10;
console.log(++a); // 11: a를 먼저 1 증가시킴
console.log(a++); // 11: a를 출력한 후에 1 증가 (결과는 여기선 반영안됨)
console.log(a);   // 12

let b = 10;
console.log(--b); // 9: b를 먼저 1 감소시킴
console.log(b--); // 9: b를 출력한 후에 1 감소 (결과는 여기선 반영안됨)
console.log(b);   // 8

```

- 설명
    - **전위 연산자 `++a`**: 값을 **먼저 증가**시키고 반환합니다.
    - **후위 연산자 `a++`**: 값을 **먼저 반환**하고, 그 후에 증가합니다. 그래서 증가된 값은 **다음에 반영**됩니다.
- !!이중부정 연산자를 사용하여 불리언 값으로 변형시
대부분의 값은 true가 되지만 false가 되는 값들이 있다.

  1. !!false
  2. !! ' ' - 빈문자형
  3. !! 0
  4. !! Nan

<br>

### 대입연산자(=중첩연산자) `+=,` `-=` , `*=` , `/=` ..

- **변수에 값을 할당**하거나 **기존 값을 연산하여 재할당**할 때 사용됩니다

```jsx
let a = 0;
a += 2; // a = a + 2;  로 인식후 a에 다시 할당
a -= 2; // a = a - 2;  로 인식후 a에 다시 할당
a *= 2; // a = a * 2;  로 인식후 a에 다시 할당
a /= 2; // a = a / 2;  로 인식후 a에 다시 할당
a %= 2; // a = a % 2;  로 인식후 a에 다시 할당

```

<br>

### 비교 연산자  `>` , `<`, `>=`, `<=`, `!=` , `==`, `===`

- boolean 값을 반환한다.
- 주로 제어문 (if,  while…) 에서 사용한다.
- 원시타입 비교 예시

```jsx
console.log(3 > 2);   //true
console.log(3 < 2);    //false     
console.log(3 >= 3);   //3을 포함해서 같은지, true
console.log(3 <= 3);   //3을 포함해서 같은지, true
console.log(3 == '2'); // ''사이 숫자를 알아서 숫자로 바꿔서 비교함 // 3 == 2
console.log(3 == 'A'); // 아스키코드를 가져와서 // 3 == 67을 비교함
console.log(3 === '2'); // 데이터타입 비교 // num === str
console.log(3 === 'A'); // 데이터타입 비교 // num === str
```

- 원시타입 비교 코드 설명
    - **`==`**: 값만 비교 (타입은 무시)
    - **`===`**: 값과 **타입** 모두 비교 (엄격 비교)

- object 값 비교 예시

```jsx
// Object 비교
let obj1 = { name: "홍길동" };
let obj2 = { name: "홍길동" };
let obj3 = obj1; // obj3는 obj1을 참조

console.log(obj1); // 객체 obj1 출력
console.log(obj2); // 객체 obj2 출력
console.log(`obj1 : ${obj1}`); // 템플릿 리터럴로 obj1 출력
console.log(`obj2 : ${obj2}`); // 템플릿 리터럴로 obj2 출력

// 객체 비교
console.log(obj1 == obj2);  // false (서로 다른 객체, 참조 주소가 다름)
console.log(obj1 === obj2); // false (서로 다른 객체, 참조 주소가 다름)
console.log(typeof obj1 === typeof obj2); // true (둘 다 객체 타입)

// obj1과 obj3 비교
console.log(obj1 == obj3);  // true (obj3이 obj1을 참조하므로 같은 객체)
console.log(obj1 === obj3); // true (같은 객체, 참조 주소도 같음)
console.log(typeof obj1 === typeof obj3); // true (둘 다 객체 타입)

```

- **object 값 비교 코드 설명**:
    - **객체 비교**: 객체는 **참조 주소**를 비교합니다. 동일한 속성을 가지더라도 서로 다른 객체는 비교 시 `false`를 반환합니다.
    - **객체 참조**: `obj3 = obj1`처럼 객체를 참조하는 경우, 같은 주소를 가리키기 때문에 비교 시 `true`가 반환됩니다.
<br>
<br>



