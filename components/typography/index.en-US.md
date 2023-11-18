---
category: Components
group: General
title: Typography
cover: https://mdn.alipayobjects.com/huamei_7uahnr/afts/img/A*MLt3R6m9huoAAAAAAAAAAAAADrJ8AQ/original
coverDark: https://mdn.alipayobjects.com/huamei_7uahnr/afts/img/A*LT2jR41Uj2EAAAAAAAAAAAAADrJ8AQ/original
---

텍스트의 기본 형식

## 사용할 시기

- 글 / 블로그 / 노트에서 제목 또는 단락 내용을 표시해야할 때.
- 복사 / 편집 / 말줄임 등 기능이 있는 텍스트가 필요한 경우.

## 사용 예시

<!-- prettier-ignore -->
<code src="./demo/basic.tsx">기본</code>
<code src="./demo/title.tsx">Title 컴포넌트</code>
<code src="./demo/paragraph-debug.tsx" debug>Title 그리고 Paragraph</code>
<code src="./demo/text.tsx">Text 그리고 Link 컴포넌트</code>
<code src="./demo/interactive.tsx">상호적인 기능</code>
<code src="./demo/ellipsis.tsx">말줄임 (Ellipsis)</code>
<code src="./demo/ellipsis-middle.tsx">텍스트 중간 말줄임 (Ellipsis)</code>
<code src="./demo/ellipsis-debug.tsx" debug>Ellipsis Debug</code>
<code src="./demo/suffix.tsx">텍스트 접미사 말줄임 (suffix)</code>
<code src="./demo/componentToken-debug.tsx" debug>컴포넌트 토큰</code>

## API

일반적인 속성 참조：[일반적인 속성](/docs/react/common-props)

### Typography.Text

| 속성 | 설명 | 타입 | 기본값 | 버전 |
| --- | --- | --- | --- | --- |
| code | 코드 스타일 설정 | boolean | false |  |
| copyable | 텍스트의 복사 가능 여부를 설정할 수 있으며 대상이 객체일 경우 다양한 속성을 정의할 수 있습니다 | boolean \| [copyable](#copyable) | false | [copyable](#copyable) |
| delete | 취소선 스타일 설정 | boolean | false |  |
| disabled | 사용불가 스타일 설정 | boolean | false |  |
| editable | 텍스트의 편집 가능 여부를 설정할 수 있으며 대상이 객체일 경우 편집 상태를 제어할 수 있습니다 | boolean \| [editable](#editable) | false | [editable](#editable) |
| ellipsis | 텍스트가 너무 길어지면 말줄임 처리를 합니다. 객체를 이용하여 행 개수 또는 확장 가능 여부 등을 설정할 수 없습니다. Typography.Paragraph와 달리 Text는 100% width 를 할 수 없으므로 첫 번째 말줄임표의 width 는 고정적입니다. 반응형 말줄임표를 사용하고 싶다면 width 를 수동으로 설정하세요 | boolean \| [Omit<ellipsis, 'expandable' \| 'rows' \| 'onExpand'>](#ellipsis) | false | [ellipsis](#ellipsis) |
| keyboard | 키보드 스타일 | boolean | false | 4.3.0 |
| mark | 마킹 스타일 설정 | boolean | false |  |
| onClick | 버튼을 클릭했을 때 실행되는 콜백함수를 등록합니다 | (event) => void | - |  |
| strong | 강조된 텍스트 스타일 설정 | boolean | false |  |
| italic | 이탤릭체 스타일 설정 | boolean | false | 4.16.0 |
| type | 컨텐츠 타입 설정 | `secondary` \| `success` \| `warning` \| `danger` | - | success: 4.6.0 |
| underline | 텍스트 밑줄 설정 | boolean | false |  |

### Typography.Title

| 속성 | 설명 | 타입 | 기본값 | 버전 |
| --- | --- | --- | --- | --- |
| code | 코드 스타일 설정 | boolean | false |  |
| copyable | 텍스트의 복사 가능 여부를 설정할 수 있으며 대상이 객체일 경우 다양한 속성을 정의할 수 있습니다 | boolean \| [copyable](#copyable) | false | [copyable](#copyable) |
| delete | 취소선 스타일 설정 | boolean | false |  |
| disabled | 사용불가 스타일 설정 | boolean | false |  |
| editable | 텍스트의 편집 가능 여부를 설정할 수 있으며 대상이 객체일 경우 편집 상태를 제어할 수 있습니다 | boolean \| [editable](#editable) | false | [editable](#editable) |
| ellipsis | 텍스트가 너무 길어지면 말줄임 처리를 합니다. 객체를 이용하여 행 개수 또는 확장 가능 여부를 설정할 수 있습니다 | boolean \| [ellipsis](#ellipsis) | false | [ellipsis](#ellipsis) |
| level | 텍스트 컨텐츠의 중요도를 표시할 수 있습니다. 표현수준은 `h1`, `h2`, `h3`, `h4`, `h5` 와 같습니다 | number: 1, 2, 3, 4, 5 | 1 | 5: 4.6.0 |
| mark | 마킹 스타일 설정 | boolean | false |  |
| onClick | 버튼을 클릭했을 때 실행되는 콜백함수를 등록합니다 | (event) => void | - |  |
| italic | 이탤릭체 스타일 설정 | boolean | false | 4.16.0 |
| type | 컨텐츠 타입 설정 | `secondary` \| `success` \| `warning` \| `danger` | - | success: 4.6.0 |
| underline | 텍스트 밑줄 설정 | boolean | false |  |

### Typography.Paragraph

| 속성 | 설명 | 타입 | 기본값 | 버전 |
| --- | --- | --- | --- | --- |
| code | 코드 스타일 설정 | boolean | false |  |
| copyable | 텍스트의 복사 가능 여부를 설정할 수 있으며 대상이 객체일 경우 다양한 속성을 정의할 수 있습니다 | boolean \| [copyable](#copyable) | false | [copyable](#copyable) |
| delete | 취소선 스타일 설정 | boolean | false |  |
| disabled | 사용불가 스타일 설정 | boolean | false |  |
| editable | 텍스트의 편집 가능 여부를 설정할 수 있으며 대상이 객체일 경우 편집 상태를 제어할 수 있습니다 | boolean \| [editable](#editable) | false | [editable](#editable) |
| ellipsis | 텍스트가 너무 길어지면 말줄임 처리를 합니다. 객체를 이용하여 행 개수 또는 확장 가능 여부를 설정할 수 있습니다 | boolean \| [ellipsis](#ellipsis) | false | [ellipsis](#ellipsis) |
| mark | 마킹 스타일 설정 | boolean | false |  |
| onClick | 버튼을 클릭했을 때 실행되는 콜백함수를 등록합니다 | (event) => void | - |  |
| strong | 강조된 텍스트 스타일 설정 | boolean | false |  |
| italic | 이탤릭체 스타일 설정 | boolean | false | 4.16.0 |
| type | 컨텐츠 타입 | `secondary` \| `success` \| `warning` \| `danger` | - | success: 4.6.0 |
| underline | 텍스트 밑줄 설정 | boolean | false |  |

### copyable

    {
      text: string,
      onCopy: function(event),
      icon: ReactNode,
      tooltips: false | [ReactNode, ReactNode],
      format: 'text/plain' | 'text/html',
    }

| 속성 | 설명 | 타입 | 기본값 | 버전 |
| --- | --- | --- | --- | --- |
| format | 텍스트의 Mime 타입 | 'text/plain' \| 'text/html' | - | 4.21.0 |
| icon | 커스텀 복제 버튼 아이콘: \[copyIcon, copiedIcon] | \[ReactNode, ReactNode] | - | 4.6.0 |
| text | 복사 된 텍스트 내용 | string | - |  |
| tooltips | 값이 false 일시, 텍스트를 숨기는 커스텀 툴팁을 등록합니다 | \[ReactNode, ReactNode] | \[`Copy`, `Copied`] | 4.4.0 |
| onCopy | 텍스트가 복사될 때 실행되는 콜백함수를 등록합니다 | function | - |  |

### editable

    {
      icon: ReactNode,
      tooltip: boolean | ReactNode,
      editing: boolean,
      maxLength: number,
      autoSize: boolean | { minRows: number, maxRows: number },
      text: string,
      onChange: function(string),
      onCancel: function,
      onStart: function,
      onEnd: function,
      triggerType: ('icon' | 'text')[],
      enterIcon: ReactNode,
    }

| 속성 | 설명 | 타입 | 기본값 | 버전 |
| --- | --- | --- | --- | --- |
| autoSize | 텍스트 영역을 `autoSize` 처리합니다 | boolean \| { minRows: number, maxRows: number } | - | 4.4.0 |
| editing | 편집 가능 여부 | boolean | false |  |
| icon | 커스텀 편집 버튼 | ReactNode | &lt;EditOutlined /> | 4.6.0 |
| maxLength | 텍스트 영역의 `maxLength` 속성 | number | - | 4.4.0 |
| tooltip | 텍스트를 줄임 처리할 시 표시되는 툴팁 | boolean \| ReactNode | `Edit` | 4.6.0 |
| text | 명시적으로 편집 텍스트를 지정해줍니다. 빈값일 시 암시적으로 children 을 사용합니다 | string | - | 4.24.0 |
| onChange | 텍스트 영역에서 입력을 할 때 실행되는 콜백함수를 등록합니다 | function(value: string) | - |  |
| onCancel | ESC 를 눌러 편집상태를 종료했을 때 실행되는 콜백함수를 등록합니다 | function | - |  |
| onStart | 편집상태에 진입했을 때 실행되는 콜백함수를 등록합니다 | function | - |  |
| onEnd | Enter 를 눌러 편집상태를 종료했을 때 실행되는 콜백함수를 등록합니다 | function | - | 4.14.0 |
| triggerType | 편집 모드 트리거 - 아이콘, 텍스트 또는 둘 다 설정할 수 있습니다 (아이콘을 따로 트리거로 지정해주지 않으면 숨김처리 됩니다) | Array&lt;`icon`\|`text`> | \[`icon`] |  |
| enterIcon | 편집 필드에서 Enter 아이콘을 커스터마이징 할 수 있습니다 (`null` 을 전달 시 아이콘 제거) | ReactNode | `<EnterOutlined />` | 4.17.0 |

### ellipsis

    {
      rows: number,
      expandable: boolean,
      suffix: string,
      symbol: ReactNode,
      tooltip: boolean | ReactNode | TooltipProps,
      onExpand: function(event),
      onEllipsis: function(ellipsis),
    }

| 속성 | 설명 | 타입 | 기본값 | 버전 |
| --- | --- | --- | --- | --- |
| expandable | 확장 (전개) 가능 여부 | boolean | - |  |
| rows | 텍스트 내용의 최대 행 수 | number | - |  |
| suffix | 줄임표의 접미사 (Suffix of ellipsis content) | string | - |  |
| symbol | 텍스트 줄임 시 표시되는 설명 | ReactNode | `Expand` |  |
| tooltip | 텍스트를 줄임 처리할 시 표시되는 툴팁 | boolean \| ReactNode \| [TooltipProps](/components/tooltip/#api) | - | 4.11.0 |
| onEllipsis | 텍스트를 줄였을 때 실행되는 콜백함수를 등록합니다 | function(ellipsis) | - | 4.2.0 |
| onExpand | 텍스트를 펼쳤을 때 실행되는 콜백함수를 등록합니다 | function(event) | - |  |

## 테마 변수 (Design Token)

<ComponentTokenTable component="Typography"></ComponentTokenTable>

## FAQ

### react-router 에서 Typography.Link 사용하는 방법?

`react-router` 는 [커스터마이즈](https://github.com/ReactTraining/react-router/blob/master/packages/react-router-dom/docs/api/Link.md#component-reactcomponent) 렌더 컴포넌트를 지원합니다:

```tsx
<Link to="/" component={Typography.Link} />
```

**Note：** react-router's Link 실행 로직과 다릅니다. [참고문서](https://github.com/ant-design/ant-design/pull/26737/files#r488769888)
