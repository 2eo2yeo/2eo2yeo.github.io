---
title: "[CSS] Display 디스플레이 속성"
excerpt: "display 속성으로 요소를 배치하는 방법에 대해 알아보자"

categories:
  - css
tags:
  - [css]

permalink: /categories/css/10

toc: true
toc_sticky: true

date: 2024-11-10
last_modified_at: 2024-11-10
---

## 🦥 본문

<br>
<br>

### display 속성이란?

> 브라우저 화면에 어떻게 디스플레이(요소, 레이아웃을 어떻게 배치) 할지 결정하는 속성이다.
태그가 가지고 있는 디폴트 값인 **인라인 속성을 → 블록 속성** 으로 **변경**하거나
반대로 **블록 속성 → 인라인 속성**으로 **변경**시켜주는 CSS 속성이다.
> 

<br>
<br>

### 대표적인 태그들의 display 속성 구분

| 구분        |                                                                                                                                                      |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| 인라인      | `a` `span` `input` `label` `i` `b` `em` `strong`                                                                                                    |
| 블록        | `h1` `h2` `p` `ul` `ol` `dl` `li` <br> `table` `thead` `div` `header` <br> `section` `article` `aside` `footer` <br> `nav` `figure` `figcaption`    |
| 인라인-블록 | `img` `video`                                                                                                                                        |


<br>
<br>


### 1. `display: block`

- **설명**: 블록 레벨 요소로, 가로 전체를 차지하며  항상 새 줄에서 시작합니다.
- **특징**:
    - 가로 전체를 사용
    - 다음 요소는 항상 새 줄에서 시작
    - width, height 속성 지정이 가능하다.
- **사용 예시**:
    
    ```css
    
    div {
      display: block;
    }
    
    ```

<br>
<br>


### 2. `display: inline`

- **설명**: 인라인 요소로, 컨텐츠의 크기만큼만 공간을 차지한다
- **특징**:
    - 컨텐츠 크기만큼만 공간 차지
    - 다른 요소와 같은 줄에 배치됨 (줄바꿈이 되지 않음)
    - width, height 지정이 불가능하다.
- **사용 예시**:
    
    ```css
    span {display: inline;}
    ```
    

<br>
<br>

### 3. `display: inline-block`

- **설명**: 인라인 요소처럼 한 줄에 배치되지만, 블록 요소처럼 너비와 높이를 설정할 수 있습니다.
- 인라인, 블록 요소의 특성을 합친 하이브리드 속성이
- **특징**:
    - 블록 요소처럼 크기 지정 가능
    - 다른 인라인 요소와 같은 줄에 배치
- **사용 예시**:
    
    ```css
    button { display: inline-block;
    ```
    

<br>
<br>

### 4. `display: none`

- **설명**: 요소를 화면에서 완전히 숨깁니다. 해당 요소는 페이지 레이아웃에서 완전히 제외되며, 공간을 차지하지 않습니다.
- **특징**:
    - 요소가 화면에 표시되지 않고 크기 차지도 하지 않음
    - **차이점**: `visibility: hidden`은 공간은 차지하지만 보이지 않음, `opacity: 0`은 투명하지만 공간을 차지
- **사용 예시**:
    
    ```css
    .hidden {display: none;
    ```

<br>
<br> 

### 5. `display: table`, `display: table-cell`

- **설명**: 요소를 테이블과 테이블 셀처럼 배치할 때 사용합니다.
    - `table`: 테이블의 역할을 하는 컨테이너
    - `table-cell`: 테이블 셀(td) 처럼 배치되는 요소
- **특징**:
    - 가로 정렬을 쉽게 처리할 수 있음
- **사용 예시**:
    
    ```css
    .container {display: table;}
    
    .item {display: table-cell;}
    ```


