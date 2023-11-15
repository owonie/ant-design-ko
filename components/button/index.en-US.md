---
category: Components
title: Button
cover: https://mdn.alipayobjects.com/huamei_7uahnr/afts/img/A*BrFMQ5s7AAQAAAAAAAAAAAAADrJ8AQ/original
coverDark: https://mdn.alipayobjects.com/huamei_7uahnr/afts/img/A*Lp1kTYmSsgoAAAAAAAAAAAAADrJ8AQ/original
demo:
  cols: 2
group:
  title: General
  order: 1
---

작업을 트리거 하기 위한 요소.

## 사용할 시기

버튼은 한번 (또는 한 묶음) 의 액션 조작을 의미합니다. 클릭을 트리거로 비즈니스 로직을 실행할 수 있습니다.

Ant Design 은 다섯 종류의 버튼을 제공합니다.

- Primary 버튼: 메인 액션을 수행하기 위한 버튼입니다. 한 섹션엔 단 하나의 primary 버튼만 사용할 수 있습니다.
- Default 버튼: 실행 순서와 상관 없는 액션들을 수행할 때 사용하는 버튼입니다.
- Dashed 버튼: 요소를 추가하는 액션에 주로 사용되는 버튼입니다.
- Text 버튼: 부가적인 액션을 수행할 떄 사용되는 버튼입니다.
- Link 버튼: 외부링크를 참조할 때 사용할 수 있는 버튼입니다.

버튼은 아래의 4가지 속성과 함께 조합해서 사용할 수 있습니다.

- `danger`: 삭제기능 또는 권한수정과 같이 리스크가 있는 액션에 사용됩니다.
- `ghost`: 메인 페이지처럼 배경색이 복잡한 곳에서 사용할 수 있습니다.
- `disabled`: 액션을 수행할 수 없는 상태를 표시하는 속성입니다.
- `loading`: 버튼에 로딩 스피너를 추가할 수 있으며, 필요에 따라 다중 제출을 방지할 수도 있습니다.

## 사용 예시

<!-- prettier-ignore -->
<code src="./demo/basic.tsx">버튼 종류</code>
<code src="./demo/icon.tsx">아이콘</code>
<code src="./demo/debug-icon.tsx" debug>Debug Icon</code>
<code src="./demo/debug-block.tsx" debug>Debug Block</code>
<code src="./demo/size.tsx">사이즈</code>
<code src="./demo/disabled.tsx">비활성화</code>
<code src="./demo/loading.tsx">로딩 상태</code>
<code src="./demo/multiple.tsx">다중버튼 조합</code>
<code src="./demo/ghost.tsx">고스트 버튼</code>
<code src="./demo/danger.tsx">위험 버튼</code>
<code src="./demo/block.tsx">블록 버튼</code>
<code src="./demo/legacy-group.tsx" debug>Deprecated Button Group</code>
<code src="./demo/chinese-chars-loading.tsx" debug>Loading style bug</code>
<code src="./demo/component-token.tsx" debug>Component Token</code>

## API

일반적인 속성 참조：[일반적인 속성](/docs/react/common-props)

버튼 속성을 이용해 다양한 버튼 스타일을 생성할 수 있습니다. 다음과 같은 순서로 버튼 속성에 접근해보세요: `type` -> `shape` -> `size` -> `loading` -> `disabled`.

| 속성 | 설명 | 타입 | 기본 값 | 버전 |
| --- | --- | --- | --- | --- |
| block | 버튼의 `width` 를 부모의 `width` 에 맞게 설정한다 | boolean | false |  |
| classNames | 시멘틱 DOM 클래스 | Record<SemanticDOM, string> | - | 5.4.0 |
| danger | 버튼 `danger` 속성 설정 | boolean | false |  |
| disabled | 버튼 `disabled` 속성 설정 | boolean | false |  |
| ghost | 배경을 투명색으로 지정하고, 텍스트와 테두리 색상을 반전합니다 | boolean | false |  |
| href | 링크된 페이지의 URL을 명시합니다 | string | - |  |
| htmlType | `button`의 오리지널 html `type` 을 설정합니다 [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/button#attr-type) | string | `button` |  |
| icon | 버튼의 아이콘 컴포넌트 설정 | ReactNode | - |  |
| loading | 버튼 로딩 상태 | boolean \| { delay: number } | false |  |
| shape | 버튼 모양 | `default` \| `circle` \| `round` | `default` |  |
| size | 버튼 사이즈 | `large` \| `middle` \| `small` | `middle` |  |
| styles | 시멘틱 DOM 스타일 | Record<SemanticDOM, CSSProperties> | - | 5.4.0 |
| target | `href` 가 지정된 경우 `a` 요소의 `target` 속성과 동일한 역할을 합니다 | string | - |  |
| type | 버튼 타입 | `primary` \| `dashed` \| `link` \| `text` \| `default` | `default` |  |
| onClick | `click` 이벤트를 처리하는 핸들러 설정 | (event: MouseEvent) => void | - |  |

기존 html 버튼에서 지원하는 다른 속성들 까지 모두 지원하고 있습니다.

### `styles` 와 `classNames` 속성

| 속성 | 설명             | 버전  |
| ---- | ---------------- | ----- |
| icon | `icon` 요소 설정 | 5.5.0 |

## 테마 변수(Design Token)

<ComponentTokenTable component="Button"></ComponentTokenTable>

## FAQ

### 두 한자 사이의 공백을 없애는 방법?

Ant Design 에선 버튼에 한자가 두 글자만 있는 경우, 두 한자 사이에 공백을 추가합니다 (Text 버튼과 Link 버튼은 예외). 공백을 없에고 싶다면 [ConfigProvider](/components/config-provider/#api) 을 이용해서 `autoInsertSpaceInButton` 를 `false` 로 설정하세요.

```tsx
<ConfigProvider autoInsertSpaceInButton={false}>
  <Button>按钮</Button>
</ConfigProvider>
```

<img src="https://gw.alipayobjects.com/zos/antfincdn/MY%26THAPZrW/38f06cb9-293a-4b42-b183-9f443e79ffea.png" width="100px" height="64px" style="box-shadow: none; margin: 0;" alt="Button with two Chinese characters" />

<style>
.site-button-ghost-wrapper {
  padding: 16px;
  background: rgb(190, 200, 200);
}
</style>
