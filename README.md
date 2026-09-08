# Portfolio · 个人作品集网站

一个**零依赖的响应式静态作品集**网站，用于求职场景向 HR 展示个人项目与技术能力。

纯 HTML/CSS/JS 构建，无框架、无构建步骤，打开即用、部署秒级完成。

> 在线预览：https://2c9d53b84b984f54b37703e7367d7d02.app.workbuddy.link

## ✨ 特性

- 🌍 **中英双语一键切换**——内容数据驱动，同一套结构与样式渲染两种语言
- 🎨 **手写设计系统**——暖纸张底色 + 深墨文字 + 朱红强调色，CSS 变量集中管理主题
- 📱 **完全响应式**——桌面 / 平板 / 手机自适应布局
- 🚀 **零依赖**——无框架、无构建工具、无外部 CDN，单个静态目录即可托管
- ♿ **可访问性**——语义化 HTML、键盘可导航、`prefers-reduced-motion` 支持

## 🧩 页面板块

| 板块 | 说明 |
| --- | --- |
| Hero 首屏 | 一句话定位 + 核心事实栏 + 行动按钮 |
| Selected Work | 代表项目卡片：简介 / 技术栈 / 亮点 / 链接 |
| Skills | 分组技能图谱 |
| Journey | 工作与教育时间线 |
| Contact | 联系方式、简历 PDF 下载、二维码 |

## 🛠 技术栈

- HTML5 语义化结构
- CSS3：自定义属性（变量）、Grid/Flex、媒体查询、动效（尊重系统减弱动效设置）
- Vanilla JavaScript：DOM 渲染、语言状态管理（`localStorage` 记忆偏好）、主题切换

## 🚀 本地运行

任选一种，浏览器打开对应地址：

```bash
# Python
python -m http.server 8000

# Node
npx serve .
```

## 📂 目录结构

```
portfolio-site/
├── index.html          # 页面结构骨架
├── assets/
│   ├── styles.css      # 设计系统与全部样式（主题变量在 :root）
│   ├── app.js          # 中英文内容数据 + 渲染与交互逻辑
│   ├── resume-zh.pdf   # 中文简历
│   └── resume-en.pdf   # English Résumé
└── scripts/
    └── gen_resume_pdf.py  # 生成简历 PDF 的工具脚本（Python 标准库）
```

## 📝 维护提示

- **内容与文案**集中在 `assets/app.js`（`L.zh` / `L.en` 两份数据），改内容不需要动结构。
- **简历 PDF**：替换 `assets/` 下同名文件即自动生效。

---

© 2026 · Built with plain HTML/CSS/JS
