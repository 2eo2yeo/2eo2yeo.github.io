---
title: "[CSS] 레이아웃 - Display : Flex "
excerpt: "레이아웃을 한방향으로 배치해보자, flex 총정리"

categories:
  - css
tags:
  - [css, css기초]

permalink: /categories/css/18

toc: true
toc_sticky: true

date: 2024-11-10
last_modified_at: 2024-11-10
---

## 🦥 본문

<br>

### 📌 CSS `flex` 속성 설명

`flex`는 **플렉스 박스(Flexbox)** 레이아웃을 활용해 요소들을 효율적으로 배치하는 데 사용된다

- flex  박스는 최신 레이아웃 작성 방식이다
- 부모 요소에  `display : flex` 를 지정하면 자식요소는 자동으로 가로 배치가 된다.
- 이때 부모요소를 `flex box`, 자식 요소를 `flex item` 이라고 한다
- 하나의 축만을 가지고 정렬한다 (가로 or 세로)

<br>

## 🌟 **Flexbox의 기본 개념**

1. *부모 요소(컨테이너)**에 `display: flex`를 설정하면 자식 요소들이 Flexbox 레이아웃으로 정렬됩니다. 
2. 기본적으로 주축의 시작점 → 끝점으로 배치, 교차축의 시작점 → 끝점으로 배치
3. **부모 요소의 속성**: 주로 **전체 레이아웃**과 **정렬 방식을 설정**합니다.
4. **자식 요소의 속성**: 개별 아이템의 **크기와 정렬**을 조정합니다.

| 속성명: 값            | 설명                                                        |
|-----------------------|-------------------------------------------------------------|
| `display: flex;`      | 플렉스 박스를 블록수준으로 작동하게 한다.                   |
| `display: inline-flex;` | 플렉스 박스로 인라인 플렉스 수준으로 작동하게 한다.        |


---

<br>
<br>



## 1. Flex Box 속성들 (부모 요소)

### 1-1 ) `flex-direction` (주축 방향 설정)

➡️ **설명 : 주(메인) 축이 될 정렬 방향을 설정, 메인 축을 가로로 할지 세로로 할지 결정한다.**

| 값               | 설명                                                         |
|------------------|--------------------------------------------------------------|
| `row`            | 디폴트 값 / 행으로 표현, 가로 정렬 (왼쪽 → 오른쪽)          |
| `row-reverse`    | 행 형태에서 반전됨, 가로 정렬 (오른쪽 → 왼쪽)               |
| `column`         | 열으로 표현, 세로 정렬 (위 → 아래)                          |
| `column-reverse` | 열 형태에서 반전됨, 세로 정렬 (아래 → 위)                   |


<br>

**예제:**

```css
.container {
  display: flex;
  flex-direction: row;
}

```

---

<br>
<br>

### 1-2) `justify-content` (주 축 정렬)

➡️ **설명 : 주축을 따라 아이템을 정렬 한다.**

| 값               | 설명                                                                                   |
|------------------|----------------------------------------------------------------------------------------|
| `flex-start`     | 앞에서 시작, 아이템을 주 축의 시작 지점으로 정렬 (기본값)                              |
| `flex-end`       | 끝에서 시작, 주 축의 끝 지점으로 정렬                                                  |
| `center`         | 가운데서 시작, 주 축 중앙으로 정렬                                                     |
| `space-between`  | 양쪽 정렬 - 끝을 기준으로 맞춰짐                                                      |
|                  | 아이템 간에 동일한 간격 부여, 양끝에 여백 없음                                         |
| `space-around`   | 아이템 주위에 동일한 간격 부여                                                         |
|                  | 아이템 하나당 좌우 공간을 동일하게 설정                                                |
| `space-evenly`   | 아이템 간 간격을 균등하게 부여                                                        |

<br>

**예제:**

```css
.container {
  display: flex;
  justify-content: center;
}
```

---


<br>
<br>

### 1-3) `align-items`

➡️ **설명**  교차축(예를 들어 주축이 가로일 경우 세로축이 교차축이다) 에서 정렬한다.
주축이 가로로 설정되어있다고 하면 세로라고 생각하면 쉽다. 

<br>

| 값            | 설명                                    |
|---------------|-----------------------------------------|
| `stretch`     | 아이템을 교차 축을 따라 늘림 (기본값)   |
| `flex-start`  | 교차 축의 시작 지점에 정렬              |
| `flex-end`    | 교차 축의 끝 지점에 정렬                |
| `center`      | 교차 축의 중앙으로 정렬                 |
| `baseline`    | 텍스트 기준선에 맞춰 정렬               |

<br>

**예제:**

```css

.container {
  display: flex;
  align-items: center;
}
```

---

<br>
<br>


### 1-4)  `align-content` (여러 행 정렬)

- *`align-content`*는 플렉스 아이템이 여러 줄에  걸쳐있을 때(나눠져 있을 때) 교차 축에서의 정렬 방식을 설정합니다.

| 값              | 설명                                                        |
|-----------------|-------------------------------------------------------------|
| `stretch`       | 아이템이 교차 축을 따라 늘어남 (기본값)                     |
| `center`        | 교차 축 중앙에 정렬                                        |
| `flex-start`    | 교차 축의 시작 지점에 정렬                                 |
| `flex-end`      | 교차 축의 끝 지점에 정렬                                   |
| `space-between` | 아이템 간에 동일한 간격 부여, 양끝에 여백 없음              |
| `space-around`  | 아이템 주위에 동일한 간격 부여                             |

<br>

**예제:**

```css

.container {
  display: flex;
  flex-wrap: wrap;
  align-content: space-around;
}

```

➡️ **설명:** 여러 줄의 아이템들이 교차 축을 따라 균등하게 배치됩니다.

---

<br>
<br>


## 2. Flex Item 속성들 (자식)

: 플랙스 박스에 여백이 있을 때 플렉스 아이템의 크기를 어떻게 늘려서 빈 여백을 채울지를 결정하는 속성

### 2-1) `flex-grow`, `flex-shrink`, `flex-basis`

| 속성          | 설명                                                 | 예제                  |
|---------------|------------------------------------------------------|-----------------------|
| `flex-grow`   | 남은 공간을 얼마나 차지할지 결정 (기본값: 0)         | `flex-grow: 1;`      |
| `flex-shrink` | 넘치는 아이템의 크기를 줄임 (기본값: 1)              | `flex-shrink: 1;`    |
| `flex-basis`  | 아이템의 기본 크기 설정                              | `flex-basis: 100px;` |
| `flex`        | 위의 3가지 속성을 순서대로 한 번에 지정 가능         | `flex: 1 1 0;`       |

<br>

**예제:**

```css

.item {
  flex-grow: 2;
  flex-basis: 50px;
}
```

➡️ **설명:** 각 아이템이 초기 크기 50px을 가지며, 남은 공간의 두 배를 차지합니다.

---

<br>
<br>


### `order` (아이템 순서 설정)

| 속성   | 설명                                                                                  |
|--------|---------------------------------------------------------------------------------------|
| `order`| 아이템이 화면에 나타나는 순서를 설정 (기본값: 0)                                     |
|        | 양수, 음수 지정 가능하고 속성의 값이 적을 수록 먼저 표시됨                            |


<br>

**예제:**

```css
.item {
  order: 1;
}
```

➡️ **설명:** 해당 아이템이 다른 아이템들 뒤에 배치됩니다.

---

<br>
<br>



## **3. 줄 바꿈과 간격 설정**

### 3-1) `flex-wrap` (줄 바꿈 설정) - 부모

| 값            | 설명                                   |
|---------------|----------------------------------------|
| `nowrap`      | 줄 바꿈 없이 한 줄에 배치 (기본값)     |
| `wrap`        | 줄 바꿈 허용 (아래로 이동)             |
| `wrap-reverse`| 줄 바꿈 허용 (위로 이동)               |

<br>

**예제:**

```css
.container {
  display: flex;
  flex-wrap: wrap;
}
```

➡️ **설명:** 아이템이 한 줄에 가득 차면 다음 줄로 넘어갑니다.

---

<br>
<br>


### 3-2) `gap` (아이템 간 간격 설정)

| 속성  | 설명                                 |
|-------|--------------------------------------|
| `gap` | 플렉스 아이템 간의 간격을 설정       |

<br>

**예제:**

```css
.container {
  display: flex;
  gap: 10px;
}
```

➡️ **설명:** 각 아이템 간의 간격이 10px로 설정됩니다.

---


<br>
<br>


## flex 전체 예제 코드

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Flexbox Example</title>
  <style>
    .container {
      display: flex;
      flex-direction: row;
      justify-content: space-around;
      align-items: center;
      gap: 20px;
      height: 100vh;
    }

    .item {
      background-color: #4CAF50;
      color: white;
      padding: 20px;
      font-size: 24px;
      text-align: center;
    }
  </style>
</head>
<body>
  <div class="container">
    <div class="item">Item 1</div>
    <div class="item">Item 2</div>
    <div class="item">Item 3</div>
  </div>
</body>
</html>

```


<br>
<br>