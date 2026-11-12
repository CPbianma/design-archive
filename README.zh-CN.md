# Design Archive / 设计档案

**[English](README.md) · 中文**

一个可以持续扩充的视觉方向仓库，用于作品集、技术文档、软件界面与演示文稿。每种风格都独立存放；需要时复制对应的 style package，不必引入框架或构建工具。

![Research Archive 风格封面](styles/research-archive/assets/cover.svg)

## 风格目录

| 风格 | 特征 | 包含内容 | 预览 |
| --- | --- | --- | --- |
| [Research Archive](styles/research-archive/) | 暖色中性色、精细分隔线、技术元数据、编辑式留白 | CSS + JSON tokens、组件、明暗主题、响应式示例 | [打开](styles/research-archive/preview.html) |

预览页右上角支持 **CN／EN** 与 **System／Light／Dark** 切换。CN 版保留技术名词、代码与必要英文标签，只把介绍和使用说明改为中文。

## 使用仓库

在 GitHub 上选择 **Use this template**，或克隆后复制所需风格包：

```sh
git clone https://github.com/CPbianma/design-archive.git
```

直接用浏览器打开 `styles/research-archive/preview.html`，无需启动服务。

Web 项目先引入 tokens，再引入组件：

```html
<link rel="stylesheet" href="styles/research-archive/tokens.css">
<link rel="stylesheet" href="styles/research-archive/components.css">
```

SVG、幻灯片或其他非 CSS 工具可以读取 `tokens.json`。不同媒介共用相同的颜色角色和字体层级。

## 目录约定

```text
styles/
└── research-archive/
    ├── assets/cover.svg
    ├── components.css
    ├── tokens.css
    ├── tokens.json
    ├── preview.html
    ├── README.md
    └── README.zh-CN.md
catalog.json
CONTRIBUTING.md
```

`styles/` 下每个目录都是一种完整视觉方向。个人姓名、项目链接等具体内容只放在示例里，不写进通用 tokens 或组件。

## 设计原则

- 按用途定义颜色，不按某个组件的名字定义颜色。
- 明暗主题分别调校，不做简单反色。
- 用少量字体角色区分展示、正文和技术标签。
- 优先通过间距与对齐建立层级，少用装饰容器。
- 核心不依赖框架和运行时服务。
- 发布前检查键盘焦点、减少动态效果、手机排版和文字对比度。

## 添加新风格

目录结构与检查清单见 [CONTRIBUTING.md](CONTRIBUTING.md)。新风格应命名一个可复用的大类，不要绑定某位客户或某一次任务。

## 实际案例

Research Archive 已用于 [Peng Cai 的 GitHub Profile](https://github.com/CPbianma)。Profile 提供中文主页与 [English README](https://github.com/CPbianma/CPbianma/blob/main/README.en.md)，SVG 采用同一组色彩角色，并把字体转为轮廓以保证跨平台一致。

## 许可证

[MIT](LICENSE)
