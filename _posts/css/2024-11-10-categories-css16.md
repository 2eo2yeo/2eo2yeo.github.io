---
title: "[CSS] 레이아웃 - Position"
excerpt: "요소의 위치를 조정해보자"

categories:
  - css
tags:
  - [css, css기초]

permalink: /categories/css/16

toc: true
toc_sticky: true

date: 2024-11-10
last_modified_at: 2024-11-10
---

## 🦥 본문

<br>


### postion 속성 설명

`position` 속성은 요소의 위치를 정할 때 사용하는 CSS 속성입니다. 이 속성은 다양한 값을 통해 요소를 **정확한 위치**에 배치하거나, **다른 요소와의 관계를 조정**하는 데 사용됩니다.

- 특징 : 포지션으로 위치 지정하는 태그는 어디에 있든 상관이 없다.

<br>

### `position` 속성의 값과 기능



| 값           | 설명                                                                                                 |
|--------------|------------------------------------------------------------------------------------------------------|
| `static`     | 기본값으로, 요소는 HTML 문서의 기본 흐름에 따라 위치됩니다. 배치가 불가능하다.                       |
|              | `top`, `bottom`, `left`, `right` 속성을 사용할 수 없습니다.                                          |
| `relative`   | 설정만으로 위치와 크기가 변하진 않는다.                                                              |
| (상대적)     | `relative` 설정한 것을 기준으로 **기본 위치에서** 오프셋하여 배치한다.                               |
|              | `top`, `bottom`, `left`, `right` 속성으로 위치를 조정할 수 있습니다.                                  |
|              | → 위치 조정 시 다른 요소들의 위치에 영향을 주지 않는다.                                               |
| `absolute`   | 가장 가까운 **부모 요소**를 기준으로 배치됩니다.                                                     |
| (절대 값)    |                                                                                                      |
| `fixed`      | **화면(Viewport) 전체**를 기준으로 절대 위치에 배치됩니다. 스크롤해도 위치가 고정됩니다.              |
|              | 주로 네비게이션 바에 사용됩니다.                                                                     |
| `sticky`     | 요소가 특정 위치에 도달하기 전에는 **기본 위치에** 있다가, 특정 지점에 도달하면 고정되는 속성입니다. |
|              | `top`, `bottom`, `left`, `right`와 함께 설정할 수 있습니다.                                          |


### **1. relative 예제**

- 기본 위치에서 이동

```html
<style>
  .relative-box {
    position: relative;
    top: 20px;
    left: 30px;
    background-color: lightblue;
  }
</style>

<div class="relative-box">Relative Position</div>

```

<br>

### **2. Absolute 예제**

- 가장 가까운 부모를 기준으로 절대 위치

`position: relative;`를 기준으로 `absolute` 속성이 적용된 하위 요소(`.absolute-box`)가 **부모 요소**인 회색 박스를 기준으로 내부에서 상단10px, 우측기준 20px  만큼 이동하였다.

<br>


```html
<style>
  .parent {
    position: relative;
    width: 300px;
    height: 200px;
    background-color: lightgrey;
  }
  .absolute-box {
    position: absolute;
    top: 10px;
    right: 20px;
    background-color: pink;
  }
</style>

<div class="parent">
  <div class="absolute-box">Absolute Position</div>
</div>
```

<br>

### **3. Fixed 예제**

- 화면에 고정된 위치 → 배치한 화면 한쪽에 계속 고정된다.

```html
<style>
  .fixed-box {
    position: fixed;
    bottom: 10px;
    right: 10px;
    background-color: lightgreen;
    width: 150px;
    height: 50px;
  }
</style>

<div class="fixed-box">Fixed Position</div>
```

<br>

### **4. Sticky 예제**

- 스크롤할 때 특정 위치에 고정

```html
<style>
  .sticky-box {
    position: sticky;
    top: 0;
    background-color: yellow;
  }
</style>

<div class="sticky-box">Sticky Position</div>
<p>스크롤할 때 이 요소가 고정됩니다.</p>

```

<br>
<br>