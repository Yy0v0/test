# Yy0v0 · 个人主页

一个轻量的个人主页，纯静态单页，无任何构建步骤 —— 直接用浏览器打开 `index.html` 即可。

**线上地址：** https://yy0v0.github.io/test/

## 页面结构

| 板块 | 说明 |
| --- | --- |
| Hero | 头像字母块、名字与一句话简介 |
| 关于我 | 两段自我介绍 |
| 技能 | 按「硬件 / 创客」「编程」「创作」分组的能力标签 |
| 项目 | 三张项目卡片，悬停上浮 |

## 目录

```
.
├── index.html      # 全部内容（HTML + CSS + JS 内联，方便直接改）
├── .gitignore
└── README.md
```

## 本地预览

直接双击 `index.html` 就能看。若想用本地服务器：

```bash
python -m http.server 8000
# 然后打开 http://localhost:8000
```

## 怎么改内容

全部在 `index.html` 里，几个关键位置：

- **名字 / 一句话简介**：`<header class="hero">` 里的 `<h1>` 和 `.tagline`
- **关于我**：`<section id="about">`
- **技能标签**：`<section id="skills">`，每行一个 `<span class="tag">`
- **项目卡片**：`<section id="projects">`，复制 `.card` 整块即可新增一个项目
- **主题色**：文件顶部 `:root` 里的 `--accent`（默认蓝色 `#2563eb`）

改完提交推送即可，GitHub Pages 会自动重新构建：

```bash
git add -A
git commit -m "update: ..."
git push
```

## 部署

托管在 GitHub Pages，来源为 `main` 分支根目录。推送后约一分钟生效。
