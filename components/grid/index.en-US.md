---
category: Components
group: Layout
title: Grid
cover: https://mdn.alipayobjects.com/huamei_7uahnr/afts/img/A*mfJeS6cqZrEAAAAAAAAAAAAADrJ8AQ/original
coverDark: https://mdn.alipayobjects.com/huamei_7uahnr/afts/img/A*DLUwQ4B2_zQAAAAAAAAAAAAADrJ8AQ/original
---

24 Grid 시스템.

## 디자인 컨셉

<div class="grid-demo">
  <img src="https://gw.alipayobjects.com/zos/bmw-prod/9189c9ef-c601-40dc-9960-c11dbb681888.svg" alt="grid design" />
</div>

Ant Design 은 대부분의 비즈니스 상황에서 디자인 영역에 많은 데이터를 저장해야 합니다. 그래서 12 Grid 시스템을 기반으로 디자인 영역을 24개 섹션으로 나누었습니다.

Ant Design 에선 나눠진 영역을 'box' 라고 부릅니다. Grid 를 사용할 때, 가로 방향으로 box 는 최소 1 개, 최대 4 개만 배치하는 것을 추천드립니다. Box 는 위의 그림과 같이 전체 화면에 맞춰 비율이 조정됩니다. Box 단위로 내부의 Typography 를 설정할 수 있어, 사용자에게 시각적으로 편안한 느낌을 제공합니다.

## 개요

Grid 시스템에선 `row` 와 `column` 을 기반으로 섹션의 외부 프레임을 정의하여, 안정적인 구조로 섹션을 나눌 수 있습니다.

Grid 시스템의 동작 원리에 대해 간단하게 살펴봅시다:

- `row` 에 의해 정의된 가로 공간에 `column` 집합을 설정합니다 (줄여서 col).
- 컨텐츠 요소는 `col` 내부에 작성해야합니다. 그리고 오직 `col` 만 `row` 내부에 요소로서 존재합니다.
- `col` 을 이용한 grid 시스템은 1-24 규모의 범위를 적용할 수 있습니다. 예를 들어 동일한 width 의 세 열은 `<Col span={8} />` 로 생성할 수 있습니다.
- 하나의 `row` 안에 `col` 갯수가 24 를 넘으면, 나머지 `col` 들은 새로운 라인에 (row) 에 배치됩니다.

Antd 의 Grid 시스템은 Flex Layout 을 기반으로 하여 부모 요소 내부의 각 요소들을 수평으로 정렬할 수 있습니다. 이는 left 정렬, center 정렬, right 정렬, 동일 간격 정렬, 분산 정렬이 가능합니다. Grid 시스템은 수직 정렬 기능도 지원합니다. top 정렬, 수직 중앙 정렬, bottom 정렬 등이 가능합니다. 또한 `order` 를 사용하여 요소의 순서를 정의할 수도 있습니다.

Layout 은 24 Gird Layout 을 이용해 box 의 너비를 정의하지만, Grid 에 완전 종속되진 않습니다.

## 사용 예시

<!-- prettier-ignore -->
<code src="./demo/basic.tsx">기본 Grid</code>
<code src="./demo/gutter.tsx">Grid 간격</code>
<code src="./demo/offset.tsx">Column 오프셋 (offset)</code>
<code src="./demo/sort.tsx">Grid 순서</code>
<code src="./demo/flex.tsx">타입 세팅 (Typesetting)</code>
<code src="./demo/flex-align.tsx">수직 정렬 (Alignment)</code>
<code src="./demo/flex-order.tsx">순서 정렬 (Order)</code>
<code src="./demo/flex-stretch.tsx">Flex Stretch</code>
<code src="./demo/responsive.tsx">반응형</code>
<code src="./demo/responsive-more.tsx">더 많은 반응형</code>
<code src="./demo/playground.tsx">플레이그라운드</code>
<code src="./demo/useBreakpoint.tsx">useBreakpoint Hook</code>

## API

일반적인 속성 참조：[일반적인 속성](/docs/react/common-props)

Ant Design Grid Layout Component 가 요구 사항을 충족하지 못하는 경우, 다른 커뮤니티의 Layout Component 를 참조해봐도 좋습니다:

- [react-flexbox-grid](http://roylee0704.github.io/react-flexbox-grid/)
- [react-blocks](https://github.com/whoisandy/react-blocks/)

### Row

| 속성 | 설명 | 타입 | 기본값 | 버전 |
| --- | --- | --- | --- | --- |
| align | 수직 정렬 | `top` \| `middle` \| `bottom` \| `stretch` \| `{[key in 'xs' \| 'sm' \| 'md' \| 'lg' \| 'xl' \| 'xxl']: 'top' \| 'middle' \| 'bottom' \| 'stretch'}` | `top` | object: 4.24.0 |
| gutter | Grid 의 간격을 설정합니다, 숫자 또는 객체 형식이 가능합니다 { xs: 8, sm: 16, md: 24}. `[수평, 수직]` 형식처럼 배열 방식으로 간격을 조정할 수 도 있습니다 | number \| object \| array | 0 |  |
| justify | 수평 정렬 | `start` \| `end` \| `center` \| `space-around` \| `space-between` \| `space-evenly` \| `{[key in 'xs' \| 'sm' \| 'md' \| 'lg' \| 'xl' \| 'xxl']: 'start' \| 'end' \| 'center' \| 'space-around' \| 'space-between' \| 'space-evenly'}` | `start` | object: 4.24.0 |
| wrap | 자동 줄 바꿈 | boolean | true | 4.8.0 |

### Col

| 속성 | 설명 | 타입 | 기본값 | 버전 |
| --- | --- | --- | --- | --- |
| flex | Flex 레아아웃 스타일 | string \| number | - |  |
| offset | Grid 왼쪽 간격 개수, 간격 사이에 Grid 가 있으면 안됩니다 | number | 0 |  |
| order | Grid 순서 | number | 0 |  |
| pull | Grid 를 왼쪽으로 옮길 개수 | number | 0 |  |
| push | Grid 를 오른쪽으로 옮길 개수 | number | 0 |  |
| span | Grid 가 차지할 간격 개수, 0 일 때 `display: none` 와 동일한 결과를 보여줍니다 | number | - |  |
| xs | 스크린 사이즈가 `576px` 보다 작을 때, 해당 속성은 `span` 값이나 `props` 갖고있는 객체를 받습니다 | number \| object | - |  |
| sm | 스크린 사이즈가 `576px` 보다 크거나 같을 때, 해당 속성은 `span` 값이나 `props` 갖고있는 객체를 받습니다 | number \| object | - |  |
| md | 스크린 사이즈가 `768px` 보다 크거나 같을 때, 해당 속성은 `span` 값이나 `props` 갖고있는 객체를 받습니다 | number \| object | - |  |
| number \| object | - |  |
| lg | 스크린 사이즈가 `992px` 보다 크거나 같을 때, 해당 속성은 `span` 값이나 `props` 갖고있는 객체를 받습니다 | number \| object | - |  |
| xl | 스크린 사이즈가 `1200px` 보다 크거나 같을 때, 해당 속성은 `span` 값이나 `props` 갖고있는 객체를 받습니다 | number \| object | - |  |
| xxl | 스크린 사이즈가 `1600px` 보다 크거나 같을 때, 해당 속성은 `span` 값이나 `props` 갖고있는 객체를 받습니다 | number \| object | - |  |

[Theme customization](/docs/react/customize-theme) 을 이용해 `screen[XS|SM|MD|LG|XL|XXL]` 을 수정하여 breakpoints 값을 조정할 수 있습니다. ( 버전 5.1.0 부터 가능, [sandbox demo](https://codesandbox.io/s/antd-reproduction-template-forked-dlq3r9?file=/index.js)).

반응형 Grid 의 breakpoints 는 [BootStrap 4 의 규칙](https://getbootstrap.com/docs/4.0/layout/overview/#responsive-breakpoints) (`occasionally part` 제외) 을 따릅니다.

## 테마 변수 (Design Token)

<ComponentTokenTable component="Grid"></ComponentTokenTable>
