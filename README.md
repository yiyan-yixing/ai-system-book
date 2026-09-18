# 《AI System 原理 —— 从一个 Token，到一个 AI System》

从一个 Token 出发，逐个零件回答同一个问题：为什么一个 AI System 需要它。写给工程师的大模型系统原理书。

[![Build](https://github.com/yiyan-yixing/ai-system-book/actions/workflows/book-site.yml/badge.svg)](https://github.com/yiyan-yixing/ai-system-book/actions/workflows/book-site.yml)
[![在线阅读](https://img.shields.io/badge/在线阅读-yiyan--yixing.github.io-blue)](https://yiyan-yixing.github.io/ai-system-book/)
[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/license-CC%20BY--NC--SA%204.0-lightgrey.svg)](LICENSE)

> **在线阅读**
>
> [yiyan-yixing.github.io/ai-system-book](https://yiyan-yixing.github.io/ai-system-book/)
>
> 站点由 MkDocs Material 构建，支持全文搜索与深色模式。

## 这本书解决什么问题

市面上的书大多停在两头：要么停在 Transformer 的结构图，要么停在「怎么调接口」。这本走第三条路：每讲一个零件，都回答同一个问题——**为什么一个 AI System 需要它**。

读完你应当能回答三类问题。**是什么**：每个零件为什么必须存在，去掉它会怎样。**怎么决策**：模型放哪、上下文给多少、什么时候该加一层，依据是什么。**怎么算账**：显存、延迟、准确率、成本在模型内部到底怎么算出来。

它不从架构图讲起，而是从一次翻车讲起。作者用大模型做产品，先写出了「接个模型就完事」的幻觉，然后在接下来的两个月里被现实逼着补上一个又一个零件：小模型、模型池、路由、上下文、记忆、agent、harness、评估闸门。补完回头一看，这些零件今天都有了行业公认的名字。

写作原则只有一条：**每一节都挂真实的实验和真实的账本**。没有一手数据支撑的节，宁可等，不编。

全书 15 章 34 节，分上下两篇。上篇「零件」从 Token 与向量讲到预训练与对齐，把模型的内部机制拆到能画图、能算账；下篇「系统」从 Small Model 一路讲到 AI System，回答「一堆零件怎么拼成一个能自己运转的系统」。

## 适合谁读

- **用大模型做产品的工程师**：想知道「底下到底在发生什么」，而不只是会调接口
- **独立开发者 / 小团队技术负责人**：要自己决定模型放哪、上下文给多少、什么时候该加一层
- **技术决策者**：需要一张能跟团队讲清楚的原理地图

> 不解释「什么是 API」；但会从最底层的 Token 讲起，假定你没有手推过 attention。

## 不适合谁读

- **想找一本「照着调接口」的书**：本书不写 SDK 用法，也不给提示词模板
- **想速成的读者**：零件之间有依赖，按零件顺序写，跳读会断链
- **完全不想碰公式与数字的读者**：推导、显存账、跑分表都是具体数字，绕不开

## 内容目录

章节名可点，进入在线阅读站对应章节的导读页；每节的 Markdown 源文件在仓库 `manuscripts/` 目录下。

| 章 | 主题 |
|---|---|
| [序章](https://yiyan-yixing.github.io/ai-system-book/正文/00-序章.html) | 从一个模型，到一个 AI System |
| [第一章](https://yiyan-yixing.github.io/ai-system-book/正文/第01章-Token-与向量/index.html) | Token 与向量 |
| [第二章](https://yiyan-yixing.github.io/ai-system-book/正文/第02章-神经网络在学什么/index.html) | 神经网络在学什么 |
| [第三章](https://yiyan-yixing.github.io/ai-system-book/正文/第03章-Transformer/index.html) | Transformer：一个架构改变一切 |
| [第四章](https://yiyan-yixing.github.io/ai-system-book/正文/第04章-稀疏与高效/index.html) | 稀疏与高效：让大模型跑得动 |
| [第五章](https://yiyan-yixing.github.io/ai-system-book/正文/第05章-预训练/index.html) | 预训练：模型怎么学 |
| [第六章](https://yiyan-yixing.github.io/ai-system-book/正文/第06章-后训练与对齐/index.html) | 后训练与对齐 |
| [第七章](https://yiyan-yixing.github.io/ai-system-book/正文/第07章-本地训练/index.html) | 本地训练：亲手造一个 |
| [第八章](https://yiyan-yixing.github.io/ai-system-book/正文/第08章-Small-Model/index.html) | Small Model |
| [第九章](https://yiyan-yixing.github.io/ai-system-book/正文/第09章-Model-Pool-Router/index.html) | Model Pool / Router |
| [第十章](https://yiyan-yixing.github.io/ai-system-book/正文/第10章-Context/index.html) | Context |
| [第十一章](https://yiyan-yixing.github.io/ai-system-book/正文/第11章-Knowledge-Graph-Memory/index.html) | Knowledge / Graph · Memory |
| [第十二章](https://yiyan-yixing.github.io/ai-system-book/正文/第12章-Agent/index.html) | Agent |
| [第十三章](https://yiyan-yixing.github.io/ai-system-book/正文/第13章-Harness/index.html) | Harness |
| [第十四章](https://yiyan-yixing.github.io/ai-system-book/正文/第14章-Evaluation-与闭环/index.html) | Evaluation 与闭环 |
| [第十五章](https://yiyan-yixing.github.io/ai-system-book/正文/第15章-AI-System/index.html) | AI System |

## 当前进度

正文随写作进度分批发布：已开放的节可以直接读，其余节先占位。

| 部分 | 已发布 | 合计 |
|---|---:|---:|
| 序章 | 1 | 1 |
| 上篇 · 零件 | 1 | 22 |
| 下篇 · 系统 | 11 | 11 |
| **合计** | **13** | **34** |

其余 21 节为占位（只列节名与一句话导语）。正文分批同步，每发布一节更新一次。

## 在线阅读与下载

- **在线阅读（推荐）**：[yiyan-yixing.github.io/ai-system-book](https://yiyan-yixing.github.io/ai-system-book/)
- **仓库正文**：[`manuscripts/`](manuscripts/)，每节一个 Markdown 文件
- **同系列另一本**：《一人公司：把一个人的边界，扩成一家公司》，[在线阅读](https://yiyan-yixing.github.io/one-person-company-book/)
- **PDF**：排版定稿后发布，暂不提供

## 勘误与反馈

发现正文、图表或数据里的错误，请开一条 [勘误 Issue](https://github.com/yiyan-yixing/ai-system-book/issues/new?template=erratum.yml) 提交。

提交时请写清楚三件事：**位置**（章节号与小节）、**原文**（出问题的句子、公式或数字）、**问题与建议**（错在哪、建议怎么改；涉及数据请附来源、单位与计算过程）。

## 许可与署名

本书正文采用 [CC BY-NC-SA 4.0](LICENSE) 许可，署名「一言AI行」：

- 可以自由阅读、复制、转载、改编
- 转载与改编须保留署名「一言AI行」
- 不得用于商业目的
- 改编作品须以相同协议共享

协议全文见 [LICENSE](LICENSE)。

## 同步与红线

本站正文由主仓的同步脚本产出，推 `main` 后自动构建发布。同步前会跑一道红线闸。

**文本**：扫描所有将被提交的文件，命中内部仓库路径、凭据、金额、内部会议与白板引用等模式即**中止发布**。

**图片（已知盲区）**：图片的像素内容无法用文本 grep 检测。已实测发生过「正文文本干净、但配图 PNG 的像素里印着内部仓库路径」的情况。因此同步脚本会：

- 列出本批全部二进制文件并要求人工过目，未经确认不允许推送
- 用 OCR（`tesseract -l chi_sim+eng`）对图片自动扫描，命中内部路径模式即中止

OCR 有漏检可能（字体、小字号、艺术字、图形化排版都会降低识别率），**OCR 通过不等于图是干净的**——每张新图仍须人工过目一遍。

## 关于本站

静态站点由 MkDocs Material 构建，推 `main` 后自动发布到 GitHub Pages。本地预览：

```bash
pip install -r requirements.txt
mkdir -p .site-src/正文
cp -r manuscripts/. .site-src/正文/
cp archive/outlines/outline.md .site-src/目录大纲.md
cp index.md .site-src/index.md
cp -r assets .site-src/assets
mkdocs serve
```

正文按章分目录（`正文/第NN章-章名/`），章导语页是该目录下的 `index.md`；站点首页是封面页 `index.md`，由 `overrides/home.html` 渲染，数据来自 `mkdocs.yml` 的 `extra.*`。
