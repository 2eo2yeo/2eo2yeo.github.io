---
title: "[CSS] 글꼴, 서체 스타일링"
excerpt: "CSS를 사용하여 글꼴에 스타일을 주자"

categories:
  - css
tags:
  - [css]

permalink: /categories/css/7

toc: true
toc_sticky: true

date: 2024-11-09
last_modified_at: 2024-11-09
---

## 🦥 본문



### 1. **font-family**: 글꼴 종류 설정

`font-family`는 텍스트에 적용할 글꼴을 지정하는 속성입니다. 하나 이상의 글꼴을 나열하여 지정할 수 있으며, 만약 첫 번째 글꼴이 사용자 시스템에 없으면 다음 글꼴로 넘어갑니다. 
<br>
```css
<style>
  body {
    font-family: 'Helvetica', 'Arial', sans-serif;}
</style>
```
- 차례대로 우선순위가 높은 폰트를 나열하여 지정한다.
    - 위 코드에서, 브라우저는 먼저 'Helvetica'를 적용하려 시도하고, 없으면 'Arial'을 사용하며, 두 글꼴 모두 없을 경우 os 기반 기본폰트인 sans-serif 글꼴을 사용한다.
- 폰트명이 영어가 아니거나, 공백(스페이스)이 있을 경우 폰트명에 ‘따옴표’ 로 감싸준다.

<br>
<br>
<br>

### 2. **font-size**: 글꼴 크기 설정

- `font-size`는 텍스트의 크기를 지정합니다. px, em, rem, % 등의 단위를 사용할 수 있으며, 상황에 따라 적절한 단위를 선택해야 한다.

```css
<style>
  p {font-size: 16px; /* 픽셀 단위 */}
</style>
```
<br>
<br>
<br>

### 3. **font-weight**: 글꼴 두께 설정

`font-weight`는 글꼴의 두께를 설정하는 속성입니다. 일반적으로 **normal**과 **bold**로 두께를 구분하지만, 숫자를 넣어 조정이 가능하다.

```css
<style>
  h1 {font-weight: bold; /* 굵게 */}
  p {font-weight: 300; /* 얇게 */}
</style>

```
<br>
<br>
<br>

### 4. **font-style**: 글꼴 스타일 설정

`font-style` 속성은 글꼴의 기울임꼴(이탤릭체) 여부를 설정합니다. 보통 **normal**, **italic**, **oblique**의 세 가지 값을 사용할 수 있습니다.

```css
<style>
  em {font-style: italic; /* 이탤릭체 적용 */}
</style>
```

- `italic`은 글꼴에서 제공하는 기울임꼴을 사용하고, `oblique`는 글꼴을 강제로 기울이는 차이가 있습니다

<br>
<br>
<br>

### 5. **text-align**: 텍스트 정렬

`text-align` 속성은 텍스트를 left(왼쪽),  right(오른쪽), center(가운데), justify(양쪽) 정렬할 수 있게 합니다.

- inline 속성을 가진 태그는 text-align이 적용 되지 않는다.

```css
<style>
  h2 { text-align: center; /* 중앙 정렬 */}
</style>
```
<br>
<br>
<br>
### 6. text-decoration  글자 장식

`text-decoration` 속성은 텍스트에 밑줄, 취소선, 윗줄 등의 스타일을 적용할 수 있는 속성이다. 

- text-decoration의 주요 속성
    
    
| none                    | `<a>`는 기본적으로 밑줄이 있다 → 밑줄을 없앨 때 주로 사용 |
|-------------------------|------------------------------------------------------|
| text-decoration-style (테두리) | `solid`(실선), `dotted`(도트선), `double`(이중실선), `dashed`(약간 긴 점선)으로 설정이 가능 |
| text-decoration-line    | `underline`(밑줄), `overline`(윗줄), `line-through`(가로줄) 등 설정 |

```css
<style>
  a {text-decoration: underline; /* 밑줄 */ }
  del {text-decoration: line-through; /* 취소선 */}
</style>
```
<br>
<br>
<br>

### 7. word-spacing, letter0-spacing 글자 간격 띄우기

- letter-spacing(글자 한글자 한글자 사이의 간격 지정), word-spacing(단어와 단어사이 간격을 지정)이 가능하다.

```css
<style>
  h1 {word-spacing: 10px;} /* 단어와 단어사이 띄우기 */
</style>
```
<br>
<br>
<br>

### 8. Text-trasnsform 글자 변형
    
| 속성        | 설명             |    
|------------|-------------------|  
| :uppercase | 모두 대문자로 변형 |
| :lowercase | 모두 소문자로 변형 |
| :capitalize| 첫 글자만 대문자   |


```css
<style>
  .uppercase {text-transform: uppercase;}    /* 모두 대문자 */
  .lowercase {text-transform: lowercase;}      /* 모두 소문자 */
  .capitalize {text-transform: capitalize;}   /* 첫글자만 대문자 */ 
</style>
```
<br>
<br>
<br>

### 9. text-indent 글자 들여쓰기

- 양수 값 입력 : 들여쓰기 / 음수 값 입력 : 내어쓰기
- 블록 요소에서 제대로 작동된다.
<br>
<br>
<br>

### 10. Line-height

- text-height 는 텍스트 줄 사이 거리를 설정하는 속성이다, 행의 높이를 지정한다.