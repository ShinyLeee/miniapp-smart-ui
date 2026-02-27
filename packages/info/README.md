---
category: 展示
---

# Info 信息提示

### 介绍

用于在图标右上角展示提示信息。

### 引入

在`app.json`或`index.json`中引入组件，详细介绍见[快速上手](/material/smartui?comId=help-getting-started&appType=miniapp)。

```json
"usingComponents": {
  "smart-info": "@tuya-miniapp/smart-ui/lib/info/index"
}
```

## 代码演示

### 基础用法

通过 `info` 属性设置提示信息内容。

```html
<smart-info info="5" />
<smart-info info="99+" />
```

### 小红点

通过 `dot` 属性展示小红点。

```html
<smart-info dot />
```

### 自定义样式

可以通过 `custom-style` 属性设置自定义样式。

```html
<smart-info info="5" custom-style="background-color: #1989fa; margin-left: 20px;" />
```

## API

### Props

| 参数 | 说明 | 类型 | 默认值 |
| --- | --- | --- | --- |
| info | 提示信息内容 | _string \| number_ | - |
| dot | 是否显示小红点 | _boolean_ | `false` |
| custom-style | 自定义样式 | _string_ | - |

### 外部样式类

| 类名 | 说明 |
| --- | --- |
| custom-class | 根节点样式类 |

### 样式变量

组件提供了下列 CSS 变量，可用于自定义样式，使用方法请参考 [ConfigProvider 组件](/material/smartui?comId=config-provider&appType=miniapp)。

| 名称 | 默认值 | 描述 |
| --- | --- | --- |
| --info-size | _14px_ | 提示信息尺寸 |
| --info-color | _@white_ | 提示信息文字颜色 |
| --info-padding | _0 4px_ | 提示信息内边距 |
| --info-font-size | _11px_ | 提示信息文字大小 |
| --info-font-weight | _600_ | 提示信息文字粗细 |
| --info-border-width | _0_ | 提示信息边框宽度 |
| --info-background-color | _@M2_ | 提示信息背景颜色 |
| --info-dot-color | _@M2_ | 小红点颜色 |
| --info-dot-size | _8px_ | 小红点尺寸 |
| --info-font-family | _-apple-system-font, PingFang SC, Helvetica Neue, Arial, sans-serif_ | 提示信息字体 |
