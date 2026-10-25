# CLAUDE.md

《计算机寓言》是一本纯静态的中文技术寓言集。每则先讲一个中国旧行当里的故事，再在“谜底”区揭晓一个计算机概念，并附元素→概念对照表与术语详解。

## 目录结构

站点文件全部在 `docs/` 下，根目录只留 `README.md`、`CLAUDE.md` 与仓库配置。

- `docs/index.html` —— 目录页
- `docs/assets/book.css` —— 纸色、版心、书口、页脚等共用样式
- `docs/assets/fable.css` —— 正文、对白、谜底的排版
- `docs/assets/index.css` —— 目录页样式
- `docs/assets/site.css` —— 右上角 GitHub 入口
- `docs/` 下其余 `.html` 为各篇正文，各自独立，文件名即篇名

## 体例与设计

- 排版取意于刻本：纸色、朱印、双线；谜底换一张稍深的纸。
- 每篇有自己的印章字（题头上方）与第二墨色；颜色分别定义在 `docs/assets/book.css` 的 `.fable-N` 与 `docs/assets/index.css` 的 `.entry-N`。
- 单一版心：题头、故事、谜底、页脚共用同一条左缘。
- 不做页边批注，也不做篇目编号（后续按分类组织）。
- 副标题只点冲突，不点破概念；故事在前，谜底在后。
- 中文正文不拉字距、不用两端对齐，引号用全角。
- 正文骨架依次为：题头（印章 / 标题 / 副标题 / 双线）、`section.story`（段落、`dialogue`、`chapter-mark`）、`section.reveal`（`reveal-intro`、`mapping`、`terms`）、页脚。新篇沿用既有骨架与共用样式，不要另起炉灶。

## 新增一篇

1. 以现有篇目为骨架，在 `docs/` 下新建 `<篇名>.html`，`<body>` 上写 `class="fable fable-N"`。
2. 在 `docs/assets/book.css` 与 `docs/assets/index.css` 各加一条 `fable-N` / `entry-N`，给出本篇的第二墨色。
3. 在 `docs/index.html` 的目录里登记篇名、副标题与概念，并同步更新篇数说明。
4. 在 `README.md` 的篇目表中补一行，链接指向 GitHub Pages 的在线阅读地址。
5. 校验内链，提交并推送。

## 部署

本站为纯静态页面，由 GitHub Pages 托管 `main` 分支的 `/docs` 目录，无需构建。新增一篇后，把它登记进 `docs/index.html` 的目录并推送即可。
