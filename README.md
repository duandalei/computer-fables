# 计算机寓言 · Computer Fables

用中国旧行当的故事，讲计算机里的一些简单概念。每一则先讲故事，再揭谜底，最后附上与技术概念的逐条对照。

**在线阅读：<https://duandalei.github.io/computer-fables/>**

## 篇目

| | 寓言 | 概念 |
|---|---|---|
| 壹 | [碎成一百片的信](碎成一百片的信.html) | 分组交换与 TCP/IP |
| 贰 | [记住每一场雨的人](记住每一场雨的人.html) | 过拟合 |
| 叁 | [随班戏楼](随班戏楼.html) | Docker 与容器化 |

## 结构

- `index.html` —— 目录页
- `assets/fable.css` —— 各篇共用的排版样式
- `assets/index.css` —— 目录页样式
- 三篇正文各自是独立的 HTML 文件

## 部署

本站为纯静态页面，由 GitHub Pages 直接托管 `main` 分支根目录，无需构建。新增一篇后，把它登记进 `index.html` 的目录并推送即可。
