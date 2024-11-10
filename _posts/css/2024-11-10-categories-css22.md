---
title: "[CSS] 반응형 웹 / 미디어쿼리 / 반응형 단위"
excerpt: "반응형 웹에대한설명, 미디어쿼리 사용법과, 반응형에서 쓰이는 단위에 대해 알아보자"

categories:
  - css
tags:
  - [css, css기초]

permalink: /categories/css/22

toc: true
toc_sticky: true

date: 2024-11-10
last_modified_at: 2024-11-10
---

## 🦥 본문

<br>

### 반응형 웹에 대한 설명

css만으로 다양한 기기의 너비에 맞춰 컨텐츠의 너비와 배치를 조절하여 최적화 함.

<br>

### Media query

`@media`로 시작하는 미디어 쿼리를 이용 하여 설정 가능하다.

`html`의 `head` 태그에 `viewport`설정이 필수 

| media 속성 | 설명                                                 |
|------------|------------------------------------------------------|
| `screen`   | 화면(컴퓨터 모니터)용 스타일 시트를 정의한다.       |
| `print`    | 프린트(인쇄)용 화면의 스타일시트를 정의한다.        |
| `all`      | 화면과 인쇄 출판용 스타일 시트를 정의한다.          |


<br>

### Media query  예시 코드

```css
@media screen and (min-width:769px)
            /*769이상 화면에서 적용*/
  {
  #wrapper {
  background-color: silver;}
  }
            
@media screen and (max-width:768px) 
           /*768 이하 화면에서 적용*/
 {
 #wrapper {
  background-color: blue;
  color: white}
  }
```

<br>

### 하위 속성 비율 계산식

- max-width 등의 속성이 부모 태그에만 적용이 되기 때문에 하위 속성들은 아래의 계산식으로 비율을 계산해서 설정해주면 된다.

> 작은 값 / 큰 값 (기준 값 ) * 100% = 하위 속성 비율 값
> 
<br>

```css
 @media screen and (max-width:960px) {  
/* 화면이 960px 이하이면 무조건 width를 100퍼 */
  #wrapper {
            width: 100%;    
            /* 100퍼의 기준은 960px */
            }
  aside {
          width: 36.45%;    
          /*    350px/960px*100%=36.45%
  350px로 픽스된 것이 화면이 줄었을 때 안잘리도록 비율값 조정 */
        }

  article {
            width: 57.29%;
          }
    }
```

<br>

### 반응형 CSS 단위

| 단위        | 종류                          |
|-------------|-------------------------------|
| 고정 단위   | `px`, `rem`, `em`            |
| 비율 단위   | `%`, `vw`, `vh`              |

    
    : 어떤 디스플레이 화면을 사용하는지와 상관없이 **고정된 값으로 표시**
    
- 비율 단위 (상대 단위)
    
    : 미디어쿼리와 함께 사용하면 비율에 따라 **유연하게 사용할 수 있음**


<br>
<br>