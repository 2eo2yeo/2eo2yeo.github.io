---
title: "[JavaScript] 객체(Object), 객체 리터럴, 객체의 속성 변경 및 삭제"
excerpt: "객체를 알아보고, 객체 리터럴, 객체의 속성에 관하여 예제로 실습해보기"

categories:
  - javascript
tags:
  - [javascript, 자바스크립트]

permalink: /categories/javascript/37

toc: true
toc_sticky: true

date: 2025-01-03
last_modified_at: 2025-01-03
---

## 🦥 본문

<br>

### **객체(Object)**

- 오브젝트는 다양한 타입의 데이터를 하나의 구조로 저장할 수 있는 데이터 형태다.
- 객체 프로퍼티의 값은 원시 값 데이터 타입 또는 다른 객체를 포함할 수 있다

---

### **객체 리터럴(Object Literal)**

- 객체 리터럴은 중괄호 **`{}`**를 사용해 간편하게 오브젝트를 생성하는 방식이다.
- 0개 이상의  **키(key) 와 값(value)의 쌍**으로 구성된다.
- 여기서 Key는 속성의 역할을 한다.

**구문**

```jsx
{property(key):value, property:value..}
```

---

### **[예제] 학생 정보에 관한 객체 데이터 생성**

```jsx
const student = {
    name: "홍길동",
    age: 20,
    address: "서울시",
    gender: "남"
};
```

- 객체는 여러 속성(예: 이름, 나이, 주소, 성별 등)을 묶어서 저장하는데 유용하다.
- **`name`**: **`"홍길동"`**과 같이 속성의 이름과 값을 쌍으로 정의한다.

---

### 객체 속성 접근 방법

```jsx
console.log(obj); // { name: '홍길동', age: 20 }
console.log(obj.name); // 홍길동 
console.log(obj.name, typeof obj.name); // 홍길동 string
console.log(obj.age, typeof obj.age); // 20 number
```

- 객체 전체를 출력하거나,
 `.` ,`[]` 연산자를 이용하여개별 프로퍼티에 접근해 값을 확인할 수 있다.
- `typeof`를 사용해 각 프로퍼티의 데이터 타입을 알 수 있다.

---

### **객체의 속성 변경 및 삭제**

• 오브젝트명은(주솟값) **`const`로 정의하면 변경할 수 없지만**, 객체 **내부의 속성 값은 변경이 가능**하다. 

1. **속성 값 변경 및 추가**
    - **`const`**로 선언한 오브젝트라도 속성 값은 변경할 수 있다.
    - . 점표기법으로 객체의 속성에 접근이 가능하다
        - 접근하려는 속성이 객체에 존재 : 기존 속성값이 변경
        - 접근하려는 속성이 객체에 존재x : 속성이 추가됨
    
    ```jsx
    // 이 객체의 주소인 obj는 변경이 불가능
    const obj = {    
        name : "홍길동",
        age : 20 }
    
    obj.name = '김철수'; // 기존 속성
    console.log(obj.name);  // 홍길동 -> 김철수
    ```
    
2. **속성 삭제**
    - **`delete`** 연산자를 사용해 속성을 삭제할 수 있다.
    
    ```jsx
    delete obj.age;     //obj의 age 삭제
    console.log(obj);   // '김철수' 만 출력
    ```
    
3. **속성 키 출력**
    - **`Object.keys(obj)`**로 객체의 모든 속성 키를 배열로 얻는다.
    - 객체의 key 로만 이루어진 배열을 반환한다.
    
    ```jsx
    console.log(Object.keys(obj));// [ 'name' ]
    ```
    

---

### 참고

MDN
<br>
<br>



