---
title: "[JavaScript] 객체 프로퍼티 축약(Short)"
excerpt: "객체 프로퍼티 명을 생략하여 코드를 간결하게 표현해 보자"

categories:
  - javascript
tags:
  - [javascript, 자바스크립트]

permalink: /categories/javascript/36

toc: true
toc_sticky: true

date: 2025-01-03
last_modified_at: 2025-01-03
---

## 🦥 본문

<br>


### 프로퍼티명 생략이 가능한 때

**변수명을** 그대로 **객체의 프로퍼티명**으로 사용할 경우, **프로퍼티 이름을 생략**할 수 있다.
 축약 문법을 사용하면 `key` 이름은 변수 이름, `value`는 해당 변수의 값으로 자동 설정됨.

---

### 프로퍼티 축약 예제

**[예제1]  프로퍼티명 생략 문법 사용**

```jsx
let name = "홍길동";
let age = 20;

// 기존 방식: { name: name, age: age }
const person = { name, age }; // 프로퍼티 생략 문법 사용

console.log(person.name); // 출력: 홍길동
console.log(person.age);  // 출력: 20
```

**→** 설명: 객체를 생성할 때, 변수 이름과 프로퍼티 이름이 동일하다면 `key: value`를 value만 사용하여 축약할 수 있다. 

- 생성된 객체의 형태는 다음과 같다.

```jsx
person = { name: "홍길동", age: 20 }
```

**[예제2] : 사원들의 정보를 입력받아서, 객체로 반환하는 함수 생성**

- 조건
    - 사원들의 정보를 입력받아서, 객체로 반환하는 함수를 정의한다
    - {empno: "1234", ename:"홍길동", age:20} 으로 출력되도록 한다.
    - 객체 정보 :  사번(empno), 이름(ename), 나이(age)

```jsx
function createObject(empno, ename, age) {
    return { empno, ename, age };// 축약 문법
}

// 값 전달 밑 출력
console.log(createObject('1234', '홍길동', 20));
console.log(createObject('7854', '김[수', 30));
```

→ 축약 문법: `{ empno, ename, age }`는 `{ empno: empno, ename: ename, age: age }`를 간결하게 표현한 형태이다.

→ 출력과 동시에 값을 전달한다.

- 생성된 객체의 형태는 다음과 같다

```sql
[
		{
		    empno: '1234',
		    ename: '홍길동',
		    age: 20
		},
	{
	    empno: '7854',
	    ename: '김철수',
	    age: 30
	}
]
```

<br>
<br>



