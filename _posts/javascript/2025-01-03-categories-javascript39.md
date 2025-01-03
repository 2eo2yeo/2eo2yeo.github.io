---
title: "[JavaScript] 객체의 메서드, this 키워드"
excerpt: "객체에서 메서드 사용과, this 키워드를 이용하여 접근해보기"

categories:
  - javascript
tags:
  - [javascript, 자바스크립트]

permalink: /categories/javascript/39

toc: true
toc_sticky: true

date: 2025-01-03
last_modified_at: 2025-01-03
---

## 🦥 본문

<br>


### 메서드, this 키워드 개념 정리

- 메서드(Method)
    - 객체의 속성으로 함수를 정의한 것이다.
    - 객체 내에서 `function` 키워드를 사용하거나 ES6 이후에는 간단히 `속성명() {}` 형식으로 작성이 가능하다.
- `this` 키워드
    - 메소드 내부에서 `this`는 메소드를 호출한 객체 자신을 참조한다.
    - this 키워드를 통해 객체의 속성에 접근하거나 수정할 수 있다.

---

### 객체 안의 메서드 호출하기

- 메소드는 객체의 속성을 사용해 호출한다. (`객체명.메소드명()`)
- 호출 시 메소드가 객체와 연결되어 동작한다.

---

### [예제] 객체에서 기능을 실행하는 메소드

- 객체 생성

```sql
const apple = {
    name: "사과",
    color: "Red",
    emoji: "🍎",
    display : function () { console.log("🍎"); }, // 사과 이모티콘 출력
    getName: function () { console.log(this.name); }, // 객체의 name 속성 출력
    getColor: function () { console.log(this.color); }, // 객체의 color 속성 출력
    getEmoji: function () { console.log(this.emoji); } // 객체의 emoji 속성 출력
}
```

- 코드 설명
    - 객체 내에서 메서드 정의시 `속성명 : 함수` 의 형태로 작성한다.
    - this 키워드를 이용하여 자기자신(객체) 을 참조하여 출력하는 메서드를 생성함
- 객체 호출

```jsx
console.log(apple); // 객체를 출력 
apple.getName(); //getName 메서드 호출
apple.getColor(); // getColor 메서드 호출
apple.getEmoji(); // getEmoji 메서드 호출
```

<br>
<br>



