---
title: "[JavaScript] 제어문 - 반복문 : For"
excerpt: "반복문 for에 대해서 알아보자"

categories:
  - javascript
tags:
  - [javascript, 자바스크립트기초]

permalink: /categories/javascript/17

toc: true
toc_sticky: true

date: 2024-11-17
last_modified_at: 2024-11-17
---

## 🦥 본문

<br>
<br>


### **반복문 : `for` 문**

- `for` 문은 **반복 횟수가 명확할 때** 사용하는 반복문이다. 초기값 설정, 조건식, 증감식을 사용하여 반복을 제어한다.
- **Array(배열)**과 함께 자주 쓰인다.

---

<br>

### **사용 방법**

```jsx

for ( 1️⃣ 초기값;  2️⃣조건식 ;  4️⃣증감식 ) {
    3️⃣실행문;}

```

- **초기값**: 반복에 사용할 변수를 선언하고 초기화한다. **반복문이 몇번 실행될지 설정**할 때 사용한다. `for` 블록 내에서만 유효하다.
- **조건식**: 각 반복 전에 평가되며, **`true`일 경우** 실행문을 실행한다. **`false`일 경우** 반복을 종료한다.
- **증감식**: 실행문이 끝난 후, 변수를 증감시켜 다음 반복을 준비한다.


<br>

### **작동 순서**

1. 1️⃣**초기값**을 선언한다. (한 번만 실행)
2. 2️⃣**조건식(boolean)**으로 평가하여 `true`면 실행문을 실행하고, `false`면 반복문을 종료한다.
3. **4️⃣실행문**을 실행한다.
4. **3️⃣증감식**을 실행하여 변수를 증가하거나 감소시킨다.
5. 2️⃣~4️⃣ 과정을 반복하여 조건식이 `false`가 될 때 `for` 루프를 종료한다.
    
    ex. a에 5라는 값을 할당함, a를 1씩 증가시켜서 a>5 라는 식이 될때 false가 되어 루프 종료
    
<br>

---

### **예제 코드**

**(예제 1)  1부터 100까지 출력**

```jsx
for (let i = 1; i <= 100; i++) {
    console.log(i);}
```

- **설명**: `i`가 1부터 100까지 증가하며(i의 값이 계속 변화), 각 값을 출력한다.

<br>

**(예제 2)   배열 요소 출력**

```jsx

let numberList = ['🍕', '🍔', '🍟'];
for (let i = 0; i <= numberList.length-1; i++) {
    console.log(numberList[i]);
}
// 출력 결과 
🍕
🍔
🍟
```

- **초기값**: `let i = 0` → 반복 변수 `i`를 0으로 초기화한다. 배열의 인덱스는 0부터 시작하기 때문에 0으로 설정한다.
- **조건식**: `i <= numberList.length - 1` 는`i`가 배열의 마지막 인덱스보다 작거나 같을 때(`numberList.length - 1`) 반복을 계속한다.  → `numberList.length`는 3이므로, `numberList.length - 1`은 2가 된다. 따라서 `i`는 0, 1, 2일 때까지 반복된다.
- **증감식**: `i++` → 각 반복이 끝날 때마다 `i`를 1씩 증가시킨다.
- **출력** : `numberList[i]`는 `i`의 값에 해당하는 배열의 요소를 가리킨다.
- **공식** : **배열의 마지막 인덱스는 `배열 크기 - 1` , 배열의 크기 구하는 형식 : `배열객체.length`**

<br>

**(예제 3)  과일 리스트와 이모지 출력**

```jsx
let fruitList = ['apple', 'orange', 'lemon'];  // 배열 선언 및 초기화 
let emojiList = ['🍎', '🍊', '🍋'];           // 배열 선언 및 초기화 

let length = fruitList.length-1;   //lenght에 배열의 크기 할당

for (let k = 0; k < length; k++) {
    let fruit = fruitList[k];
    let emoji = emojiList[k];
    if (fruit === 'lemon') {
        console.log(emoji);
    }
}   

//실행결과 : 🍋
```

- for문 설명
    - **초기값**: `let k = 0` → 반복 변수 `k`를 0으로 초기화. 배열의 인덱스는 0부터 시작하기 때문에 0으로 설정.
    - **조건식**: `k < length` → `k`가 `fruitList` 배열의 길이보다 작을 때 반복. `fruitList.length`는 3이므로 `k`는 0, 1, 2일 때까지 반복한다.
    - **증감식**: `k++` → 각 반복이 끝날 때마다 `k`를 1씩 증가시켜 다음 인덱스를 가리킨다.
- 실행문 설명
    - `fruit = fruitList[k]`: `fruit`에 `fruitList`의 현재 인덱스 `k`에 해당하는 과일 이름을 할당.
    - `emoji = emojiList[k]`: `emoji`에 `emojiList`의 현재 인덱스 `k`에 해당하는 이모지를 할당.
- if 문 조건 검사
    - `fruit`가 `'lemon'`일 경우에만 `emoji`를 출력하는 조건.
    - `fruitList[2]`가 `'lemon'`이므로, `emojiList[2]`인 `'🍋'`가 출력됨

<br>
<br>



