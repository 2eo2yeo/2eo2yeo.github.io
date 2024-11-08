---
title: "[CSS] (Cascade Style Sheet) 문법"
excerpt: "style로 색상을 표현하는 방법"

categories:
  - CSS
tags:
  - [css]

permalink: /css/2

toc: true
toc_sticky: true

date: 2024-11-07
last_modified_at: 2024-11-07
---

## 🦥 본문

> HTML이 뼈대라면, CSS는 뼈대에 옷을 입혀주는 개념이다
> 

### CSS 문법 구조

![image.png](/assets/images/posts_img/css/css_image1.png)

- 선택자의 종류 : id(#), class(.), 경로(부모/자식 관계..)

### CSS 문법

1. **Inline Style**
    
    : HTML 태그에 직접 스타일을 적용하는 방법이다.
    
    ```html
    <li style="color: red ;">Inline style</li>
    ```
    

1. **Internal Style**
    
    : Style 태그에 스타일을 적용하는 방법이다. 
    
    ```html
    <head>
      <style> li.internal {color: green;} </style>	
    </head>
    <body>
      <li class="internal">internal style</li>
    </body>
    ```
    
    - 가장 많이 사용 되는 CSS 문법이다.
    - <head>에 <style>태그를 입력하여  <Body>에서 도출되도록 한다.
    
2. **External  style**
    - 별도의 CSS파일을 생성하고 해당 파일을 HTML파일과 연결하는 방법이다.
    - 주의 : CSS파일은 단독으로 쓸 수 없으며 HTML 파일과 연동해야 사용이 가능하다.
    - <link>로 스타일 시트와 연동이 가능하다.
        - 예시 : syntax.css 파일과의 연동
    
    ```html
      <link rel="stylesheet" type="text/css" herf="css/syntax.css"> </link>
    ```