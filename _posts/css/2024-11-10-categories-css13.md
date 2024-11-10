---
title: "[CSS] 박스 모델의 기본 개념"
excerpt: "css 박스 모델에 대해서 알아보자"

categories:
  - css
tags:
  - [css]

permalink: /categories/css/13

toc: true
toc_sticky: true

date: 2024-11-10
last_modified_at: 2024-11-10
---

## 🦥 본문

<br>

### CSS Box 모델: 웹 요소의 기본 구조 및 구성 요소

CSS Box 모델은 웹 요소의 크기와 배치할 때 필수로 숙지해야 할 개념이다. 

모든 HTML 요소는 아래의 사각형의 박스 모델로 구성된다.

![box모델설명](/assets/images/posts_img/css/css_images13.png)

<br>
<br>

### 박스모델 구성 요소 설명

| 속성      | 설명                                                          | 예제                    |
|-----------|---------------------------------------------------------------|-------------------------|
| `content` | 요소의 내용이 표시되는 영역으로 텍스트, 이미지가 위치한다.     | `width: 200px;`         |
| `padding` | content 주변, Border 안쪽 여백이다. 기본적으로 투명하다.       | `padding: 10px;`        |
| `border`  | Padding 바깥에 위치한다. 쉽게 말하면 테두리이다.               | `border: 2px solid black;` |
| `margin`  | Border 바깥의 여백이다. 기본적으로 투명하다.                   | `margin: 20px;`         |

<br>
<br>

### Box 모델 예제 코드

```css
.box {
  width: 200px;
  padding: 10px;
  border: 2px solid black;
  margin: 20px;
}
```


<br>
<br>