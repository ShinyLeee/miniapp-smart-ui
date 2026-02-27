---
category: Display
---

# Info

### Introduction

Used to display prompt information in the upper right corner of the icon.

### Install

Introduce components in `app.json` or `index.json`. For details, see [Quick Start](/material/smartui?comId=help-getting-started&appType=miniapp).

```json
"usingComponents": {
  "smart-info": "@tuya-miniapp/smart-ui/lib/info/index"
}
```

## Demo

### Basic Usage

Set the prompt information content through the `info` attribute.

```html
<smart-info info="5" />
<smart-info info="99+" />
```

### Dot

Display a small red dot through the `dot` attribute.

```html
<smart-info dot />
```

### Custom Style

Customize the style through the `custom-style` attribute.

```html
<smart-info info="5" custom-style="background-color: #1989fa; margin-left: 20px;" />
```

## API

### Props

| Attribute | Description | Type | Default |
| --- | --- | --- | --- |
| info | Info content | _string \| number_ | - |
| dot | Whether to show red dot | _boolean_ | `false` |
| custom-style | Custom style | _string_ | - |

### External Class

| Class | Description |
| --- | --- |
| custom-class | Root node class |

### CSS Variables

The component provides the following CSS variables, which can be used to customize styles. Please refer to [ConfigProvider component](/material/smartui?comId=config-provider&appType=miniapp).

| Name | Default | Description |
| --- | --- | --- |
| --info-size | _14px_ | Info size |
| --info-color | _@white_ | Info text color |
| --info-padding | _0 4px_ | Info padding |
| --info-font-size | _11px_ | Info font size |
| --info-font-weight | _600_ | Info font weight |
| --info-border-width | _0_ | Info border width |
| --info-background-color | _@M2_ | Info background color |
| --info-dot-color | _@M2_ | Dot color |
| --info-dot-size | _8px_ | Dot size |
| --info-font-family | _-apple-system-font, PingFang SC, Helvetica Neue, Arial, sans-serif_ | Info font family |
