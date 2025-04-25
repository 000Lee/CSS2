#  CSS 텍스트 스타일 & 폰트 정리

##  글꼴 관련 스타일

###  기본 속성

| 속성 | 설명 |
|------|------|
| `font-family` | 글꼴 지정 (보유 중인 글꼴만 사용 가능)<br>`font-family: pretendard;` |
| `font-size` | 글자 크기 |
| `font-style` | 이탤릭체 (예: `font-style: italic;`) |
| `font-weight` | 글자 굵기 |
| `font-optical-sizing: auto;` | 텍스트 크기에 따라 글자모양 최적화 |

---

##  폰트 크기 단위

| 단위 | 기준 | 예시 | 특징 |
|------|------|------|------|
| `px` | 절대 크기 | `font-size: 16px` | 고정 크기 |
| `%` | 부모 요소 기준 | `font-size: 200%` | 레이아웃에 자주 사용 |
| `em` | 부모 요소 기준 | `font-size: 2em` | 폰트 크기에 사용 |
| `rem` | 루트 요소(html) 기준 | `font-size: 2rem` | 글로벌 폰트 사이즈 조절에 유리 |

---

##  웹 폰트 사용 방법

###  `@font-face` 방식 (직접 폰트 파일 사용)

```css
@font-face {
  font-family: 'Ostrich';
  src: url('../fonts/ostrich-sans-bold.eot'),
       url('../fonts/ostrich-sans-bold.svg') format('svg'),
       url('../fonts/ostrich-sans-bold.woff') format('woff');
}
```

- 다양한 포맷 사용 권장 (브라우저 호환성)
- `eot`는 `format()` 안 씀
- `src`: 경로 지정  
- `format`: 확장자명 정의

```css
.wfont {
  font-family: 'Ostrich', 바탕, sans-serif;
}
```
- 여러 글꼴을 쉼표로 나열 → 브라우저가 순서대로 적용 시도
- 마지막에는 `sans-serif` 또는 `system-ui` 권장

---

###  구글 폰트 사용

#### `<link>` 방식
1. 구글 폰트 사이트에서 `<link>` 태그 복사
2. `<head>`의 `<title>` 아래에 붙여넣기

#### `@import` 방식
1. 구글 폰트에서 `@import` 코드 복사
2. `<style>` 태그 안에 붙여넣기

#### 클래스 적용
구글폰트에서 제공한 CSS 클래스도 복사해서 원하는 태그에 사용

---

###  폰트명 따옴표

- **필요 O**: 이름에 공백이나 특수문자가 있을 경우  
  → `'Nanum Gothic'`, `"Roboto Slab"`
- **필요 X**: 하나의 단어일 경우  
  → `Pretendard`, `Arial`

---

##  텍스트 관련 스타일

| 속성 | 설명 |
|------|------|
| `color` | 글자 색상 |
| `text-decoration` | 밑줄, 취소선 등 (`none`, `underline`, `overline`, `line-through`) |
| `text-transform` | 대소문자 변환 (`capitalize`, `uppercase`, `lowercase`) |
| `text-shadow` | 그림자 효과: `x y blur color` |
| `letter-spacing` | 글자 간격 |
| `word-spacing` | 단어 간격 |
| `text-align` | 정렬 (`left`, `center`, `right`) |
| `line-height` | 줄 간격 (ex. `2.5` = 2.5배) |

---

##  색상 지정 방법

| 방법 | 설명 | 예시 |
|------|------|------|
| 16진수 (`#`) | `#RRGGBB` 형식 | `#ff0000` |
| `rgb()` | 빨강, 초록, 파랑 (0~255) | `rgb(255,0,0)` |
| `rgba()` | + 불투명도 (0~1) | `rgba(255,0,0,0.5)` |
| `hsl()` | 색상(H), 채도(S), 명도(L) | `hsl(0, 100%, 50%)` |
| `hsla()` | + 불투명도 | `hsla(0, 100%, 50%, 0.5)` |
| 색상 이름 | CSS 키워드 | `red`, `blue`, `black` 등 |

---
