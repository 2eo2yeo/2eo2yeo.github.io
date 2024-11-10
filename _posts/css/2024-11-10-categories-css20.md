---
title: "[CSS] Order 속성"
excerpt: "flex와 grid 레이아웃에서 요소의 배치순서를 정해보자"

categories:
  - css
tags:
  - [css, css기초]

permalink: /categories/css/20

toc: true
toc_sticky: true

date: 2024-11-10
last_modified_at: 2024-11-10
---

## 🦥 본문

<br>


### order 속성 설명

- `order` 속성은 Flexbox와 Grid 레이아웃에서 요소의 **배치 순서를 조정**할 때 사용한다.
- 기본값은 `0`이며, 숫자를 변경하여 아이템의 순서를 자유롭게 재배치할 수 있다.
- 값이 작을수록 아이템이 앞에 배치되고, 값이 클수록 뒤로 밀린다.
- 반응형 디자인에서도 잘 활용된다.

<br>


### order 속성 사용 방법

- **기본 형식:** `order: <숫자>;`
- **배치 순서:** 작은 숫자가 먼저, 큰 숫자가 나중에 배치된다.
- **음수도 가능:** 음수를 사용해 아이템을 더 앞쪽에 배치할 수 있다.

<br>

### 예시코드

```css
.container {
    display: flex;
}

.text {
    order: 2;     /* image의 뒤에 배치 */
}

.image {          
    order: 1;     /* text 의 앞에 배치 */
}
```

<br>
<br>