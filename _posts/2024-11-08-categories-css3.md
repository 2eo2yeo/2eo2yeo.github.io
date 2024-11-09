---
title: "[CSS] 단위"
excerpt: "CSS 단위에 대해서 알아보자"

categories:
  - css
tags:
  - [css]

permalink: /categories/css/3

toc: true
toc_sticky: true

date: 2024-11-09
last_modified_at: 2024-11-09
---

## 🦥 본문

- CSS에서 단위
    
    → width, height 처럼 너비, 높이, 간격의 속성을 가지고 있는 요소의 크기를 지정해줄 때 사용합니다
    

### 1. Pixel (px)

| 단위 | 설명 |
| --- | --- |
| Pixel (px) | 스타일 요소를 지정하는 기본적인 단위입니다. |
- 적용 예시

```html
<style>
     div.pixel{background-color: aquamarine; width: 400px; height: 200px;}
     div.pixel-child1{background-color: yellow; width: 50%;}
</style>
<body>
  <div class="pixel"> <!--parent-->
  <h5>pixel</h5>
  <div class="pixel-child1">pixel child element</div> <!--child-->
  </div>
</body>
```

❗부모tag에 스타일 단위가 적용되었을 경우 자식 tag는 그 단위를 넘어설 수 없는 것을 주의해야합니다 

- 적용 화면

![image.png](image.png)

→ 아쿠아마린 색상으로 너비 400px 높이 200px 적용 되었음

→ 자식 Tag에 백그라운드 비율 50%를 지정했을 때 부모 Tag의 50% 비율로 표현 되는 것을 알 수 있습니다.

---

### 2. Percent (%)

| 단위 | 설명 |
| --- | --- |
| percent (%) | 브라우저 화면 비율대로 나타내는 방법 |
- 적용 예시

```html
<style>
  div.percent{background-color: tomato; width: 100%; height: 200px;}
</style>
<body>
  <h2>percent(%)</h2>
    <div class="percent">percent</div>
</body>
```

- 적용 화면
    
    ![image.png](image%201.png)
    
    → 화면 비율의 100%로 적용된 모습 브라우저 창의 크기를 변동하게 되면 너비 또한 줄어드는 것을 알 수 있습니다. 
    

### 3. em / rem

| 단위 | 설명 |
| --- | --- |
| em | em 단위가 쓰여진 곳의 폰트 사이즈 배수 |
| rem | 문서의  기본 값이 16px의 배수 |

  * 1em, 2rem 등 앞에 숫자를 붙여 배수 사용이 가능합니다.

- 적용예시
    
    ```html
    <style>
       p.lorem{width: 500px;font-size: 1.2em;}
       strong{font-size: 2rem;}
    </style>
    <body>
        <h2>em/rem</h2>
        <p class="lorem">
        <strong>Lorem</strong>
        ipsum dolor sit amet consectetur adipisicing elit. Delectus laudantium voluptatum eligendi.
        Minus ab aperiam quibusdam laudantium rerum inventore eveniet a facilis,
        expedita cumque vero consequatur tenetur asperiores accusantium excepturi!</p>
    </body>
    ```
    

- 적용화면
    
    ![image.png](image%202.png)
    
    → p 태그 안의 다른 글자는 기본 폰트사이즈의 1.2배 (1.2em ) 된 형태
    
    → strong 태그 안의 폰트는 2rem (16px*3) 으로 나타난 모습입니다.