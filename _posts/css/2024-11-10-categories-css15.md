---
title: "[CSS] 레이아웃 - Float"
excerpt: "요소를 원하는 위치에 띄워보자"

categories:
  - css
tags:
  - [css, css기초]

permalink: /categories/css/15

toc: true
toc_sticky: true

date: 2024-11-10
last_modified_at: 2024-11-10
---

## 🦥 본문

<br>

### 1. float 속성 설명

`float` 은 ‘뜨다’ 라는 뜻을 가지고 있으며

CSS에서`float`속성은 요소를 원하는 위치에 배치하여 떠있게, 부유하도록 하는속성이다.

기본적으로 이미지를 띄워서 텍스트와 함께 배치할 때 쓰거나, 레이아웃 영역을 지정할 때 사용된다.

- 특징 : float의 특징은 한 태그에만 float을 지정하고 싶어도 뒤의 태그들이 다 같이 영향을 받는다. 
예를들어, float : left  를 사용할 경우 후에 나오는 모든 요소가 왼쪽으로 따라붙게 된다.

<br>

### 2. float의 속성값

| 속성 값 | 설명 |
| --- | --- |
| `inherit` | 부모 요소로부터 상속함 |
| `left` | 요소를 **왼쪽에** 띄운다. |
| `right` | 요소를 **오른쪽에** 띄운다 |
| `none` | **기본값**으로, 요소를 띄우지 않고 문서의 기본 흐름대로 배치한다. |

<br>

### 3. 응용 : `clear` 속성 사용

 `float` 속성이 적용된 요소 다음에 오는 요소가 `float`의 영향을 받지 않도록 할 때 `clear` 속성을 사용한다.

| 속성 값   | 설명                                                                 |
|-----------|----------------------------------------------------------------------|
| `left`    | 요소의 왼쪽에 떠 있는 (floating) 요소가 없도록 합니다.               |
| `right`   | 요소의 오른쪽에 떠 있는 (floating) 요소가 없도록 합니다.             |
| `both`    | 요소의 양쪽(왼쪽과 오른쪽)에 떠 있는 요소가 없도록 합니다.           |
| `none`    | 기본값. 요소가 `clear` 없이 배치되며, `float`의 영향을 받습니다.     |

<br>

### 예시 코드

```css
<style>
  .box-group > div {
            width: 100px;
            height: 100px;
            background-color: aquamarine;
            text-align: center;  
            float: left; 
            margin: 10px;
            border-radius: 10px;         
        }
        div.box-group > p { clear: both;}
</style>
<body>
<div class="box-group">
   <div>box1</div>
   <div>box2</div>
   <div>box3</div>
   <p>
     Lorem ipsum dolor sit amet consectetur adipisicing elit. 
     Expedita voluptate dolor vero doloribus omnis quasi, commodi est 
     placeat itaque facilis delectus iusto cumque quaerat maiores deleniti 
     rem aut assumenda facere.
        </p>
</body>
```

<br>

### 적용 화면

→ `float`이 적용된 `div` 는 왼쪽으로 정렬되었고, clear를 이용해 float 적용을 없애준 p태그는 정상적인 문서의 흐름으로 배치되었다. 

![float속성 결과](/assets/images/posts_img/css/css_images15.png)

<br>
<br>