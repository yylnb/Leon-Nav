# leonyeung.com 视觉识别手册

薄荷青绿 · 黑 · 白

定稿日期 2026 年 11 月 23 日 · 版本 1.0

本手册以 Leon-Nav 提交 `254608d` 的页面为视觉基准，供后续网站、子项目和组件设计使用。品牌通过明亮的薄荷青绿背景、黑色结构、白色内容表面、大字号数字与直角轮廓建立识别。

[打开可视化手册](./mint-teal-vi.html) · [查看当前网站](../index.html) · [查看实际样式](../styles.css)

## 品牌标识

文字标识统一写作 `leonyeung.com`，保持小写。个人署名使用 `Leon Yeung`。项目名沿用当前站点中的正式写法，例如 `FinanceYY`、`NewsYY` 和 `YProgram`。

导航中的标识由青绿色方块、黑色字母 `Y` 和白色域名组成，放在黑色横栏内。当前字母方块为 `34 × 34px`，与域名间距 `11px`。用于其他尺寸时等比例调整，四周至少留出半个方块宽度的空白。

浏览器图标直接使用仓库中的 [favicon.svg](../assets/favicon.svg)，由黑底、白色字形与薄荷青绿方块组成。输出图标时保持原始比例，使用方形画布。

## 色彩体系

| 角色 | 名称 | 色值 | 用途 |
| --- | --- | --- | --- |
| 品牌主色 | 薄荷青绿 | `#36E0BB` | 页面外壳、首屏、品牌方块、重点色面 |
| 主文字与结构色 | 墨黑 | `#111111` | 标题、正文、主按钮、边框、硬阴影 |
| 内容表面 | 白色 | `#FFFFFF` | 卡片、表单、阅读区域、深底文字 |
| 文字强调色 | 深青绿 | `#007B70` | 白底上的卡片序号、正文链接、重要数字 |
| 次级文字 | 深灰 | `#444444` | 白底说明、域名、辅助信息 |

薄荷青绿和深青绿属于同一套品牌色的两个用途。前者承担大色面，后者承担白底上的文字强调。当前卡片数字使用深青绿，全部卡片采用统一的白底、黑字和黑边框。

页面外壳铺薄荷青绿，内容卡片铺白色，黑色集中在标题、导航和结构线条。内容越密集，白色阅读区域可以越大。产品页延续这一角色关系，根据内容调整面积。

### 文字和背景搭配

以下数值按 sRGB 相对亮度计算，保留两位小数。

| 前景 | 背景 | 对比度 | 使用范围 |
| --- | --- | ---: | --- |
| 墨黑 | 薄荷青绿 | 11.27∶1 | 首屏标题、说明、标签、焦点环 |
| 墨黑 | 白色 | 18.88∶1 | 正文、卡片标题、表单 |
| 白色 | 墨黑 | 18.88∶1 | 黑色导航、主按钮、深色内容块 |
| 深灰 | 白色 | 9.74∶1 | 卡片说明、域名、辅助文案 |
| 深青绿 | 白色 | 5.16∶1 | 序号、链接、强调文字 |
| 白色 | 薄荷青绿 | 1.68∶1 | 仅作无信息的装饰图形组合 |

普通文字采用对比度达到 `4.5∶1` 的组合。大字采用至少 `3∶1` 的组合。薄荷青绿底统一搭配墨黑文字，黑底搭配白字或薄荷青绿字，白底强调文字采用深青绿。

## 字体与信息层级

| 内容 | 字体 | 字重与尺寸 |
| --- | --- | --- |
| 英文主标题、项目名、序号 | Bricolage Grotesque | `800` |
| 拉丁正文、域名、界面文字 | Manrope | `500 / 700 / 800` |
| 中文文字 | Noto Sans SC | 正文 `400 / 500`，标题 `700 / 900` |
| 系统回退 | Microsoft YaHei、sans-serif | 跟随相应文本层级 |

主标题采用 `clamp(3.8rem, 8vw, 7rem)`、行高 `.92`、字距 `-.075em`，在 `500px` 以下改为 `2.8rem`。这组紧凑参数用于短英文品牌标题。中文标题与多行标题使用至少 `1.2` 的行高和接近正常的字距，按实际内容检查换行。

卡片标题采用 `clamp(2rem, 3.4vw, 3rem)`、行高 `1.12`。卡片说明采用 `.9375rem`、行高 `1.7`。域名采用 `.72rem`，手机端 `.7rem`。独立产品页的长正文以 `1rem`、行高 `1.7` 为起点。

大序号采用等宽数字特性 `lining-nums tabular-nums`，桌面 `6rem`，手机 `4rem`。导航中的装饰序号带 `aria-hidden="true"`，信息顺序由 DOM 和链接名称表达。

## 形状、边框和留白

卡片、按钮、标签、输入框与品牌方块统一使用 `border-radius: 0`。主要轮廓为 `2px solid #111111`，内容内部的分割线为 `1px solid #111111`。

交互卡片悬停时出现 `7px 7px 0 #111111` 硬阴影，同时向左上方移动 `3px`。按钮沿用方形轮廓，可采用较小的 `4px 4px 0` 硬阴影。每个区域使用统一的阴影方向。

布局间距优先使用 `8 / 12 / 16 / 20 / 24 / 28 / 32 / 40 / 48 / 56px`。当前导航在卡片中使用 `28px` 内边距和 `20px` 内容间距，手机端内边距为 `22px`。

## 页面结构与响应式

页面顺序为品牌栏、介绍、项目标题与数量、项目网格、页脚。阅读区域最大宽度 `1160px`，桌面左右总留白至少 `40px`。

| 视口 | 布局 |
| --- | --- |
| `1040px` 及以上 | 12 列网格，卡片按 `7/5`、`5/7` 交错排列 |
| `821–1039px` | 两列等宽卡片 |
| `820px` 及以下 | 单列，内容最大宽度 `680px`，左右总留白 `28px` |
| `500px` 及以下 | 左右总留白 `20px`，卡片间距 `14px`，标题与数字缩小 |

当前卡片桌面最小高度为 `288px`，手机为 `240px`，内容增长时自然撑高。字体和布局尺寸以浏览器默认 `16px` 根字号为参照，支持用户缩放。

## 卡片与箭头

卡片信息顺序固定为右上角大序号、项目名称与说明、域名与访问箭头。整张项目卡片使用一个 `<a>` 元素，链接名包含项目名称和用途。箭头作为卡片链接的一部分，使用 `aria-hidden="true"`。

默认箭头为 `38 × 38px` 方框、`2px` 黑边、黑色箭头。鼠标位于卡片或箭头上时，卡片左上移并出现硬阴影，箭头方框变为黑底白字，箭头整体向右上移动 `2px`。键盘聚焦卡片时也显示黑底白字箭头。

白底卡片内的描述和域名使用深灰，序号统一使用深青绿。新增项目沿用相同的颜色角色和层级。

## 按钮

本节将已确定的黑白青绿风格扩展到后续产品控件。按钮最小高度 `44px`，水平内边距 `18px`，文字字重 `800`，边框 `2px`，圆角 `0`。图标按钮的可点击区域至少为 `44 × 44px`。

| 类型 | 默认 | 悬停 | 使用场景 |
| --- | --- | --- | --- |
| 主要按钮 | 墨黑底、白字、墨黑边 | 左上移 `2px`，出现硬阴影 | 保存、提交、开始使用 |
| 次要按钮 | 白底、墨黑字、墨黑边 | 薄荷青绿底，出现硬阴影 | 返回、查看说明、取消 |
| 品牌按钮 | 薄荷青绿底、墨黑字、墨黑边 | 左上移 `2px`，出现硬阴影 | 黑白内容区域中的品牌入口 |
| 禁用按钮 | 保留配色，透明度 `.45` | 保持禁用外观 | 条件尚未满足的操作 |

按钮按下时回到原位，阴影消失。禁用按钮使用原生 `disabled`，配合说明文字告知原因。按钮文字描述动作，跳转动作使用 `<a>`，提交和界面操作使用 `<button>`。

## 链接、导航、表单和状态

白底正文链接使用深青绿、`2px` 下划线与 `4px` 下划线偏移，悬停时加粗下划线。青绿色底正文链接采用墨黑与下划线。导航链接使用墨黑，当前项增加 `2px` 底线，并通过 `aria-current="page"` 标明位置。

表单使用白底、墨黑字、`2px` 墨黑边框和直角。输入框高度至少 `44px`，标签放在控件上方，说明紧邻控件。输入焦点采用 `3px` 墨黑外轮廓，外移 `4px`。错误和结果使用明确的文字反馈，表单错误关联 `aria-describedby`，错误控件设置 `aria-invalid="true"`。

状态标签采用直角轮廓和简短文字。白底上的普通标签使用白底黑字黑边，品牌标签使用青绿底黑字。状态含义同时由文字或图标表达，品牌青绿承担品牌识别。涉及金融涨跌等领域语义时，按产品已有约定使用文字、符号和状态色。

## 焦点与动效

浅底和青绿色底上的链接、按钮与输入框使用 `3px` 墨黑焦点环，外移 `4px`。黑色区域中的控件使用白色焦点环。当前导航对 `.brand:focus-visible` 使用白色轮廓。

卡片和箭头交互时长 `220ms`，位移动画使用 `cubic-bezier(0.22, 1, 0.36, 1)`。悬停位移仅在 `(hover: hover) and (pointer: fine)` 条件下开启。页面进入动画时长约 `600–700ms`，卡片依次延迟出现。

尊重 `prefers-reduced-motion: reduce`，关闭入场、平滑滚动与位移动画，保留颜色和轮廓提供的状态反馈。触屏通过按下态与焦点态提供反馈。

## 可复用 CSS 变量

以下名称与当前导航的变量保持一致，按钮与表单可引用同一组变量。

```css
:root {
  --teal: #36E0BB;
  --teal-ink: #007B70;
  --black: #111111;
  --surface: #FFFFFF;
  --muted: #444444;
  --line: #111111;
  --shadow: 7px 7px 0 var(--black);
  --ease-out: cubic-bezier(0.22, 1, 0.36, 1);
  --display: "Bricolage Grotesque", "Noto Sans SC", "Microsoft YaHei", sans-serif;
  --body: "Manrope", "Noto Sans SC", "Microsoft YaHei", sans-serif;
}

.button {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  gap: 8px;
  min-height: 44px;
  padding: 10px 18px;
  border: 2px solid var(--black);
  border-radius: 0;
  color: var(--surface);
  background: var(--black);
  font: inherit;
  font-weight: 800;
  text-decoration: none;
  cursor: pointer;
  transition: transform 220ms var(--ease-out), box-shadow 220ms ease;
}

.button-secondary { color: var(--black); background: var(--surface); }
.button-brand { color: var(--black); background: var(--teal); }
.button:disabled { opacity: .45; cursor: not-allowed; }

@media (hover: hover) and (pointer: fine) {
  .button:enabled:hover, a.button:hover {
    transform: translate(-2px, -2px);
    box-shadow: 4px 4px 0 var(--black);
  }
  .button-secondary:hover { background: var(--teal); }
}

.button:active { transform: none; box-shadow: none; }
:where(a, button, input, select, textarea):focus-visible {
  outline: 3px solid var(--black);
  outline-offset: 4px;
}
.on-dark :where(a, button, input, select, textarea):focus-visible {
  outline-color: var(--surface);
}

@media (prefers-reduced-motion: reduce) {
  *, *::before, *::after {
    scroll-behavior: auto !important;
    animation: none !important;
    transition: none !important;
  }
  .button:enabled:hover, a.button:hover { transform: none; }
}
```

## 后续网站使用方式

新页面先引用上述变量，再确定外壳、内容表面和正文层级。保留青绿色品牌区域、统一的卡片结构、直角和黑色轮廓。按钮按操作优先级选择对应类型，白底数字和链接引用深青绿。

交付时检查实际文案换行、手机布局、键盘焦点、触屏访问和减少动态效果设置，并确认页面使用 `leonyeung.com` 域名体系。

## 历史手册备份

黄油可可规范与 HTML 展示页已按原始字节复制到 `archive` 目录，原文件路径继续可访问。备份中的相对资源引用仍以原目录为基准，阅读其配色来源时可打开原路径下的文件。

- [旧规范备份](./archive/butter-cocoa-guidelines.md)
- [旧展示页备份](./archive/butter-cocoa-guidelines-demo.html)
- [旧规范原路径](./butter-cocoa-guidelines.md)
- [旧展示页原路径](./butter-cocoa-guidelines-demo.html)

历史手册记录黄油可可版本的配色与圆角设定。本手册记录 2026 年 11 月 23 日确定的薄荷青绿版本。
