# 开发注意事项

## 组件

- 属性名，监听事件名称都用 camel-case 格式；
- 子组件监听事件名称前加 "on",如 `@click="onClick"` 父组件监听事件 `@click="click"`

## Class 命名

- 每页最外层 class 命名为 `container pagename-cotainer`
- 每个功能模块命名依次为 `pagename-module pagename-module-container`