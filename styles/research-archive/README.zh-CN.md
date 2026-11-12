# Research Archive / 研究档案

**[English](README.md) · 中文 · v1.0.0**

一套用于研究型作品集、软件索引、项目文档和技术个人主页的暖色视觉方向。它借用研究档案里的字段、日期、索引和表格元数据，以克制的软件配色组织内容。

这套风格不是玻璃拟态 AI 仪表盘，也不是生活方式类的米色 editorial。层级来自文字对齐与分隔线，而不是阴影。

## 文件

- `tokens.css`：颜色、字体、间距、边框、布局和 motion variables。
- `tokens.json`：供 SVG 生成器、幻灯片工具及其他非 CSS 媒介使用。
- `components.css`：可选的记录网格、索引列表、标签和按钮。
- `preview.html`：独立风格指南，支持 CN／EN 和明暗主题切换。
- `assets/cover.svg`：目录与社交预览封面。

## 核心色板

| 角色 | 浅色 | 深色 | 用途 |
| --- | --- | --- | --- |
| Page | `#E8E7E1` | `#151712` | 主表面之外的画布 |
| Paper | `#F7F6F0` | `#20231C` | 主要阅读表面 |
| Ink | `#292C26` | `#E9E9DF` | 标题与正文 |
| Muted | `#5F6459` | `#B4B7AA` | 描述与次要信息 |
| Faint | `#6A6F64` | `#A2A797` | 小标签与元数据 |
| Line | `#D2D2C6` | `#3C4135` | 内部分隔线 |
| Strong line | `#A7AA9C` | `#646B58` | 外框与主要分区 |
| Accent | `#A94F36` | `#D98565` | 索引、箭头、数据点或焦点 |

核心正文和强调色与 Paper 的对比度：浅色主题最低 4.76:1，深色主题最低 5.68:1。修改颜色后需要重新检查。

## 字体角色

- **展示：** Archivo Medium，紧凑字距，适中字重。
- **正文：** IBM Plex Sans Regular；中文使用 Noto Sans SC，行宽保持在舒适范围。
- **技术标签：** IBM Plex Mono Regular／Medium，用于英文大写标签、日期、索引与技术信息。

中文版本不要把所有内容强行翻译。项目名、技术栈、代码、专业缩写与必要标签可以保留英文；介绍性旁白、使用说明和项目描述使用自然中文。

## Web 使用

```html
<link rel="stylesheet" href="tokens.css">
<link rel="stylesheet" href="components.css">
```

在根元素设置 `data-theme="light"` 或 `data-theme="dark"` 可明确指定主题；不设置时跟随系统。

```html
<section class="ra-surface">
  <p class="ra-label">01 / Research</p>
  <h1 class="ra-display">研究健康数据，做真正可用的软件。</h1>
</section>
```

## SVG 与 GitHub

SVG 可以使用 `tokens.json` 中的颜色，并通过内部的 `prefers-color-scheme` media query 适配明暗主题。复杂桌面构图在移动端应使用独立版本，而不是整体缩小。

需要跨平台完全一致时，把成品文字转为矢量轮廓，同时保留 `<title>`、`<desc>` 和 image alt。中英文混排要分别检查：英文按单词换行，中文按字符换行，并避免中文标点出现在行首。

## 排版规则

1. 先组织姓名、方向、当前状态和精选项目，再考虑装饰。
2. 使用一像素分隔线和充足留白，不用悬浮卡片堆叠层级。
3. 保持方形或近方形转角，避免通用胶囊和玻璃面板。
4. 陶土色只标记值或动作，不大面积铺色。
5. 编号必须代表真实索引、顺序或时间关系。
6. 小标签仍需可读，长文案应自然换行，不靠缩小字号硬塞。
7. CN 与 EN 共享网格和 tokens，但分别调整文字长度与断行。

## 适用范围

研究与工程作品集、精选项目索引、技术 CV、文档封面、实验室或工作室网站，以及数据感较强的编辑页面。

高情绪消费品牌、 playful illustration、密集分析仪表盘，或高度依赖语义状态色的界面，应选择其他方向或明确扩展本风格。
