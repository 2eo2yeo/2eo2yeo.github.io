---
title: "[CSS] 레이아웃 -  Z-INDEX"
excerpt: "요소들이 겹칠 때 어떤 순서로 보여질지 지정해보자"

categories:
  - css
tags:
  - [css, css기초]

permalink: /categories/css/17

toc: true
toc_sticky: true

date: 2024-11-10
last_modified_at: 2024-11-10
---

## 🦥 본문

<br>

### Z-index란?

`z-index`는 CSS에서 요소가 쌓이는 순서를 지정하는 속성으로, 특히 요소들이 겹칠 때 어떤 요소가 위에 표시될지를 결정합니다. 주로 `position` 속성이 `absolute`, `relative`, `fixed`, 또는 `sticky`로 설정된 요소에 적용됩니다.

- 특징 : index는 수치가 높은 것이 가장 우선순위로 앞에 온다

<br>

**코드예시와 설명**

```html
    <style>
        div {
            width: 150px;
            height: 150px;
            color: white;
        }
        .red {background-color: red;}
        .blue {background-color: blue;}
        .green {background-color: green;}

        /* z-index는 수치가 높은 것이 가장 우선순위로 앞에 배치된다. */
        .child1 {
            position: relative;
            top: 20px;
            left: 50px; 
            z-index: 1;}
        .child2 {
            position: relative;         /* child1 기준으로 배치됨 */
            left: 20px;
            z-index: 2;}
        .child3 {
            position: relative;         /* child2 기준으로 배치됨 */
            top: -230px;
            left: 10px;
            z-index: 3;}
    </style>

</head>
<body>
    <h1>Z-index</h1>
    <div class="red child1">child 1</div>
    <div class="blue child2">child 2</div>
    <div class="green child3">child 3</div>
</body>
```

<br>

### 적용화면

![z-index결과](/assets/images/posts_img/css/css_image17.png)
<br>
<br>