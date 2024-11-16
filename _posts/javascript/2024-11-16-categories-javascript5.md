---
title: "[JavaScript] 탬플릿 리터럴 "
excerpt: "탬플릿 리터럴의 다양한 표현방법을 알아보자"

categories:
  - javascript
tags:
  - [javascript, 자바스크립트기초]

permalink: /categories/javascript/5

toc: true
toc_sticky: true

date: 2024-11-16
last_modified_at: 2024-11-16
---

## 🦥 본문

<br>
<br>


### 문자열 접합 연산자 (기존 방식)

자바스크립트에서는 문자열을 연결할 때 **`+` 연산자**를 사용할 수 있다. 이 방법을 사용하면 여러 개의 문자열과 변수를 하나의 문장으로 연결할 수 있다.

```jsx
let myName = "홍길동";
let myAge = 30;
let output = "저의 이름은 " + myName + "이고, 나이는 " + myAge + "입니다.";
console.log(output); // 저의 이름은 홍길동이고, 나이는 30입니다.

```

---

<br>


### 템플릿 리터럴 (최신 방식)

- 기존엔 접합 연산자를 이용해 문자열을 표현했지만 ES6부터는 **템플릿 리터럴(Template Literal)**을 사용한다.
- **백틱(```) 기호**를 사용하여 문자열을 감싸며, **`${}`*를 사용해 변수를 삽입할 수 있다.
- 표현식/문자열 삽입, 여러 줄 문자열, 문자열 형식화, 문자열 태깅 등 여러 다양한 작업이 가능하다.

```jsx
let myName = "홍길동";
let myAge = 30;

// 템플릿 리터럴 사용
let output2 = `저의 이름은 ${myName}이고, 나이는 ${myAge}입니다.`;
console.log(output2); // 저의 이름은 홍길동이고, 나이는 30입니다.

```

<br>

### 여러 줄 문자열 작성

템플릿 리터럴을 사용하면 줄 바꿈이 필요한 문자열도 간단히 작성할 수 있다.

```jsx
let multiLine = `안녕하세요
저는
홍길동입니다.`;
console.log(multiLine);

```

<br>

### **문자열 형식화**:

숫자, 날짜, 객체 등 다양한 값을 형식화하여 문자열에 포함시킬 때 유용하다.

```jsx
let price = 1500;
let formatted = `상품의 가격은 ${price.toLocaleString()}원입니다.`;
console.log(formatted); // 상품의 가격은 1,500원입니다.

```
<br>

### **문자열 태깅(Tagging)**:

- 태그 함수와 함께 사용하여 문자열을 더 복잡하게 처리하거나 구문 분석을 할 수 있다.
    
    ```jsx
    function tag(strings, ...values) {
        console.log(strings); // ['이름: ', ', 나이: ', '입니다.']
        console.log(values);  // ['홍길동', 30]
        return `${strings[0]}${values[0]}${strings[1]}${values[1]}${strings[2]}`;
    }
    
    let taggedOutput = tag`이름: ${name}, 나이: ${age}입니다.`;
    console.log(taggedOutput); // 이름: 홍길동, 나이: 30입니다.
    
    ```

<br>
<br>



