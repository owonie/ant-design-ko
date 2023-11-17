---
category: Components
group: General
title: Icon
description: 시맨틱 벡터 그래픽.
toc: false
cover: https://mdn.alipayobjects.com/huamei_7uahnr/afts/img/A*PdAYS7anRpoAAAAAAAAAAAAADrJ8AQ/original
coverDark: https://mdn.alipayobjects.com/huamei_7uahnr/afts/img/A*xEDOTJx2DEkAAAAAAAAAAAAADrJ8AQ/original
demo:
  cols: 2
---

## 사용하는 법

Icon 을 사용하기 전에 [@ant-design/icons](https://github.com/ant-design/ant-design-icons) 패키지 설치가 필요합니다:

<InstallDependencies npm='npm install @ant-design/icons --save' yarn='yarn add @ant-design/icons' pnpm='pnpm install @ant-design/icons --save'></InstallDependencies>

## Icon 리스트

<IconSearch></IconSearch>

## 사용 예시

<!-- prettier-ignore -->
<code src="./demo/basic.tsx">기본 Icon</code>
<code src="./demo/two-tone.tsx">투톤 Icon</code>
<code src="./demo/custom.tsx">커스텀 Icon</code>
<code src="./demo/iconfont.tsx">iconfont.cn 라이브러리</code>
<code src="./demo/scriptUrl.tsx">iconfont.cn 라이브러리의 다양한 리소스</code>

## API

### 일반 Icon

| 속성 | 설명 | 타입 | 기본값 | 버전 |
| --- | --- | --- | --- | --- |
| className | Icon 의 className | string | - |  |
| rotate | Icon 로테이션 각도 (IE9 버전에선 지원하지 않습니다) | number | - |  |
| spin | Icon 을 로테이션 시킵니다 | boolean | false |  |
| style | Icon 의 style (예: `fontSize`, `color`) | CSSProperties | - |  |
| twoToneColor | 투톤 Icon 전용속성, 메인색을 지정할 수 있습니다 | string (hex color) | - |  |

세 가지 다른 Icon 테마가 있으며, Icon 컴포넌트명 뒤에 테마를 접미사로 붙여 import 할 수 있습니다.

```jsx
import { StarOutlined, StarFilled, StarTwoTone } from '@ant-design/icons';

<StarOutlined />
<StarFilled />
<StarTwoTone twoToneColor="#eb2f96" />
```

### 커스텀 Icon

| 속성 | 설명 | 타입 | 기본값 | 버전 |
| --- | --- | --- | --- | --- |
| component | Icon 렌더링을 제어하는 데 사용되며, 일반적으로 `<svg>` 에 감싸진 React 컴포넌트 형태를 갖고있습니다 | ComponentType&lt;CustomIconComponentProps> | - |  |
| rotate | Icon 로테이션 각도 (IE9 버전에선 지원하지 않습니다) | number | - |  |
| spin | Icon 을 로테이션 시킵니다 | boolean | false |  |
| style | Icon 의 style (예: `fontSize`, `color`) | CSSProperties | - |  |

### SVG Icon 관하여

버전 `3.9.0` 이후, antd 는 SVG Icon 으로 폰트 Icon 을 대체하여 아래와 같은 메리트를 얻을 수 있었습니다:

- CDN 파일 호스팅에 의존할 필요없이 오프라인에서 사용 가능 (빈 Icon 이미지를 유저에게 노출시키지 않으며, 로컬에서 Icon 폰트파일을 배포할 필요가 없어집니다)
- 낮은 해상도 화면에서 더 좋은 화질 표시
- Icon 색상 지정 가능
- `style` 오버라이드 없이 built-in Icon 컴포넌트에 더 많은 속성을 제공

더 많은 내용은 해당 링크를 참조하세요: [#10353](https://github.com/ant-design/ant-design/issues/10353).

> ⚠️ 버전 3.9.0 에서 모든 svg Icon 을 가져오면서 번들 사이즈가 거대해지는 현상을 해결하기 위해, 사용자가 필요한 Icon 만 가져올 수 있는 API 를 제공할 예정입니다. 관심이 있다면 해당 링크를 참조하세요: [#12011](https://github.com/ant-design/ant-design/issues/12011) .
>
> 커뮤니티에서 [webpack plugin](https://github.com/Beven91/webpack-ant-icon-loader) 을 이용해 Icon 파일을 chunk 할 수 도 있습니다.

`theme`, `component` 그리고 `twoToneColor` 속성은 버전 `3.9.0` 에 추가되었습니다. 모든 `<Icon />` 컴포넌트에 `theme` 속성을 적용하는 방식을 사용하는 것을 추천드립니다.

```jsx
import { MessageOutlined } from '@ant-design/icons';

<MessageOutlined style={{ fontSize: '16px', color: '#08c' }} />;
```

모든 Icon 컴포넌트는 `<svg>` 형식으로 렌더됩니다. 기본 Icon 과 똑같이 `style` 과 `className` 속성을 이용해 Icon 의 사이즈와 컬러를 설정할 수 있습니다.

```jsx
<Icon type="message" style={{ fontSize: '16px', color: '#08c' }} theme="outlined" />
```

### 투톤 컬러 설정하기

투톤 Icno 의 정적 메서드 `getTwoToneColor()` 와 `setTwoToneColor(colorString)` 를 이용해 투톤 컬러를 지정하세요.

```jsx
import { getTwoToneColor, setTwoToneColor } from '@ant-design/icons';

setTwoToneColor('#eb2f96');
getTwoToneColor(); // #eb2f96
```

### 커스텀 폰트 Icon

사용자가 [iconfont.cn](http://iconfont.cn/) 라이브러리에서 제공되는 Icon 을 편리하게 사용할 수 있게끔 `createFromIconfontCN` 함수를 제공합니다.

> 해당 메서드는 [iconfont.cn](http://iconfont.cn/) 전용 메서드입니다.

```jsx
import React from 'react';
import { createFromIconfontCN } from '@ant-design/icons';
import ReactDOM from 'react-dom/client';

const MyIcon = createFromIconfontCN({
  scriptUrl: '//at.alicdn.com/t/font_8d5l8fzk5b87iudi.js', // generate in iconfont.cn
});

ReactDOM.createRoot(mountNode).render(<MyIcon type="icon-example" />);
```

`<use>` 태그로 Icon 컴포넌트를 렌더하는 방식으로 작동됩니다.

커스텀 Icon 속성:

| 속성 | 설명 | 타입 | 기본값 | 버전 |
| --- | --- | --- | --- | --- |
| extraCommonProps | 컴포넌트의 추가 속성 | { \[key: string]: any } | {} |  |
| scriptUrl | [iconfont.cn](http://iconfont.cn/) 프로젝트에서 생성된 URL. `@ant-design/icons@4.1.0` 버전 이후로 `string[]` 타입을 지원합니다 | string \| string\[] | - |  |

`scriptUrl` 속성이 유효하게 설정된 경우, Icon 컴포넌트는 렌더링 전 자동으로 iconfont.cn 에서 필요한 `Svg sprites symbols` 를 가져옵니다.

[iconfont.cn documents](http://iconfont.cn/help/detail?spm=a313x.7781069.1998910419.15&helptype=code) 에서 `scriptUrl` 주소를 생성하는 방법을 확인할 수 있습니다.

### 커스텀 SVG Icon

`webpack` 을 사용한다면 [`@svgr/webpack`](https://www.npmjs.com/package/@svgr/webpack)로 SVG icon 을 React 컴포넌트 형식으로 import 해보세요. `@svgr/webpack` `options` 속성은 [참고문서](https://github.com/smooth-code/svgr#options)을 확인해보세요.

```js
// webpack.config.js
module.exports = {
  // ... other config
  test: /\.svg(\?v=\d+\.\d+\.\d+)?$/,
  use: [
    {
      loader: 'babel-loader',
    },
    {
      loader: '@svgr/webpack',
      options: {
        babel: false,
        icon: true,
      },
    },
  ],
};
```

```jsx
import React from 'react';
import Icon from '@ant-design/icons';
import MessageSvg from 'path/to/message.svg'; // path to your '*.svg' file.
import ReactDOM from 'react-dom/client';

// in create-react-app:
// import { ReactComponent as MessageSvg } from 'path/to/message.svg';

ReactDOM.createRoot(mountNode).render(<Icon component={MessageSvg} />);
```

svg Icon 에서 사용 가능한 속성:

| 속성      | 설명                               | 타입             | readonly 값    | 버전 |
| --------- | ---------------------------------- | ---------------- | -------------- | ---- |
| className | 다 그려진 `svg` 요소의 className   | string           | -              |      |
| fill      | `svg` 요소를 그릴 때 사용되는 색상 | string           | `currentColor` |      |
| height    | `svg` 요소의 `height` 값           | string \| number | `1em`          |      |
| style     | 다 그려진 `svg` 요소의 style       | CSSProperties    | -              |      |
| width     | `svg` 요소의 `width` 값            | string \| number | `1em`          |      |

## 테마 변수 (Design Token)

<ComponentTokenTable component="Icon"></ComponentTokenTable>
