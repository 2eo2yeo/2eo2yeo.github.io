---
title: "[CSS] List-Style 목록 스타일"
excerpt: "목록에 순번, 불릿 스타일을 지정해보자"

categories:
  - css
tags:
  - [css]

permalink: /categories/css/9

toc: true
toc_sticky: true

date: 2024-11-09
last_modified_at: 2024-11-09
---

## 🦥 본문

목록 태그의 목록 표시 모양을 변형 할 수 있다.

| 속성             | 설명                                                                                                                                                    |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| list-style-type  | `disc`, `circle`, `square` 등이 있다.                                                                                                                   |
| :none            | 목록 표시를 안보이게 하고 싶을 때 사용                                                                                                                   |
| 기타             | - 목록표시를 `-`(하이픈)로 하고 싶은 경우 `''` (따옴표)를 사용하여 적용 가능  <br> - 이모지의 유니코드를 넣으면 이모지 사용도 가능하다                              |



```css
<style>
  ol li {list-style-type: decimal;}
  ol li {list-style-type: '-';}
</style>
```


