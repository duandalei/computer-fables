# CLAUDE.md

《计算机寓言》是一本纯静态的中文技术寓言集。每则先讲一个中国旧行当里的故事，再在“谜底”区揭晓一个计算机概念，并附元素→概念对照表与术语详解。

## 目录结构

站点文件全部在 `docs/` 下，根目录只留 `README.md`、`CLAUDE.md` 与仓库配置。

- `docs/index.html` —— 全书章目，只列各章
- `docs/chapter-1.html` ～ `docs/chapter-4.html` —— 各章章目页，列出该章各节
- `docs/assets/book.css` —— 纸色、版心、书口、页脚等共用样式
- `docs/assets/fable.css` —— 正文、对白、谜底的排版
- `docs/assets/index.css` —— 章目页与章内目录的样式
- `docs/assets/site.css` —— 右上角 GitHub 入口
- `docs/` 下其余 `.html` 为各篇正文，各自独立，文件名即篇名

## 体例与设计

- 排版取意于刻本：纸色、朱印、双线；谜底换一张稍深的纸。
- 每篇有自己的印章字（题头上方）与第二墨色；颜色分别定义在 `docs/assets/book.css` 的 `.fable-N` 与 `docs/assets/index.css` 的 `.entry-N`。
- 单一版心：题头、故事、谜底、页脚共用同一条左缘。
- 不做页边批注；编号只出现在目录页，正文不编号。
- 副标题只点冲突，不点破概念；故事在前，谜底在后。
- 中文正文不拉字距、不用两端对齐，引号用全角。
- 正文骨架依次为：题头（印章 / 标题 / 副标题 / 双线）、`section.story`（段落、`dialogue`、`chapter-mark`）、`section.reveal`（`reveal-intro`、`mapping`、`terms`）、页脚。新篇沿用既有骨架与共用样式，不要另起炉灶。

## 章节归属与次序

- 新篇先归入对应章目页（`docs/chapter-N.html`）的节次；现有各章都容不下时，就另立一章，新建章目页，并在 `docs/index.html` 登记章名、章序、章注与目录版式。
- 正文页脚的返回链接指向所属章目页，章目页的返回链接再指向 `docs/index.html`。
- 章内的小节按学习认知的次序排列：先修概念在前，依赖它的在后。新增一篇后要复核本章的次序，必要时挪动已有篇目，不要把新篇一律缀在末尾。
- 若发现已有篇目中的某个概念与眼下要写的概念宜合为一篇，先向作者说明理由，得到同意后再合并，并同步目录、篇数说明与 README。
- 若写到某处，发现另一个本篇尚未涉及的概念与眼下概念宜并置讲清，可以一并写进本篇，不必另立篇目。
- 若眼下概念需要读者先懂另一个尚未写过的概念，先问作者是否另写一篇前置篇目，不要在本篇里草草带过。

## 新增一篇

1. 以现有篇目为骨架，在 `docs/` 下新建 `<篇名>.html`，`<body>` 上写 `class="fable fable-N"`。
2. 在 `docs/assets/book.css` 与 `docs/assets/index.css` 各加一条 `fable-N` / `entry-N`，给出本篇的第二墨色。
3. 按〈章节归属与次序〉，在对应章目页的目录里登记篇名、副标题与概念；若新立一章，再新建章目页（`<body>` 写 `chapter-page--N`，并在 `docs/assets/index.css` 补上 `--chapter-no: N`），在 `docs/index.html` 补上该章。同步更新首页、章目页与页脚的篇数说明。
4. 在 `README.md` 的篇目表中补一行，链接指向 GitHub Pages 的在线阅读地址。
5. 校验内链，提交并推送。

## 部署

本站为纯静态页面，由 GitHub Pages 托管 `main` 分支的 `/docs` 目录，无需构建。新增一篇后，把它登记进对应章目页并推送即可；新立一章时，再在 `docs/index.html` 补上该章。
