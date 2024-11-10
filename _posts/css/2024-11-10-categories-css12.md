---
title: "[CSS] Background 속성"
excerpt: "요소의 배경을 변경해보자"

categories:
  - css
tags:
  - [css]

permalink: /categories/css/12

toc: true
toc_sticky: true

date: 2024-11-10
last_modified_at: 2024-11-10
---

## 🦥 본문

<br>

### CSS `background` 속성이란

`background` 속성은 요소의 배경을 설정하는데 사용된다. 

이 속성을 통해 배경 색상, 이미지, 반복 및 위치 등을 손쉽게 지정할 수 있다.

### 1. `background` 관련 주요 속성

| 속성                  | 설명                                                                                       | 사용법 예제                                             |
|-----------------------|------------------------------------------------------------------------------------------|---------------------------------------------------------|
| `background-color`    | 배경의 색상을 설정합니다. HEX, RGB, HSL 값 등을 사용할 수 있습니다.                        | `background-color: #f0f0f0;`<br>`background-color: rgba(255, 255, 255, 0.5);` |
| `background-image`    | 배경에 이미지를 설정합니다. URL로 경로를 지정합니다.                                       | `background-image: url('image.jpg');`                   |
| `background-repeat`   | 배경 이미지의 반복 여부를 설정합니다.<br>옵션: `repeat` (가로세로 반복), `no-repeat` (반복 없음),<br>`repeat-x` (가로 반복), `repeat-y` (세로 반복) | `background-repeat: no-repeat;`                         |
| `background-position` | 배경 이미지의 위치를 지정합니다.<br>옵션: `left`, `center`, `right`, `top`, `bottom` 외에 px, %, em 단위 사용 가능 | `background-position: center;`<br>`background-position: 20px 30px;` |
| `background-size`     | 배경 이미지의 크기를 설정합니다.<br>옵션: `cover` (가로크기에 맞춰 늘림), `contain` (세로 크기에 맞춰 늘림), 특정 크기(px, %) 지정 | `background-size: cover;`<br>`background-size: 100px 50px;` |
| `background-attachment` | 스크롤 시 배경 이미지의 고정 여부를 설정합니다.<br>옵션: `scroll`, `fixed`, `local` | `background-attachment: fixed;`                         |

<br>
<br>


### 2. `background`  단축 속성 (background stack)

`background`는 여러 속성을 한 번에 설정할 수 있다.

- 주의할 점 : **배경의 위치, 배경 사이즈** 두 속성 사용 시에 반드시 위치를 먼저 써야하고 **슬래시(/)** 로 구분해야함

```css
div {background: url('image.jpg') no-repeat center/cover #ffcc00;}
```

<br>
<br>



### 3. 예시 코드

```css

		.color {
      background-color: #ffcc00; /* 배경 색상 */
    }
    .image {
      background-image: url('https://example.com/image.jpg'); /* 배경 이미지 URL */
      background-size: cover; /* 배경 이미지 크기 */
      background-position: center; /* 가운데 정렬 */
    }
```

<br>
<br>