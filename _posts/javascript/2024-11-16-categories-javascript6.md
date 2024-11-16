---
title: "[JS] 자료형 개념 (원시타입, 참조타입) "
excerpt: "자바스크립트 데이터의 유형을 구분해보자"

categories:
  - javascript
tags:
  - [javascript, 자바스크립트기초]

permalink: /categories/javascript/6

toc: true
toc_sticky: true

date: 2024-11-16
last_modified_at: 2024-11-16
---

## 🦥 본문

<br>
<br>


*유튜브 수코딩님 강의를 수강하고 작성하였습니다.

<br>

### 자료형이란?

값이 가질 수 있는 여러가지 유형을 구분한 개념

<br>

### 자료형의 구분

| 구분            | 종류                                                                          |
|-----------------|-------------------------------------------------------------------------------|
| 원시타입        | 숫자형(number), 문자형(string), 논리형(boolean), null, undefined, symbol     |
| (primitive type)|                                                                               |
| 참조 타입       | 배열(array), 객체(object), 함수(function)                                     |
| (reference type)|                                                                               |

<br>

- 원시타입
    
    : 기본타입: 원시 데이터로 더이상 단순화 할 수 없는 값, 데이터 및 정보의 가장 단순한 형태, 내가 갖고있음 
    

```bash
//원시타입의 종류

let number = 1; //숫자형
let str = "abc"; //문자열형
let bool = true //또는 false, 논리형
let undi = undefined; //자동할당 디폴트값
let nul = null; // null(object)
let symbol = symbol();
```

<br>

- 참조 타입
    
    : 다른 여러 값으로 구성된복합 값, 기본 타입외의 모든 타입으로 객체, 크기가 크다, 내가 갖고있지 않고 다른 곳에 있는 것을 가르킴, 다른 것을 참조함
    

```bash
// 참조타입의 종류

let array = []; // 배열
let obj = {}; // 객체
let func = function(){}; //함수
```
<br>
<br>



