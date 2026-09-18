# 《AI System 原理 —— 从一个 Token，到一个 AI System》

[![Build](https://github.com/yiyan-yixing/ai-system-book/actions/workflows/book-site.yml/badge.svg)](https://github.com/yiyan-yixing/ai-system-book/actions/workflows/book-site.yml)
[![在线阅读](https://img.shields.io/badge/在线阅读-yiyan--yixing.github.io-blue)](https://yiyan-yixing.github.io/ai-system-book/)
[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/license-CC%20BY--NC--SA%204.0-lightgrey.svg)](LICENSE)

!!! tip
    **在线阅读：https://yiyan-yixing.github.io/ai-system-book/**（MkDocs Material，支持全文搜索与深色模式）

多数讲大模型的书，要么停在 Transformer 的结构图，要么停在「怎么调接口」。这本书走第三条路：
**从一个 Token 出发，每讲一个零件，都回答同一个问题——为什么一个 AI System 需要它。**

它不从架构图讲起，而是从一次翻车讲起。作者用大模型做产品，先写出了「接个模型就完事」的幻觉，
然后在接下来的两个月里被现实逼着补上一个又一个零件：小模型、模型池、路由、上下文、记忆、
agent、harness、评估闸门。补完回头一看，这些零件今天都有了行业公认的名字。

全书 15 章 34 节，分上下两篇。上篇「零件」从 Token 与向量讲到预训练与对齐，把模型的内部机制
拆到能画图、能算账；下篇「系统」从 Small Model 一路讲到 AI System，回答「一堆零件怎么拼成
一个能自己运转的系统」。

写作原则只有一条：**每一节都挂真实的实验和真实的账本**。没有一手数据支撑的节，宁可等，不编。

## 内容目录

| 章 | 主题 |
|---|---|
| 序章 | 从一个模型，到一个 AI System |
| 第一章 | Token 与向量 |
| 第二章 | 神经网络在学什么 |
| 第三章 | Transformer：一个架构改变一切 |
| 第四章 | 稀疏与高效：让大模型跑得动 |
| 第五章 | 预训练：模型怎么学 |
| 第六章 | 后训练与对齐 |
| 第七章 | 本地训练：亲手造一个 |
| 第八章 | Small Model |
| 第九章 | Model Pool / Router |
| 第十章 | Context |
| 第十一章 | Knowledge / Graph · Memory |
| 第十二章 | Agent |
| 第十三章 | Harness |
| 第十四章 | Evaluation 与闭环 |
| 第十五章 | AI System |

**当前进度**：13 / 共 34 节正文就绪，其余 21 节为占位（只列节名与一句话导语）。正文分批同步，每发布一节更新一次。

## 适合谁读

- **用大模型做产品的工程师**：想知道「底下到底在发生什么」，而不只是会调接口
- **独立开发者 / 小团队技术负责人**：要自己决定模型放哪、上下文给多少、什么时候该加一层
- **技术决策者**：需要一张能跟团队讲清楚的原理地图

> 不解释「什么是 API」；但会从最底层的 Token 讲起，假定你没有手推过 attention。

## 勘误与反馈

发现正文、图表或数据中的错误，请用 [勘误 Issue](https://github.com/yiyan-yixing/ai-system-book/issues/new?template=erratum.yml) 提交。

## 许可

本书正文采用 [CC BY-NC-SA 4.0](LICENSE) 许可：允许自由阅读、分享、非商业转载，
须保留署名「一言AI行」，改编须以相同协议共享。

## 同步与红线

本站正文由主仓的同步脚本产出，推 `main` 后自动构建发布。同步前会跑一道红线闸：

- **文本**：扫描所有将被提交的文件，命中内部仓库路径、凭据、金额、内部会议/白板引用等模式即**中止发布**。
- **图片（已知盲区）**：图片的**像素内容无法用文本 grep 检测**。已实测发生过「正文文本干净、但配图 PNG 的像素里印着内部仓库路径」的情况。因此：
  - 同步脚本会**列出本批全部二进制文件并要求人工过目**；未经 `--binary-reviewed` 确认，不允许 push。
  - 同时用 OCR（`tesseract -l chi_sim+eng`）对图片做自动扫描，命中内部路径模式即中止。
  - **OCR 有漏检可能**（字体、小字号、艺术字、图形化排版都会降低识别率），OCR 通过 ≠ 图是干净的。**每张新图仍须人工过目一遍。**

## 关于本站

静态站点由 MkDocs Material 构建，推 `main` 自动发布到 GitHub Pages。本地预览：

```bash
pip install -r requirements.txt
mkdir -p .site-src/正文
cp -r manuscripts/. .site-src/正文/
cp archive/outlines/outline.md .site-src/目录大纲.md
cp index.md .site-src/index.md
cp -r assets .site-src/assets
mkdocs serve
```

> 正文按章分目录（`正文/第NN章-章名/`），章导语页是该目录下的 `index.md`；站点首页是封面页
> `index.md`（由 `overrides/home.html` 渲染，数据来自 `mkdocs.yml` 的 `extra.*`）。
