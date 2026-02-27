---
category: Navigation
---

# GoodsAction

### Introduction

Used to provide convenient bottom navigation for product-related operations.

### Install

Introduce components in `app.json` or `index.json`. For details, see [Quick Start](/material/smartui?comId=help-getting-started&appType=miniapp).

```json
"usingComponents": {
  "smart-goods-action": "@tuya-miniapp/smart-ui/lib/goods-action/index",
  "smart-goods-action-icon": "@tuya-miniapp/smart-ui/lib/goods-action-icon/index",
  "smart-goods-action-button": "@tuya-miniapp/smart-ui/lib/goods-action-button/index"
}
```

## Demo

### Basic Usage

```html
<smart-goods-action>
  <smart-goods-action-icon icon="chat-o" text="Customer Service" />
  <smart-goods-action-icon icon="cart-o" text="Cart" />
  <smart-goods-action-button text="Add to Cart" type="warning" />
  <smart-goods-action-button text="Buy Now" />
</smart-goods-action>
```

### Icon Badge

Display prompt information in the upper right corner of the icon through the `info` attribute, and display a small red dot through the `dot` attribute.

```html
<smart-goods-action>
  <smart-goods-action-icon icon="chat-o" text="Customer Service" dot />
  <smart-goods-action-icon icon="cart-o" text="Cart" info="5" />
  <smart-goods-action-icon icon="shop-o" text="Shop" />
  <smart-goods-action-button text="Add to Cart" type="warning" />
  <smart-goods-action-button text="Buy Now" />
</smart-goods-action>
```

### Custom Button Color

Customize the button color through the `color` attribute.

```html
<smart-goods-action>
  <smart-goods-action-icon icon="chat-o" text="Customer Service" />
  <smart-goods-action-icon icon="shop-o" text="Shop" />
  <smart-goods-action-button color="#be99ff" type="warning" text="Add to Cart" />
  <smart-goods-action-button color="#7232dd" text="Buy Now" />
</smart-goods-action>
```

### Plain Button

Set the button as a plain button through the `plain` attribute.

```html
<smart-goods-action>
  <smart-goods-action-icon icon="chat-o" text="Customer Service" />
  <smart-goods-action-icon icon="shop-o" text="Shop" />
  <smart-goods-action-button color="#7232dd" text="Add to Cart" type="warning" />
  <smart-goods-action-button plain color="#7232dd" text="Buy Now" />
</smart-goods-action>
```

## API

### GoodsAction Props

| Attribute | Description | Type | Default |
| --- | --- | --- | --- |
| safe-area-inset-bottom | Whether to leave bottom safe distance for iPhoneX | _boolean_ | `true` |

### GoodsActionIcon Props

| Attribute | Description | Type | Default |
| --- | --- | --- | --- |
| text | Button text | _string_ | - |
| icon | Icon name | _string_ | - |
| icon-class | Icon class | _string_ | - |
| info | Info | _string \| number_ | - |
| dot | Whether to show red dot | _boolean_ | `false` |
| size | Icon size | _string_ | `18px` |
| color | Icon color | _string_ | - |
| class-prefix | Class prefix | _string_ | `smart-icon` |
| disabled | Whether to disable button | _boolean_ | `false` |
| loading | Whether to show loading status | _boolean_ | `false` |
| open-type | WeChat open capability | _string_ | - |

### GoodsActionButton Props

| Attribute | Description | Type | Default |
| --- | --- | --- | --- |
| text | Button text | _string_ | - |
| type | Button type, can be set to `primary` `warning` `danger` | _string_ | `danger` |
| size | Button size, can be set to `normal` `large` `small` `mini` | _string_ | `normal` |
| color | Button color, supports linear-gradient | _string_ | - |
| plain | Whether to be plain button | _boolean_ | `false` |
| loading | Whether to show loading status | _boolean_ | `false` |
| disabled | Whether to disable button | _boolean_ | `false` |
| open-type | WeChat open capability | _string_ | - |
| lang | Language for returned user info, zh_CN, zh_TW, en | _string_ | `en` |
| session-from | Session source | _string_ | - |
| send-message-title | Message card title | _string_ | Current title |
| send-message-path | Message card path | _string_ | Current path |
| send-message-img | Message card image | _string_ | Screenshot |
| show-message-card | Whether to show message card | _boolean_ | `false` |
| app-parameter | App parameter | _string_ | - |

### GoodsActionIcon Slot

| Name | Description |
| --- | --- |
| icon | Custom Icon |

### GoodsActionButton Slot

| Name | Description |
| --- | --- |
| - | Button content |

### GoodsActionIcon Event

| Event | Description | Parameters |
| --- | --- | --- |
| bind:click | Triggered when clicked | - |

### GoodsActionButton Event

| Event | Description | Parameters |
| --- | --- | --- |
| bind:click | Triggered when clicked | - |

### GoodsActionIcon External Class

| Class | Description |
| --- | --- |
| icon-class | Icon class |
| text-class | Text class |
| info-class | Info class |

### GoodsActionButton External Class

| Class | Description |
| --- | --- |
| custom-class | Root node class |

### CSS Variables

The component provides the following CSS variables, which can be used to customize styles. Please refer to [ConfigProvider component](/material/smartui?comId=config-provider&appType=miniapp).

| Name | Default | Description |
| --- | --- | --- |
| --goods-action-background-color | _var(--app-B4, #ffffff)_ | Background color |
| --goods-action-height | _48px_ | Height |
| --goods-action-icon-width | _48px_ | Icon width |
| --goods-action-icon-height | _48px_ | Icon height |
| --goods-action-icon-color | _var(--app-B4-N2, rgba(0, 0, 0, 0.7))_ | Icon color |
| --goods-action-icon-size | _18px_ | Icon size |
| --goods-action-icon-font-size | _10px_ | Icon font size |
| --goods-action-icon-text-color | _#646566_ | Icon text color |
| --goods-action-button-height | _48px_ | Button height |
| --goods-action-button-line-height | _20px_ | Button line height |
| --goods-action-button-border-radius | _999px_ | Button border radius |
| --goods-action-button-warning-color | _linear-gradient(to right, #ffd01e, #ff8917)_ | Warning button color |
| --goods-action-button-danger-color | _linear-gradient(to right, #ff6034, #ee0a24)_ | Danger button color |
| --goods-action-button-plain-color | _var(--app-B4, #ffffff)_ | Plain button color |
