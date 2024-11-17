---
title: "[JavaScript] 제어문 - 조건문 : if , else if"
excerpt: "조건문 if, else if에 대해서 알아보자"

categories:
  - javascript
tags:
  - [javascript, 자바스크립트기초]

permalink: /categories/javascript/15

toc: true
toc_sticky: true

date: 2024-11-17
last_modified_at: 2024-11-17
---

## 🦥 본문

<br>
<br>

- `if` 문은 조건식이 **참**일 때만 중괄호 `{}` 안의 코드를 실행하는 조건문이다. 특정 조건을 만족할 경우에만 동작하는 로직을 설정할 수 있다.
- **특징** : boolean 값을 리턴한다.

<br>

### if, else if 구문

```jsx
if ( 조건식 : 비교연산자 포함 ) 
	{ 조건식이 참인 경우 동작문 ; }

if ( 조건식 ) { true 일 때 동작문; } 
	else { false일 때 동작문 ; }

 if (조건식1 ) {조건식 1이 참일때 동작문; } 
	 else if(조건식2) {조건식2가 참일때 동작문; } 
	 .... else { 모든조건식에 해당되지 않을때; }

```
<br>

### 예시코드 1 →  if문 기본형과 삼항연산자

- 요구 : 입력되는 과일명이 apple인 경우에는 사과이모지 출력, 사과이외의 과일은 이름만 출력!!

```jsx
/*** if문 기본형 ***/

let fruit = "apple";
if(fruit === "apple") {
    console.log('🍎');
} else {
    console.log(fruit);    
}

/*** 삼항연산자로 변경 ***/
let display = undefined;
(fruit === "apple") ? (display ='🍎') : (display = fruit) ;
console.log(display);
```

<br>

### 예시코드 2 →  중괄호`{}` 생략

- 점심메뉴 : pizza - '🍕' , hotdog - '🌭’
- 요구사항 : 점심메뉴에 피자와 핫도그가 있다. 피자와 핫도그 중에서 선택한 메뉴에 따라 이모지가 출력되도록 한다.

```jsx
/* 중괄호 생략이 가능한 경우 */
let menu = undefined;
menu = 'pizza';
if(menu === 'pizza') console.log('🍕');  
else console.log('🌭');

/* 중괄호 생략이 불가능한 경우 */
if(menu === 'pizza') { 
    console.log(menu);    
    console.log('🍕');
} else console.log('🌭');
```

- 설명 : `if`, `else if`, 또는 `else` 문에서 **중괄호**는 **동작문이 하나만 있을 때** 생략할 수 있다. 즉, 실행할 코드가 **한 줄**일 때만 중괄호를 생략할 수 있다.

<br>

### 예시코드 3 → 중간 결과값을 사용하여 코드 줄이기

- 요구사항 : 학생명이 홍길동, 홍길순, 김영희 인지 체크하여 해당하는 경우 이름을 출력하고, 해당하지 않는 경우 '해당 학생 없음' 으로 출력해주세요
- 출력포맷 : 실행결과 ==>

```jsx
/* 중간 결과 값이 없을 때의 코드 */

let name = undefined;
let result = undefined;

name = 김영희;
// 설명 : name = ‘김영희’; 가 참일 경우 조건문이 실행된다.

if (name === '홍길동') {
    console.log(`실행결과 ==> ${name}`);
} else if (name === '홍길순') {
    console.log(`실행결과 ==> ${name}`);
} else if (name === '김영희') {
    console.log(`실행결과 ==> ${name}`);
} else {
    console.log('실행결과 ==> 해당 학생 없음');
}

/* 중간 결과값 result를 선언한 후의 코드 */
let name = undefined;
let result = undefined;
name = '김영희';

	if (name === '홍길동') {
	    result = name;
	} else if (name === '홍길순') {
	    result = name;
	} else if (name === '김영희') {
	    result = name;
	} else {
    result = '해당 학생 없음';
	}

console.log(`실행결과 ==> ${result}`);
```

- `result`는 중간 결과 값을 저장하는 변수로, 각 조건에 따라 `result`에 값을 할당한 후, 마지막에 `console.log`를 사용해 최종 결과를 출력한다.

<br>
<br>



