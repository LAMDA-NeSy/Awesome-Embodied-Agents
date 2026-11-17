# Contributing · 贡献指南

欢迎补充论文、数据集、评测基准、仿真器和阅读笔记，也欢迎修复现有条目。

## 收录范围

围绕在真实或模拟空间中进行感知、决策和行动的具身智能体，优先收录具有明确技术贡献、公开论文和可核验来源的工作。相关的机器人学习基础方法也可以收录。具体分类见 [TAXONOMY.md](docs/TAXONOMY.md)。

## 添加论文

1. 在 [README.md](README.md) 中搜索标题或 arXiv 编号，确认尚未收录。
2. 根据主要技术贡献选择一个分类，在该分类表格中插入一行。
3. 按首次公开日期倒序排列；同一天的条目可按标题字母排序。
4. 使用完整论文标题；方法简称可追加在标题末尾。链接优先采用 arXiv 摘要页、会议论文页或 DOI。
5. 核验日期、会议或期刊、代码和项目页。条目信息以作者项目页、官方代码库和论文出版页为准。

复制下面的表格行，并替换字段：

```markdown
| [**Full Paper Title**](PAPER_URL) | VENUE | YYYY-MM-DD | [Code](CODE_URL) | [Project](PROJECT_URL) |
```

没有记录的代码或项目页统一写 `—`，不要保留占位链接：

```markdown
| [**Full Paper Title**](PAPER_URL) | arXiv | YYYY-MM-DD | — | — |
```

## 字段约定

| 字段 | 约定 |
| :--- | :--- |
| Title | 完整标题；保留原文，简称可放在括号中 |
| Venue | 已核验的会议或期刊及年份，例如 `ICML 2025`；尚未记录其他出版信息时填 `arXiv` |
| Date | 首次公开日期，格式为 `YYYY-MM-DD`；arXiv 论文使用 v1 日期 |
| Code | 官方实现；第三方实现需明确标注 `[Unofficial]` |
| Project | 作者项目页，可包含视频、Demo 或模型下载入口 |

会议年份和首次公开年份不同是正常情况。后续修订、补开源或录用时更新相应字段，保留首次公开日期。

同一篇论文在主页只出现于一个主要分类；数据集或评测论文可以同时出现在对应资源索引中。跨主题联系可写在阅读笔记中。

## 添加资源

将资源加入 `Awesome Datasets`、`Awesome Benchmarks` 或 `Awesome Simulators` 的相应表格。说明主要用途，并链接官方仓库或项目页。

```markdown
| **Resource Name** | Short description of its focus | [Repository](OFFICIAL_URL) |
```

## 添加阅读笔记

1. 复制 [notes/TEMPLATE.md](notes/TEMPLATE.md)，命名为 `YYYY-short-name.md`。
2. 用自己的语言填写问题、方法、智能体闭环、实验和局限；可使用中文或英文。
3. 在 [notes/README.md](notes/README.md) 中添加索引行。
4. 区分论文结论、自己的理解和待核实问题。

## 提交前检查

- 标题、日期和链接已核验；正式出版信息有来源支持。
- 主分类正确，论文表格按首次公开日期倒序排列。
- Markdown 表格列数一致，GitHub 预览中的目录和链接可用。
- 新增笔记已加入笔记索引。

提交标题可用 `Add: Paper Name`、`Fix: Resource Link` 或 `Notes: Paper Name`。重大分类调整可先通过 issue 说明理由。
