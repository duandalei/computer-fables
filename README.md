# 计算机寓言 · Computer Fables

用中国旧行当的故事，讲计算机里的一些简单概念。每一则先讲故事，再揭谜底，最后附上与技术概念的逐条对照。

**在线阅读：<https://duandalei.github.io/computer-fables/>**

## 篇目

| | 寓言 | 概念 |
|---|---|---|
| 壹 | [碎成一百片的信](碎成一百片的信.html) | 分组交换与 TCP/IP |
| 贰 | [记住每一场雨的人](记住每一场雨的人.html) | 过拟合 |
| 叁 | [随班戏楼](随班戏楼.html) | Docker 与容器化 |
| 肆 | [一纸关引](一纸关引.html) | JWT |
| 伍 | [明码点菜](明码点菜.html) | HTTP 与 HTTPS |

## 结构

- `index.html` —— 目录页
- `assets/book.css` —— 纸色、版心、书口、页脚等共用样式
- `assets/fable.css` —— 正文、对白、谜底的排版
- `assets/index.css` —— 目录页样式
- `assets/site.css` —— 右上角 GitHub 入口
- 五篇正文各自是独立的 HTML 文件

## 设计

排版取意于刻本：纸色、朱印、双线。每篇有自己的印章与第二墨色，谜底换一张稍深的纸，不做页边批注，也不做篇目编号（后续按分类组织）。

## 部署

本站为纯静态页面，由 GitHub Pages 直接托管 `main` 分支根目录，无需构建。新增一篇后，把它登记进 `index.html` 的目录并推送即可。
