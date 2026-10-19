# AmodalEdit Project Page

论文 / 项目主页，部署地址：<https://extionkj.github.io/AmodalEdit/>

基于 [Academic Project Page Template](https://github.com/eliahuhorwitz/Academic-project-page-template)（与 LayoutAD 页面同结构：Bulma + FontAwesome）。

## 目录结构

```
AmodalEdit/
├── index.html              # 页面主体，所有待填内容都以 TODO 注释标出
└── static/
    ├── css/                # bulma / carousel / slider / fontawesome / 自定义 index.css
    ├── js/
    ├── images/
    │   ├── intro_01.png    # Teaser 图（占位）
    │   ├── net_02.png      # 方法框架图（占位）
    │   ├── social_preview.png  # OG / Twitter 预览图 1200x630（占位）
    │   └── favicon.png
    ├── videos/video.mp4    # 需要自己放入
    └── pdfs/paper.pdf      # 需要自己放入
```

## 需要替换的内容

打开 `index.html`，搜索 `TODO` 即可定位所有待填位置：

| 位置 | 说明 |
| --- | --- |
| `<title>` 与 `publication-title` | 论文完整标题 |
| `publication-authors` | 作者名 + 个人主页链接、单位、会议名 |
| `description` / `og:description` | 150–160 字研究简介 |
| `citation_*` / BibTeX 区块 | 引用信息 |
| `og:image` / `social_preview.png` | 社交预览图（1200×630） |
| 按钮链接 | arXiv / Code / Video / Data，不需要的直接删掉对应 `link-block` |
| Abstract | 粘贴摘要 |
| Teaser / Method 图 | 替换 `static/images/intro_01.png`、`net_02.png` |
| `static/pdfs/paper.pdf` | 放论文 PDF |
| `static/videos/video.mp4` | 放演示视频，不用就删掉 Video section |

## 本地预览

```bash
cd <repo-root>
python -m http.server 8000
# 浏览器打开 http://localhost:8000/AmodalEdit/
```

## 发布

推送到 GitHub 后，在仓库 Settings → Pages 里选择 **Deploy from a branch**（main / root）即可。
仓库根目录已有 `.nojekyll`，避免 Jekyll 忽略下划线开头的目录。
