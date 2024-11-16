---
title: "[JavaScript] 원시타입 - undefined, null"
excerpt: "원시타입 종류 중 숫자형, 논리형에 대해 알아보자"

categories:
  - javascript
tags:
  - [javascript, 자바스크립트기초]

permalink: /categories/javascript/8

toc: true
toc_sticky: true

date: 2024-11-16
last_modified_at: 2024-11-16
---

## 🦥 본문

<br>
<br>

> `var`, `let`, `const`와 같은 키워드로 변수 선언하게 되면
> 

자바스크립트는 메모리에 변수공간을 생성한다. 

이 변수 공간은 비워져있지 않음.

<br>

### undefined (디폴트 값)

- 값을 할당하지 않은 경우에도 undefined라는 값을 자동으로 할당함

```jsx
let num; 
console.log(num);
  
// undifiend 로 출력 
```

<br>

### null

- 명시적으로 변수 공간이 비어있음을 의미할 때 사용한다.
- 할당하지 않아도 **의도적으로** 메모리 공간을 비워두기 위해 사용하는 값

```jsx
let num = null; 
console.log(num); 
 
// null 로 출력 
```

<br>


### primitive(원시), reference(참조) 데이터 타입 초기화

```jsx
let address = undefined;  // 원시 타입 변수 초기화
let addressList = null; // 참조 타입 변수 초기화
```


<br>

### 에러와 `undefined`/`null`

- **`undefined`**: 철자나 변수에 문제가 있거나, 변수가 **초기화되지 않은 경우**에 발생하는 값이다.
- **`null`**: 객체에 들어가는 **주소가 없을 때** 주로 사용하며, 특정 오류가 발생할 경우 `null` 값으로 반환되기도 한다.

<br>
<br>



