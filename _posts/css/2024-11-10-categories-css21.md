---
title: "[CSS] Grid 트랙 함수"
excerpt: "grid와 함께 사용되는 repeat, minmax, auto-fill, auto-fill 함수"

categories:
  - css
tags:
  - [css, css기초]

permalink: /categories/css/21

toc: true
toc_sticky: true

date: 2024-11-10
last_modified_at: 2024-11-10
---

## 🦥 본문

<br>



### grid 트랙 함수 정리

| 함수           | 사용 목적                                                             | 사용 예시                                             |
|----------------|-----------------------------------------------------------------------|------------------------------------------------------|
| `repeat()`     | 동일한 크기의 열/행을 반복할 때                                       | `grid-template-columns: repeat(3, 1fr);`             |
| `minmax()`     | 요소의 최소 및 최대 크기를 설정하여 유동적 크기 조정                  | `grid-template-columns: minmax(200px, 1fr);`        |
| `auto-fill`    | 가용 공간을 최대한 채우기 위해 열/행을 자동으로 생성하고 빈칸을 남긴다. | `grid-template-columns: repeat(auto-fill, 150px);`   |
| `auto-fit`     | 공간에 맞춰 크기를 유동적으로 조정하며 빈 칸이 없도록 유지             | `grid-template-columns: repeat(auto-fit, minmax(100px, 1fr));` |

<br>

### 각 함수의 사용 예시와 단위 설명

1`fr`: 가용공간의 1등분을 의미한다.

예를 들어, `grid-template-columns: 1fr 1fr 1fr;`로 설정하면, 각 열은 **가로폭의 1/3**을 차지하게 된다. 크기를 width 처럼 고정된 크기를 설정하는 것 보다 유연하게 크기를 지정할 수 있다.


<br>

### 1. `repeat()`

- 동일한 크기의 열/행을 여러 번 설정할 때 사용.
- **예시:** `grid-template-columns: repeat(3, 1fr);`
    
    → 동일한 크기의 열을 3개 생성. 패턴이 반복될 때 코드를 간결하게 작성 가능
    

### 2. `minmax()`

- 최소/최대 크기를 지정하여, 요소가 특정 크기 범위에서 유동적으로 조정되도록 할 때 사용.
- **예시:** `grid-template-columns: minmax(200px, 1fr);`
- → 각 열의 최소 크기는 최소 200px로 고정하고, 화면이 넓을 때는 1fr까지 확장

### 3. `auto-fill`

- 가용 공간을 채울 수 있을 때까지 열/행을 추가하며, 공간이 남으면 빈 칸으로 채움.
- **예시:** `grid-template-columns: repeat(auto-fill, 150px);`
    
    → 150px 크기의 열이 화면 가로폭을 채울 때까지 자동으로 추가. 
    빈 칸이 남으면 칸이 유지됨
    

### 4. `auto-fit`

- `auto-fill`과 유사하지만, 빈 공간을 남기지 않고 크기를 자동 조정하여 균일하게 맞춤.
- **예시:** `grid-template-columns: repeat(auto-fit, minmax(100px, 1fr));`
    
    →열이 최소 100px 이상이지만 화면 공간에 맞춰 확장. 빈 칸이 남으면 열 크기를 늘려 레이아웃을 균형있게 맞춘다.

<br>
<br>