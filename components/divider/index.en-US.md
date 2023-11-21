---
category: Components
title: Divider
cover: https://mdn.alipayobjects.com/huamei_7uahnr/afts/img/A*7sMiTbzvaDoAAAAAAAAAAAAADrJ8AQ/original
coverDark: https://mdn.alipayobjects.com/huamei_7uahnr/afts/img/A*KPSEQ74PLg4AAAAAAAAAAAAADrJ8AQ/original
demo:
  cols: 2
group:
  title: Layout
  order: 2
---

Divider (구분선)는 서로 다른 컨텐츠를 나누는 역할을 합니다.

## 사용할 시기

- 서로 다른 문장의 섹션을 구분할 때
- 테이블의

## 사용 예시

<!-- prettier-ignore -->
<code src="./demo/horizontal.tsx">수평선 (Horizontal)</code>
<code src="./demo/with-text.tsx">Divider 그리고 title</code>
<code src="./demo/plain.tsx">heading style 이 없는 Text</code>
<code src="./demo/vertical.tsx">수직선 (Vertical)</code>
<code src="./demo/customize-style.tsx" debug>Style Customization</code>
<code src="./demo/component-token.tsx" debug>Component Token</code>

## API

일반적인 속성 참조：[일반적인 속성](/docs/react/common-props)

| 속성 | 설명 | 타입 | 기본값 | 버전 |
| --- | --- | --- | --- | --- |
| children | Divider 에 감싸진 대상 (제목) | ReactNode | - |  |
| className | Container 의 클래스명 | string | - |  |
| dashed | Divider 선의 점선 여부 | boolean | false |  |
| orientation | Divider 내부 텍스트의 위치 | `left` \| `right` \| `center` | `center` |  |
| orientationMargin | 제목과 가장 가까운 테두리 사이의 여백. `orientation` 은 `left` 또는 `right` 로 설정해주세요. 단위 없이 `string` 으로 숫자 값이 전달되면 픽셀(px) 값으로 인식합니다 | string \| number | - |  |
| plain | Divider 텍스트를 일반 스타일로 표시합니다 | boolean | true | 4.2.0 |
| style | Container 의 스타일 객체 | CSSProperties | - |  |
| type | Divider 의 방항 (수직/수평) | `horizontal` \| `vertical` | `horizontal` |  |

## 테마 변수 (Design Token)

<ComponentTokenTable component="Divider"></ComponentTokenTable>
