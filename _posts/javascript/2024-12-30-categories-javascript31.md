---
title: "[JavaScript] 모듈 내보내고 불러오기(import, export), 모듈 별칭 사용(AS)"
excerpt: "모듈 내보내기와 불러오기를 예제를 통해 알아보자, 파일에서 별칭으로 사용하기"

categories:
  - javascript
tags:
  - [javascript, 자바스크립트]

permalink: /categories/javascript/31

toc: true
toc_sticky: true

date: 2024-12-30
last_modified_at: 2024-12-30
---

## 🦥 본문

<br>

### 자바스크립트에서 export 와 import 란?

- 정의
    - `export`와 `import`는 코드를 모듈화하여, 자바스크립트 코드를 여러 파일과 폴더에 나누어 작성하고 **내보내고 불러와서** 사용이 가능하다.
- 역할
    - 코드의 **재사용성**과 **유지보수성을** 크게 향상시킬 수 있다.
    - 모듈은 독립적인 스코프를 가지며, 변수 충돌을 방지한다.

---

### `export`: 모듈 내보내는 방법

- **역할**: 함수를 다른 파일에서도 사용할 수 있도록 **내보낸다**.
- **사용법**: 함수나 변수 앞에 `export`를 붙이면 해당 코드를 다른 파일에서 사용할 수 있다. 
여러 함수를 한꺼번에 내보낼 수도 있다.
- export.js 파일  ⇒  함수들만 별도 작성
    
    ```jsx
    // 기본 구구단 출력 함수
    export function gugudan() {...}
    
    // 특정 단만 출력하는 함수
    export function singleGugudan() {...}
    
    // 구구단의 특정 범위만 출력하는 함수
    export function selectGugudan() {...}
    
    // 이모지로 층을 쌓아 출력하는 함수
    export function fruitsTower() {...}
    ```
    
    - **여러 함수를 내보내기**: `export`를 사용해 **하나의 파일에서 여러 함수를 내보낼 수 있습니다**.

---

### `import`: 모듈 불러오는 방법

- **역할**: 다른 파일에서 **내보낸 함수나 변수를 가져온다**.
- **사용법**: `import { 함수1, 함수2, ... } from '파일경로';` 형식으로 함수를 불러올 수 있다. 콤마로 구분하여 여러개의 함수를 불러올 수 있다.
- import.js  파일에서  export.js의 함수를 호출하여 출력한다.
    
    ```jsx
    import { gugudan, singleGugudan, selectGugudan, fruitsTower } 
    	from './exportexplain.js';
    
    gugudan(); // 1단부터 9단 출력
    singleGugudan(3); // 3단만 출력
    selectGugudan(7, 9); // 7단부터 9단까지 출력
    fruitsTower('🍎', 5); // 사과 이모지로 5층짜리 타워 출력
    ```
    

---

### 자바스크립트 파일을 HTML파일에 모듈로 불러오는 방법

```html
  <script type="module" src="./kobis.js"></script>
```

**`type="module"`**: ES6 모듈 기능을 사용하여 외부 스크립트 파일(`kobis.js`)을 가져옴. script 태그 내에 작성한다.

- 사용 이유 : JavaScript 파일이 HTML 문서에 포함되면, 그 안의 모든 내용이 전역에 영향을 끼친다. 해당 속성을 사용하게 된다면 모듈 스코프에서만 영향을 끼치며 또한 비동기적 실행이 가능하다.

---

### `as` 키워드 - 모듈의 이름을 해당 파일 내에서 별칭으로 변경 및 사용

```jsx
import { kobisBoxOffice as boxOffice} from './kobisCommons.js';
```

위 코드에서 `kobisBoxOffice`는 `kobisCommons.js` 파일에서 내보낸  함수의 이름이다. 이를 `as`를 이용해 `boxOffice`라는 별칭으로 변경하여 현재 파일에서 사용할 수 있다.

<br>
<br>



