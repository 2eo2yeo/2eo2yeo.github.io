---
title: "[CSS] Overflow (스크롤바 생성 설정)"
excerpt: "overflow 설정으로 넘치는 글에 대해 스크롤바 설정을 해보자"

categories:
  - css
tags:
  - [css]

permalink: /categories/css/11

toc: true
toc_sticky: true

date: 2024-11-10
last_modified_at: 2024-11-10
---

## 🦥 본문

<br>
<br>


### CSS `overflow` 속성이란? 

`overflow` 속성은 요소의 콘텐츠(자식)가 컨테이너(부모) 크기를 넘어설 때 어떻게 처리할지를 결정하는 CSS 속성이다. 주로 스크롤 처리나 콘텐츠 자르기 등을 설정할 때 사용합니다.

<br>
<br>


### 1. `overflow` 속성

| 속성 값             | 설명                                                                                      |
|---------------------|-------------------------------------------------------------------------------------------|
| `hidden`           | 넘치는 부분이 잘리고, 스크롤바는 나타나지 않는다.                                          |
| `scroll`           | 스크롤바가 항상 표시됨. 넘치는 않은 부분도 스크롤 영역이 나타난다.                         |
| `auto`             | 넘칠 때만 스크롤바가 나타난다.                                                             |
| `overflow-x`, `overflow-y` | 방향을 지정하고, 해당 방향으로 넘치는 부분에 대해서만 overflow 속성을 지정한다.<br> `overflow-x` (가로)와 `overflow-y` (세로) |


<br>
<br>

- **예시 코드**
    
    ```css
     <head>
     <style>
        .container {
          width: 300px;
          height: 100px;
          border: 1px solid #000;
          margin-bottom: 20px;
        }
        .visible { overflow: visible; }
        .hidden { overflow: hidden; }
        .scroll { overflow: scroll; }
        .auto { overflow: auto; }
      </style>
    </head>
    <body>
         <h3>overflow: visible</h3>
         <div class="container visible">
    	  이 콘텐츠는 overflow가 visible입니다. 
          넘쳐도 보입니다.
        </div>
    
        <h3>overflow: hidden</h3>
        <div class="container hidden">
            이 콘텐츠는 overflow가 hidden입니다. 
            넘친 부분은 잘립니다.
        </div>
    
        <h3>overflow: scroll</h3>
        <div class="container scroll">
            이 콘텐츠는 overflow가 scroll입니다.
            스크롤바가 항상 나타납니다.
        </div>
    
        <h3>overflow: auto</h3>
         <div class="container auto">
         이 콘텐츠는 overflow가 auto입니다. 
         넘칠 때만 스크롤바가 표시됩니다.
         </div>
    </body>
    
    ```


<br>
<br>