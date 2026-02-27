---
category: 导航
---

# GoodsAction 商品导航

### 介绍

用于为商品相关操作提供便捷的底部导航。

### 引入

在`app.json`或`index.json`中引入组件，详细介绍见[快速上手](/material/smartui?comId=help-getting-started&appType=miniapp)。

```json
"usingComponents": {
  "smart-goods-action": "@tuya-miniapp/smart-ui/lib/goods-action/index",
  "smart-goods-action-icon": "@tuya-miniapp/smart-ui/lib/goods-action-icon/index",
  "smart-goods-action-button": "@tuya-miniapp/smart-ui/lib/goods-action-button/index"
}
```

## 代码演示

### 基础用法

```html
<smart-goods-action>
  <smart-goods-action-icon icon="chat-o" text="客服" />
  <smart-goods-action-icon icon="cart-o" text="购物车" />
  <smart-goods-action-button text="加入购物车" type="warning" />
  <smart-goods-action-button text="立即购买" />
</smart-goods-action>
```

### 提示信息

通过 `info` 属性在图标右上角展示提示信息，通过 `dot` 属性展示小红点。

```html
<smart-goods-action>
  <smart-goods-action-icon icon="chat-o" text="客服" dot />
  <smart-goods-action-icon icon="cart-o" text="购物车" info="5" />
  <smart-goods-action-icon icon="shop-o" text="店铺" />
  <smart-goods-action-button text="加入购物车" type="warning" />
  <smart-goods-action-button text="立即购买" />
</smart-goods-action>
```

### 自定义按钮颜色

通过 `color` 属性可以自定义按钮的颜色。

```html
<smart-goods-action>
  <smart-goods-action-icon icon="chat-o" text="客服" />
  <smart-goods-action-icon icon="shop-o" text="店铺" />
  <smart-goods-action-button color="#be99ff" type="warning" text="加入购物车" />
  <smart-goods-action-button color="#7232dd" text="立即购买" />
</smart-goods-action>
```

### 朴素按钮

通过 `plain` 属性将按钮设置为朴素按钮。

```html
<smart-goods-action>
  <smart-goods-action-icon icon="chat-o" text="客服" />
  <smart-goods-action-icon icon="shop-o" text="店铺" />
  <smart-goods-action-button color="#7232dd" text="加入购物车" type="warning" />
  <smart-goods-action-button plain color="#7232dd" text="立即购买" />
</smart-goods-action>
```

## API

### GoodsAction Props

| 参数 | 说明 | 类型 | 默认值 |
| --- | --- | --- | --- |
| safe-area-inset-bottom | 是否为 iPhoneX 留出底部安全距离 | _boolean_ | `true` |

### GoodsActionIcon Props

| 参数 | 说明 | 类型 | 默认值 |
| --- | --- | --- | --- |
| text | 按钮文字 | _string_ | - |
| icon | 图标 | _string_ | - |
| icon-class | 图标样式类 | _string_ | - |
| info | 图标右上角提示信息 | _string \| number_ | - |
| dot | 是否显示小红点 | _boolean_ | `false` |
| size | 图标大小，如 `20px` `2em`，默认单位为 `px` | _string_ | `18px` |
| color | 图标颜色 | _string_ | - |
| class-prefix | 图标类名前缀 | _string_ | `smart-icon` |
| disabled | 是否禁用 | _boolean_ | `false` |
| loading | 是否显示为加载状态 | _boolean_ | `false` |
| open-type | 微信开放能力，具体支持可参考 [微信官方文档](https://developers.weixin.qq.com/miniprogram/dev/component/button.html) | _string_ | - |

### GoodsActionButton Props

| 参数 | 说明 | 类型 | 默认值 |
| --- | --- | --- | --- |
| text | 按钮文字 | _string_ | - |
| type | 按钮类型，可选值为 `primary` `warning` `danger` | _string_ | `danger` |
| size | 按钮尺寸，可选值为 `normal` `large` `small` `mini` | _string_ | `normal` |
| color | 按钮颜色，支持传入 `linear-gradient` 渐变色 | _string_ | - |
| plain | 是否为朴素按钮 | _boolean_ | `false` |
| loading | 是否显示为加载状态 | _boolean_ | `false` |
| disabled | 是否禁用 | _boolean_ | `false` |
| open-type | 微信开放能力，具体支持可参考 [微信官方文档](https://developers.weixin.qq.com/miniprogram/dev/component/button.html) | _string_ | - |
| lang | 指定返回用户信息的语言，zh_CN 简体中文，zh_TW 繁体中文，en 英文 | _string_ | `en` |
| session-from | 会话来源 | _string_ | - |
| send-message-title | 会话内消息卡片标题 | _string_ | 当前标题 |
| send-message-path | 会话内消息卡片点击跳转小程序路径 | _string_ | 当前分享路径 |
| send-message-img | 会话内消息卡片图片 | _string_ | 截图 |
| show-message-card | 显示会话内消息卡片 | _boolean_ | `false` |
| app-parameter | 打开 APP 时，向 APP 传递的参数 | _string_ | - |

### GoodsActionIcon Slot

| 名称 | 说明 |
| --- | --- |
| icon | 自定义图标 |

### GoodsActionButton Slot

| 名称 | 说明 |
| --- | --- |
| - | 按钮显示内容 |

### GoodsActionIcon Event

| 事件名 | 说明 | 参数 |
| --- | --- | --- |
| bind:click | 点击图标时触发 | - |

### GoodsActionButton Event

| 事件名 | 说明 | 参数 |
| --- | --- | --- |
| bind:click | 点击按钮时触发 | - |

### GoodsActionIcon 外部样式类

| 类名 | 说明 |
| --- | --- |
| icon-class | 图标样式类 |
| text-class | 文字样式类 |
| info-class | 图标右上角提示信息样式类 |

### GoodsActionButton 外部样式类

| 类名 | 说明 |
| --- | --- |
| custom-class | 根节点样式类 |

### 样式变量

组件提供了下列 CSS 变量，可用于自定义样式，使用方法请参考 [ConfigProvider 组件](/material/smartui?comId=config-provider&appType=miniapp)。

| 名称 | 默认值 | 描述 |
| --- | --- | --- |
| --goods-action-background-color | _var(--app-B4, #ffffff)_ | 背景颜色 |
| --goods-action-height | _48px_ | 高度 |
| --goods-action-icon-width | _48px_ | 图标宽度 |
| --goods-action-icon-height | _48px_ | 图标高度 |
| --goods-action-icon-color | _var(--app-B4-N2, rgba(0, 0, 0, 0.7))_ | 图标颜色 |
| --goods-action-icon-size | _18px_ | 图标大小 |
| --goods-action-icon-font-size | _10px_ | 图标文字大小 |
| --goods-action-icon-text-color | _#646566_ | 图标文字颜色 |
| --goods-action-button-height | _48px_ | 按钮高度 |
| --goods-action-button-line-height | _20px_ | 按钮行高 |
| --goods-action-button-border-radius | _999px_ | 按钮圆角 |
| --goods-action-button-warning-color | _linear-gradient(to right, #ffd01e, #ff8917)_ | 警告按钮颜色 |
| --goods-action-button-danger-color | _linear-gradient(to right, #ff6034, #ee0a24)_ | 危险按钮颜色 |
| --goods-action-button-plain-color | _var(--app-B4, #ffffff)_ | 朴素按钮颜色 |
