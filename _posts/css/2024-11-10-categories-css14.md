---
title: "[CSS] 박스 모델 / Padding, Margin의 방향별 값 지정"
excerpt: "padding, margin으로 방향별 여백을 만드는 방법"

categories:
  - css
tags:
  - [css, css기초]

permalink: /categories/css/14

toc: true
toc_sticky: true

date: 2024-11-10
last_modified_at: 2024-11-10
---

## 🦥 본문

<br>


### 네 방향 여백 축약 지정

CSS에서 `padding`,  `margin` 속성은 <단일 값, 두 개, 세 개, 네 개 값>을 설정하여 여러 방향에 동시에 적용할 수 있다.

| 값의 개수 | 적용 방식                    | 예제                      | 의미                        |
|-----------|-------------------------------|---------------------------|-----------------------------|
| 1개       | 모든 방향 동일 값 적용        | `padding: 10px;`          | 모든 방향이 10px로 동일하게 적용됨 |
| 2개       | 세로(상/하), 가로(좌/우)      | `padding: 10px 20px;`     | 상, 하: 10px 좌, 우: 20px   |
| 3개       | 상, 가로(좌/우), 하 순서 적용 | `padding: 10px 20px 15px;`| 상: 10px 좌, 우: 20px 하: 15px |
| 4개       | 상, 우, 하, 좌 순서 적용      | `padding: 10px 20px 15px 5px;` | 상: 10px 우: 20px 하: 15px 좌: 5px |


> **Note:** `padding`과 `margin`에서 여러 값을 사용하는 경우, 상 → 우 → 하 → 좌 순서로 적용된다. (순서 중요!)
> 

<br>
<br>

### 네 방향 여백 축약 지정의 예제

```css

.box {
  padding: 10px 20px 15px 5px; /* 상, 우, 하, 좌 */
  border: 2px solid black;     /* 전체 테두리 */
  margin: 5px 10px;            /* 상/하, 좌/우 */
}
```

<br>
<br>

### padding, margin의 개별 방향 값 지정

| 속성 | 설명 |
| --- | --- |
| **상 방향** | `margin-top` 또는 `padding-top` 지정 |
| **하 방향** | `margin-bottom` 또는 `padding-bottom` |
| **좌 방향** | `margin-left` 또는 `padding-left` |
| **우 방향** | `margin-right` 또는 `padding-right` |

<br>

### 개별 방향 값 지정 예제**

```css

margin-top: 10px;  /*margin의 상단에만 10px 여백*/
margin-bottom: 15px; /*margin의 하단에 15px */
padding-left: 20px;
padding-right: 25px;
```

<br>
<br>

### 3. `margin: auto`를 사용한 여백 자동 지정

: `margin: auto`는 주로 **수평 중앙 정렬 (가운데 정렬)**을 위해 사용된다. 

위/아래 여백을 제외한 좌 우 여백이 균등하게 분배되어 컨테이너 내에서 가로로 가운데에 배치된다. 세로 정렬에는 사용되지 않으며, 주로 좌우 중앙 정렬에 사용된다.

- fixel이 고정되어야지만 `margin: 0 auto` 적용이 가능하다

<br>

### `margin: auto` 사용 예제

```css

.centered-box {
  width: 200px;
  margin: 20px auto; /* 위아래 여백 20px, 자동 중앙 정렬 */
}

.centered-box 2 {
  width: 200px;
  margin: 20px auto; /* 위아래 여백 0px, 자동 중앙 정렬 */
}
```

<br>
<br>

### 참고 사항

- `padding`에는 `auto` 값을 사용할 수 없으며, 요소의 **내부 여백은 고정된 크기**로만 설정된다.
- `margin`은 **음수 값**도 허용되며, 이 경우 요소가 다른 요소와 겹칠 수 있다.


<br>
<br>