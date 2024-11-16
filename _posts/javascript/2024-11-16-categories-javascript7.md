---
title: "[JavaScript] 원시타입(Primitive Type) - 숫자형, 문자열형, 논리형"
excerpt: "원시타입 종류 중 숫자형, 논리형에 대해 알아보자"

categories:
  - javascript
tags:
  - [javascript, 자바스크립트기초]

permalink: /categories/javascript/7

toc: true
toc_sticky: true

date: 2024-11-16
last_modified_at: 2024-11-16
---

## 🦥 본문

<br>
<br>


원시 타입(Primitive Type) 은 자바스크립트에서 가장 기본적인 데이터 타입을 말한다. 원시 타입의 값은 객체가 아닌 단순한 데이터다. 숫자형, 문자열형, undefined, null, 논리형, symbol … 등이 있다.

<br>

### 숫자형 (Number)

- 정수, 소수 를 포함한 숫자 데이터
- 자바스크립트는 모든 숫자의 형태를 허용한다.

```jsx
let number = 10;
let double = 10.234;
let negative = -10;
let hex = 0xa;
...
```

<br>

### 문자열형 (string)

- 큰따옴표 `“”` 작은 따옴표 `‘’` 로 둘러 쌓여진 값
- 어떤 따옴표를 써도 상관없지만 시작한 따옴표 형태로 시작과 끝을 맺어야 한다.
- 따옴표 사이에 따옴표를 꼭 사용해야 할 때, 이스케이프 문자인 역슬래시`\` 를 사용한다. (큰따옴표 안의 작은 따옴표는 문제되지 않으나, 큰따옴표를 중복사용할 경우)

```bash
let str = "abc";   // 큰따옴표
let str2 = 'def';  // 작은따옴표
let str3 = "I'm Fine Thank You \"and you? \"";
              // 중복따옴표에는 역슬래시
```

<br>

### **undefined 과 null**

- undefined
    
    : 값을 할당하지 않은 경우에도 undefined라는 값을 자동으로 할당함
    
- null
    
    :  할당하지 않아도 **의도적으로** 메모리 공간을 비워두기 위해 사용하는 값 
    

👇자세한 것은 아래 링크로

[https://2eo2yeo.github.io/categories/javascript/8]

<br>

### boolean type (논리형)

- 참(True)과 거짓(False) 으로 올바른지 틀린지를 판단한다.

```jsx
let isGreater = (2 > 3); // 2가 3보다 큰지 비교, 결과는 false

console.log(isGreater); // false

```


<br>
<br>



