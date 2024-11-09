---
title: "[CSS] 선택자의 우선 순위"
excerpt: "CSS 선택자에서 우선 선택되는 것을 알아보자 "

categories:
  - css
tags:
  - [css]

permalink: /categories/css/5

toc: true
toc_sticky: true

date: 2024-11-09
last_modified_at: 2024-11-09
---

## 🦥 본문


### CSS 우선순위

> CSS 우선순위의 원칙
> 
1. 동일한 선택자는 하단에 있는 선택자가 우선순위가 높다. 
    
    → 같은 선택자에 여러 스타일이 있을 때, 마지막에 작성된 스타일이 적용됩니다.
    
2. 구체적으로 선택할수록 우선순위가 높다.
    
    → 예를 들어, 태그보다 class 같은 속성이 우선 선택 된다.
    

### 예시코드

```css
<style>
	p { color: blue; }
</style>
```

여기서는 모든 `<p>` 태그가 **파란색**으로 표시됩니다.

```css
<style>
	p { color: blue; }
  .highlighted { color: green; }
</style>
```

`.highlighted` 클래스를 가진 `<p>` 태그는 **초록색**으로 표시됩니다. 클래스 선택자가 더 구체적이기 때문에 `p` 태그보다 우선 적용됩니다.

```css
<style>
	p { color: blue; }
  .highlighted { color: green; }
  p { color: purple; }
</style>
```

이 코드에서 같은 `p` 태그에 대해 나중에 선언된 스타일이 적용되어, 이제 **보라색**이 됩니다. 그러나 `.highlighted` 클래스는 여전히 **초록색**입니다