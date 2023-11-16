---
category: Components
group: General
title: FloatButton
cover: https://mdn.alipayobjects.com/huamei_7uahnr/afts/img/A*HS-wTIIwu0kAAAAAAAAAAAAADrJ8AQ/original
coverDark: https://mdn.alipayobjects.com/huamei_7uahnr/afts/img/A*a0hwTY_rOSUAAAAAAAAAAAAADrJ8AQ/original
demo:
  cols: 2
tag: New
---

FloatButton 은 `5.0.0` 버전부터 제공된 요소입니다.

## When To Use

- 사이트 전역에서 사용 가능한 기능.
- 스크롤 위치와 상관없이 버튼이 보여야할 때.

## Examples

<!-- prettier-ignore -->
<code src="./demo/basic.tsx" iframe="360">기본</code>
<code src="./demo/type.tsx" iframe="360">타입</code>
<code src="./demo/shape.tsx" iframe="360">모양</code>
<code src="./demo/description.tsx" iframe="360">설명</code>
<code src="./demo/tooltip.tsx" iframe="360">툴팁</code>
<code src="./demo/group.tsx" iframe="360">FloatButton 그룹</code>
<code src="./demo/group-menu.tsx" iframe="360">메뉴모드</code>
<code src="./demo/controlled.tsx" iframe="360">제어모드</code>
<code src="./demo/back-top.tsx" iframe="360">맨 위로가기 (BackTop)</code>
<code src="./demo/badge.tsx" iframe="360">배지</code>
<code src="./demo/badge-debug.tsx" iframe="360" debug>debug dot</code>
<code src="./demo/render-panel.tsx" debug>\_InternalPanelDoNotUseOrYouWillBeFired</code>

## API

일반적인 속성 참조：[일반적인 속성](/docs/react/common-props)

> FloatButton 은 `5.0.0` 버전부터 제공된 요소입니다.

### common API

| 속성 | 설명 | 타입 | 기본값 | 버전 |
| --- | --- | --- | --- | --- |
| icon | 버튼의 아이콘 요소 설정 | ReactNode | - |  |
| description | 텍스트와 기타 내용 | ReactNode | - |  |
| tooltip | 툴팁에서 보여줄 텍스트 | ReactNode \| () => ReactNode |  |  |
| type | 버튼 타입 | `default` \| `primary` | `default` |  |
| shape | 버튼 모양 | `circle` \| `square` | `circle` |  |
| onClick | `click` 이벤트를 처리하는 핸들러 설정 | (event) => void | - |  |
| href | 링크된 페이지의 URL을 명시합니다 | - |  |
| target | `href` 가 지정된 경우 `a` 요소의 `target` 속성과 동일한 역할을 합니다 | string | - |  |
| badge | FloatButton 에 배지 요소를 추가합니다 (`status` 또는 `status` 와 관련된 다른 속성을 지원하지 않습니다) | [BadgeProps](/components/badge#api) | - | 5.4.0 |

### FloatButton.Group

| 속성 | 설명 | 타입 | 기본값 | 버전 |
| --- | --- | --- | --- | --- |
| shape | 자식 요소 (FloatButton) 의 모양 | `circle` \| `square` | `circle` |  |
| trigger | 트리거 활성화 방식 (click 또는 hover) | `click` \| `hover` | - |  |
| open | 메뉴 활성화 여부, 트리거와 함께 사용하세요 | boolean | - |  |
| onOpenChange | 메뉴 활성화 상태가 변경될 때 실행되는 콜백 함수, 트리거와 함께 사용하세요 | (open: boolean) => void | - |  |

### FloatButton.BackTop

| 속성 | 설명 | 타입 | 기본값 | 버전 |
| --- | --- | --- | --- | --- |
| duration | 페이지 최상단으로 돌아가는데 걸리는 시간（ms） | number | 450 |  |
| target | 스크롤 이벤트를 감지할 DOM 노드를 지정합니다 | () => HTMLElement | () => window |  |
| visibilityHeight | BackTop 버튼이 표시되기 시작하는 최소 높이 | number | 400 |  |
| onClick | 버튼을 클릭했을 때 실행되는 콜백함수를 등록합니다 | () => void | - |  |

## Design Token

<ComponentTokenTable component="FloatButton"></ComponentTokenTable>
