---
title: "[JavaScript] 객체 속성에 CRUD개념 적용하기"
excerpt: "객체 속성에 CRUD개념 적용하여 추가, 조회, 변경, 삭제를 할 수 있다. "

categories:
  - javascript
tags:
  - [javascript, 자바스크립트]

permalink: /categories/javascript/38

toc: true
toc_sticky: true

date: 2025-01-03
last_modified_at: 2025-01-03
---

## 🦥 본문

<br>

### **CRUD란?**

- **CRUD**는 **Create(생성), Read(읽기), Update(수정), Delete(삭제)의** 앞자리를 따서 만든 약자이다.
- 데이터베이스(DB)에서 쓰이는 개념이다.

---

### **객체 속성에 대한 CRUD 작업**

객체의 속성을 관리할 때도 **CRUD**(Create, Read, Update, Delete) 작업을 적용할 수 있다.  아래의 코드를 CRUD를 활용하여 작업해보자

```jsx
const person = {
    name: "홍길동",
    age : 20,
    job : "개발자"
}
const fruits = {
    name: "사과",
    emoji: "🍎"
}
```

📌 여기서 나올  …Value는 예를 들기 위한 변수명으로 내장함수가 아니다.

### **1. 새로운 속성 추가**

- 새로운 속성(key)과 값을 객체에 추가한다.
- **CRUD 중 Create에 해당한다.**

**예문**

```jsx
const setValue = (object, newKey, value) => 
object[newKey] = value;

setValue(person, "address", "서울시");   
```

→ setValue 함수는 3개의 파라미터를 받는다. 각각 person객체, "address" , “서울시”와 맵핑된다.

→ `object`에 `newKey`라는 새 속성을 추가하고(대괄호 접근법), 그 속성에 `value`를 할당함 

```jsx
// 결과
const person = {
    name: "홍길동",
    age : 20,
    job : "개발자"
    address : "서울시"
}
```

---

### **2.   속성, 값 불러오기**

- 객체의 특정 속성 값을 **가져오는** 작업이다.
- **CRUD 중 Read에 해당한다.**

```jsx
const getValue = (object, key) 
=> object[key];

console.log(getValue(person, "name"));
// person객체에서 name 속성의 값을 가져와라
```

→ `getValue` 함수는 `object`에서 `key`에 해당하는 값을 반환한다. 

---

### **3.  기존 속성 값 변경**

- 객체의 기존 속성의 값을 새로운 값으로 변경하는 작업입니다.
- **CRUD 중 Update에 해당한다.**

```jsx
const UpdateValue = (object, key, newValue) 
=> object[key] = newValue;

UpdateValue(person, "name", "김철수");
 //person 객체의 name 속성 값을 "김철수"로 수정
 
console.log(person);
```

→ `UpdateValue` 함수는 `object`의 `key`에 해당하는 값을 `newValue`로 변경한다. 

→ 기존에 `name`이란 속성이 있어야 변경이 가능

```jsx
// 결과
const person = {
    name: "김철수",
    age : 20,
    job : "개발자"
    address : "서울시"
}
```

---

### **4. 기존 속성 삭제**

- 특정 속성을 객체에서 삭제한다.
- **delete 연산자**를 사용함
- **CRUD 중 Delete에 해당한다.**

```jsx
const deleteValue = (object, key) => delete object[key];

deleteValue(person, "age");
// age 속성을 삭제해라
console.log(person);
```

→ `deleteValue` 함수는 `object` (person객체)에서 **delete 연산자를 사용하여** `key`(age)에 해당하는 속성을 삭제함 

```jsx
// 결과
const person = {
    name: "김철수",
    job : "개발자"
    address : "서울시"
}
```

<br>
<br>



