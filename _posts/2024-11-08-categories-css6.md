---
title: "[CSS] 웹 폰트 적용 (Font-face, CDN)"
excerpt: "CSS에서 글꼴을 적용하는 방법"

categories:
  - css
tags:
  - [css]

permalink: /categories/css/6

toc: true
toc_sticky: true

date: 2024-11-09
last_modified_at: 2024-11-09
---

## 🦥 본문


웹 폰트 적용 방식은 웹 페이지에 기본적으로 제공되지 않는 글꼴을 사용하기 위한 방법이다.

웹 폰트 적용에는 두가지 방식이 있다.

## @font-face

- 로컬 서버에 폰트를 업로드 하여 사용자 지정 글꼴을 불러오는 방식이다.
- 서버에 있는 글꼴 파일을 사용자가 브라우저를 통해 다운로드하여 적용한다.

사용예시

```css
@font-face {
  font-family: '나눔고딕'; /* 사용할 글꼴 이름을 지정 */
  src: url('fonts/CustomFont.woff2') format('woff2'), /* 글꼴 파일 경로 및 형식 */
  font-weight: normal; /* 글꼴 두께 설정 */
  font-style: normal; /* 글꼴 스타일 설정 */
}

/* 위에서 설정한 'CustomFont'를 본문에 적용 */
body {
  font-family: 'CustomFont', sans-serif;
}

```

### CDN

- 외부 서버를 통해 원하는 폰트를 불러오는 방식이다.
- CDN을 제공해주는 사이트로는 구글, 어도비 등이 있다

사용예시

```css
<link href="https://fonts.googleapis.com/~~~~이하 주소" rel="stylesheet">

<style>
  body {
    font-family: 'Roboto', sans-serif;
  }
</style>

```

### 웹 폰트 로드 방식에 따른 장단점

| 구분         | 장점                                                         | 단점                           |
|--------------|--------------------------------------------------------------|--------------------------------|
| `@font-face` | 외부 서버에 비해 비교적 안정적으로 로드가 가능하다.           | 로컬 서버 트래픽 소모           |
| CDN 방식     | 적용이 간편함 / 트래픽 소모 없음                            | 외부 서버에 문제가 있을 경우 해결이 어렵다. |
