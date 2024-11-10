---
title: "[CSS] 레이아웃 Display : grid"
excerpt: "레이아웃을 두방향으로 배치해보자"

categories:
  - css
tags:
  - [css, css기초]

permalink: /categories/css/19

toc: true
toc_sticky: true

date: 2024-11-10
last_modified_at: 2024-11-10
---

## 🦥 본문

<br>

### `grid` 설명
flex가 한 방향 레이아웃, 수직 or 수평으로의 정렬  형식이라면 

grid는 두 방향 레이아웃  형식 가상의 grid라는 가상의 레이아웃을 만들어서 요소를 배치한다.

<br>

### `grid` 의 속성

| 속성                   | 설명                                                                                                     |
|------------------------|----------------------------------------------------------------------------------------------------------|
| `display: grid`        | 요소를 그리드 컨테이너로 설정하여 자식 요소들이 그리드 아이템으로 배치되도록 함                           |
| `grid-template-rows`   | 행(row)의 크기 및 개수를 정의.                                                                           |
|                        | - 예: `grid-template-rows: 100px 200px`                                                                  |
|                        | - 각각의 행을 크기를 100px, 200px로 지정, `fr`(분수), %의 단위도 쓸 수 있음                               |
| `grid-template-columns`| 열(column)의 크기 및 개수를 정의. 예: `grid-template-columns: 1fr 2fr`                                   |
| `gap`                  | 행과 열 사이의 간격을 설정. `gap` 속성을 사용해 줄 수도 있음. 예: `gap: 10px`                             |
| `grid-template-areas`  | 영역 이름을 정의하여 그리드를 레이아웃할 때 이름을 기반으로 배치할 수 있음                                |


<br>

### grid와 함께 사용되는 속성

- 아이템을 좀 더 디테일하게 배치하기

아래는 `display: grid` 속성과 함께 자주 사용하는 속성이다.

| 속성                | 설명                                       | 예시                                 |
|---------------------|--------------------------------------------|--------------------------------------|
| `grid-auto-rows`    | 자식 요소의 자동 행 크기를 설정            | `grid-auto-rows: minmax(100px, auto);` |
| `grid-auto-columns` | 자식 요소 자동 열 크기를 설정              | `grid-auto-columns: 200px;`         |
| `grid-area`         | 특정 그리드 영역에 자식 요소를 배치        | `grid-area: header;`                |
| `align-items`       | 그리드 항목을 수직으로 정렬                | `align-items: center;`              |
| `justify-items`     | 그리드 항목을 수평으로 정렬                | `justify-items: stretch;`           |


### 예제 코드

 `display: grid`를 사용하여 3x3 그리드를 생성해보자.

```css

.container {
    display: grid;
    grid-template-rows: 1fr 1fr 1fr;
    grid-template-columns: 1fr 1fr 1fr;
    gap: 10px;
}

.item {
    background-color: #ccc;
    padding: 20px;
    text-align: center;
}

```

---

<br>


### grid Item에 사용하는 속성

| 속성               | 설명                                                   | 사용법 / 예시                      |
|--------------------|--------------------------------------------------------|------------------------------------|
| `grid-row`         | 요소가 어느 행부터 어느 행까지 차지할지를 정의합니다.  | `grid-row: 1 / 4;`                 |
| `grid-row-start`   | 요소가 차지할 행의 시작선을 지정합니다.                | `grid-row-start: 1;`               |
| `grid-row-end`     | 요소가 차지할 행의 끝 선을 지정합니다.                 | `grid-row-end: 4;`                 |
| `grid-column`      | 요소가 어느 열부터 어느 열까지 차지할지를 정의합니다.  | `grid-column: 1 / 4;`              |
| `grid-column-start`| 요소가 차지할 열의 시작선을 지정합니다.                | `grid-column-start: 1;`            |
| `grid-column-end`  | 요소가 차지할 열의 끝 선을 지정합니다.                 | `grid-column-end: 4;`              |
| `span` 키워드      | 지정된 선으로부터 몇 칸을 차지할지를 설정. 열의 경우에도 동일하게 사용 | `grid-row: 2 / span 2;` (2칸 차지) |


<br>

- `grid-row: 1 / 4;` , `grid-column: 1 / 4;` 형식의 의미 :
    
    **“시작선 번호(start) / 끝선 번호(end)”** 형식을 사용하여 Grid 아이템이 어느 선부터 어느 선까지 차지할지를 정의한다. 
    
    예를 들어, `1 / 4`는 **1번 라인에서 시작해 4번 라인까지 영역을 차지**한다는 의미이다.
    
- `span` 사용법 설명 :
    
    `span` 키워드를 사용하면 특정 선부터 몇 칸을 차지하도록 간단히 설정할 수 있다.
    
     예를 들어, `grid-row: 2 / span 2;`는 2번 선부터 2칸을 차지하는 것을 의미한다.