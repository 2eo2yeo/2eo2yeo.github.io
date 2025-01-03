---
title: "[JavaScript] 객체 생성자 함수 (Object Construtor)"
excerpt: "객체 생성자 함수란?, new 키워드를 사용하여 새로운 객체를 생성"

categories:
  - javascript
tags:
  - [javascript, 자바스크립트]

permalink: /categories/javascript/40

toc: true
toc_sticky: true

date: 2025-01-03
last_modified_at: 2025-01-03
---

<br>


### 객체 생성자 함수란?

- **객체를 생성하는 함수**이다.
- 동일한 구조의 객체를 여러개 생성해야할 때 효율적이다.

---

### 생성자 함수의 특징

1. 첫 글자는 대문자
2. 필드(Field)와 메서드(Method):
    - 필드(Field): 객체의 **속성(프로퍼티)**을 정의한다. 
    → (필드 안에 들어가는 내용을 파라미터로 받음)
    - 메서드(Method): 객체 안에서만 사용되는 함수입니다
3. `new` 연산와 함께 사용한다.

 ➕ `this` 키워드의 사용

- 생성자 함수 안에서 `this`는 생성된 객체 자신을 가리킨다.
- 이렇게 this에 연결되어 있는 프로퍼티와 메소드는 외부에서 참조가 가능하다.

---

### 예제 1  : 객체 생성자 함수 생성(과일 정보)

**[객체 생성자 함수 정의]**

```jsx
function Fruit(name, color, emoji) {
    // 필드(속성) 정의
    this.name = name;   // 과일 이름
    this.color = color; // 과일 색상
    this.emoji = emoji; // 과일 이모지

    // 메서드 정의, 이모지 출력하는 메소드
    this.display = () => console.log(this.emoji); 
}
```

→ `Fruit` 생성자 함수는 `name`, `color`, `emoji` 매개변수를 받아 속성과 메소드를 정의한다.

**[ `new` 키워드를 사용하여 새로운 객체 생성 및 출력]** 

```jsx
// 키워드 `new`를 사용하여 새로운 객체 생성
const apple = new Fruit("apple", "red", "🍎");
const orange = new Fruit("orange", "coral", "🍊");

// 객체 출력
console.log(apple);
console.log(orange);

//메소드 호출
apple.display(); // 🍎
orange.display(); // 🍊
```

- 생성자 함수를 호출할 때 `new` 키워드를 사용합니다. `new`는 새로운 객체를 힙 메모리에 생성하고, `this`를 해당 객체로 연결해준다.
- `new Fruit(...)`로 호출하면 `Fruit` 함수 내부에서 `this`가 새로운 객체를 가리키게 된다.
- 속성과 메소드가 `this`를 통해 새 객체에 추가된다.
- 생성된 객체는 속성과 메소드에 접근할 수 있다. 예를 들어 `apple.name`은 `"apple"` 값을 반환하며, `apple.display()`는 `🍎`를 출력한다.
- 생성된 객체는(위에서 출력된) 다음과 같다.

```jsx
// apple 객체
{
  name: "apple",
  color: "red",
  emoji: "🍎",
  display: () => console.log(this.emoji)
}

// orange 객체
{
  name: "orange",
  color: "coral",
  emoji: "🍊",
  display: () => console.log(this.emoji)
}
```

**[위 코드 메모리 작동 방식]**

- 콜 스택(Call Stack) → `apple`과 `orange`는 콜 스택에 변수로 저장된다. 이 변수들은 객체의 주소값을 참조한다.
- 힙(Heap) 메모리: `new Fruit(...)`로 생성된 객체는 힙 메모리에 저장된다. 콜 스택에 있는 변수들은 이 힙 메모리에 저장된 객체의 주소를 참조한다.

---

### 예제 2  : 객체 생성자 함수 생성 및 호출 (객체 모델링-반려동물, 동물병원..)

- 조건1 : 속성 - name, color
- 조건2 : 메소드 - display('🐶'), eat('🐶 먹는다.'), sleep('🐶 자요~')

**[생성자 함수 정의]**

```jsx
function Animal(emoji, color) {
    //field
    this.emoji = emoji;
    this.color = color;

    //method
    this.display = () => console.log(this.emoji);
    this.eat = () => console.log(`${this.emoji} 먹는다.`);
    this.sleep = () => console.log(`${this.emoji} 잔다.`);
}
```

**[new 키워드를 이용하여 새로운 객체 생성]**

```jsx
const dog = new Animal('🐶', 'brown');
const cat = new Animal('🐱', 'yellow');
const rabbit = new Animal('🐰', 'gray');
```

**[메서드 호출]**

```jsx
dog.display(); // 🐶
dog.eat();    // 🐶 먹는다.
dog.sleep();  // 🐶 잔다.

cat.display(); // 🐱
cat.eat();     // 🐱 먹는다.
cat.sleep();   // 🐱 잔다.

rabbit.display();   // 🐰
rabbit.eat();      // 🐰 먹는다.
rabbit.sleep();    // 🐰 잔다.
```

**[위에서 생성된 객체 형태 → 강아지만, 실제로 출력되는 것은 아님]** 

```jsx
// dog 객체
{
  emoji: '🐶',
  color: 'brown',
  display: () => console.log(this.emoji),
  eat: () => console.log(`${this.emoji} 먹는다.`),
  sleep: () => console.log(`${this.emoji} 잔다.`)
}
```

→ 새롭게 생성된 객체는 이와 같은 형태를 가지고 있다.

<br>
<br>



