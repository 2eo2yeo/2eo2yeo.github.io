---
title: "[CSS] 색상"
excerpt: "style로 색상을 표현하는 방법"

categories:
  - css
tags:
  - [css]

permalink: /categories/css/1

toc: true
toc_sticky: true

date: 2024-11-08
last_modified_at: 2024-11-08
---

## 🦥 본문



### 1. 색상이름

 :  색상 이름을 직접 입력하여 설정

```html
 <head>
 <style> p.color-name{color: green;} </style>
 </head>
 <body>
    <p class="color-name">CSS Color name</p>
 </body>
```

### 2. RGB

: RGB 값으로 설정

- R(Red), G(Green) B(blue) 색상 값을 통해 색상을 지정하는 방법.
- 포토샵, 그림판의 스포이드 기능을 활용하면 적용이 쉽다.

```html
 <head>
 <style>p.color-rgb{color: rgb(160,123,29);}</style>
 </head>
 <body>
    <p class="color-rgb">CSS RGB name</p>
 </body>
```

### 3. RGBA

: RGB 값에 알파(Alpha)값을 더해 투명도를 설정하는 방법

- rgba 속성 값의 네번째 자리에 알파 값이 위치한다.
- 투명도는 0~1사이의 숫자로 설정이 가능하다.

```html
 <head>
 <style> p.color-rgba{color: rgba(189,48,41,1);}</style>
 </head>
 <body>
    <p class="color-rgba">CSS RGBA color</p>
 </body>
```

### 3. 헥스(HEX)

: hex 값으로 색상을 표현하는 방법 

- hex란❓ : 16 진수를 뜻함, 색상을 6자리의 숫자로 표현한다.

```html
 <head>
 <style>p.color-hexa{color: ;#f0aefe;}</style>
 </head>
 <body>
    <p class="color-hexa">CSS #hexa color</p>
 </body>
```
