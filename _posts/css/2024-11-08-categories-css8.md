---
title: "[CSS] Vertical align 수직정렬"
excerpt: "CSS에서 요소를 수직정렬 하는 방법 "

categories:
  - css
tags:
  - [css]

permalink: /categories/css/8

toc: true
toc_sticky: true

date: 2024-11-09
last_modified_at: 2024-11-09
---

## 🦥 본문


### `vertical-align`
: 인라인 요소들이 연달아 나열 될 때 **뒤따라 오는 인라인 요소의 높이를 수직으로 조절** 할 때 사용한다.

먼저 나온 태그를 기준으로 정렬된다.



### 적용예시

```css
<style>
  .top {vertical-align: top;}  /*옆의 태그 윗쪽을 기준으로 정렬*/
  .middle {vertical-align: middle;} /*옆의 태그 가운데를 기준으로 정렬*/
  .bottom {vertical-align: bottom;} /*옆의 태그 아래쪽을 기준으로 정렬*/
</style>
```

