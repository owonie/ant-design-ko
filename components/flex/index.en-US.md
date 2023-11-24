---
category: Components
group: Layout
title: Flex
cover: https://mdn.alipayobjects.com/huamei_7uahnr/afts/img/A*SMzgSJZE_AwAAAAAAAAAAAAADrJ8AQ/original
coverDark: https://mdn.alipayobjects.com/huamei_7uahnr/afts/img/A*8yArQ43EGccAAAAAAAAAAAAADrJ8AQ/original
tag: New
---

Flex 는 `5.10.0` 버전부터 제공된 요소입니다.

## 사용할 시기

- 요소 간의 간격을 설정하는 데 유용합니다.
- 다양한 수평 및 수직 정렬을 설정하는 데 적합합니다.

### Space 컴포넌트 와 다른 점

- Space 는 인라인 요소 간의 간격을 설정하는 데 사용됩니다. Space 를 사용하게 되면, inline 정렬을 위한 래퍼 요소를 각 자식 요소에 추가합니다. 또한 Space 는 여러 자식 요소를 행 또는 열에 같은 간격으로 배치하는 데 적합합니다.
- Flex 는 블록 레벨 요소의 레이아웃을 설정하는 데 사용됩니다. Space 와 다르게 래퍼 요소를 추가하지 않습니다. Flex 는 수직 또는 수평 방향의 자식 요소 레이아웃을 구축하는 데 적합하며 더 높은 유연성과 제어성을 사용자에게 제공합니다.

## 사용 예시

<!-- prettier-ignore -->
<code src="./demo/basic.tsx">기본</code>
<code src="./demo/align.tsx">줄맞춤 (align)</code>
<code src="./demo/gap.tsx">간격 (gap)</code>
<code src="./demo/wrap.tsx">줄바꿈 (Wrap)</code>
<code src="./demo/combination.tsx">조합사용 (combination)</code>
<code src="./demo/debug.tsx" debug>debug</code>

## API

> Flex 는 `5.10.0` 버전부터 제공된 요소입니다. Flex 의 기본 설정은 수평 모드와 위쪽 정렬입니다. 수직 모드에선 stretch 정렬을 하게됩니다. Flex 의 속성들을 통해 훨씬 디테일한 작업을 할 수 있습니다.

일반적인 속성 참조：[일반적인 속성](/docs/react/common-props)

| 속성 | 설명 | 타입 | 기본값 | 버전 |
| --- | --- | --- | --- | --- |
| vertical | flex 주축 방향의 수직 여부. 설정 시 `flex-direction: column` 을 사용합니다 | boolean | `false` |  |
| wrap | 요소들이 강제로 한줄에 배치되게 할 것인지, 아니면 영역을 벗어나지 않고 여러행으로 나누어 표현할지 설정합니다 | 참고자료 [flex-wrap](https://developer.mozilla.org/en-US/docs/Web/CSS/flex-wrap) | nowrap |  |
| justify | 주축 (main axis) 방향에서의 정렬을 설정합니다 | 참고자료 [justify-content](https://developer.mozilla.org/en-US/docs/Web/CSS/justify-content) | normal |  |
| align | 교차 축 (cross axis) 방향에서의 정렬을 설정합니다 | 참고자료 [align-items](https://developer.mozilla.org/en-US/docs/Web/CSS/align-items) | normal |  |
| flex | flex CSS 단축 속성 | 참고자료 [flex](https://developer.mozilla.org/en-US/docs/Web/CSS/flex) | normal |  |
| gap | 그리드 간격을 설정합니다 | `small` \| `middle` \| `large` \| string \| number | - |  |
| component | 커스텀 요소의 타입 | React.ComponentType | `div` |  |

## 테마 변수 (Design Token)

<ComponentTokenTable component="Flex"></ComponentTokenTable>
