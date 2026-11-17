# 日常维护指南

## 日常添加一篇文章

1. 打开 [README.md](../README.md)，选择对应主题。
2. 按 [贡献指南](../CONTRIBUTING.md) 复制表格行，填写论文、会议、首次公开日期、代码和项目页。
3. 在分类内按日期从新到旧插入。
4. 如果做了精读，复制 [笔记模板](../notes/TEMPLATE.md)，并更新 [笔记索引](../notes/README.md)。

`README.md` 是论文索引的唯一维护入口，不需要运行构建工具或同步其他数据文件。`Updates` 用于记录重要新增和结构调整，可在每次集中整理后更新一条。

## 直接在 GitHub 编辑

进入自己的仓库，打开 `README.md`，点击编辑按钮，修改后使用 Preview 查看表格，再提交修改。精读笔记可以通过 Add file 创建。

其他人可以使用 **Issues → New issue → Add a paper** 推荐论文，也可以提交 PR；仓库已配好论文推荐、链接纠错和 PR 模板。

## 本地编辑

在仓库目录中编辑 Markdown 文件，然后提交和推送：

```bash
git add README.md notes/
git commit -m "Add: Paper Name"
git push
```

若修改了其他文件，将相应路径一起加入 `git add`。

## 首次发布到 GitHub

建议仓库名：`Awesome-Embodied-Agents`。

建议描述：

```text
A curated collection of papers, datasets, benchmarks, and simulators for embodied agents.
```

如果尚未登录 GitHub CLI，先在终端完成登录：

```bash
gh auth login
```

确认本地已有初始提交后，在当前仓库目录执行以下命令创建公开仓库并推送。若需要私有仓库，将 `--public` 改为 `--private`：

```bash
gh repo create Awesome-Embodied-Agents --public --source=. --remote=origin --push --description "A curated collection of papers, datasets, benchmarks, and simulators for embodied agents."
```

如果已在 GitHub 创建了空仓库，则使用该仓库实际的 Git 地址：

```bash
git remote add origin YOUR_GITHUB_REPOSITORY_GIT_URL
git push -u origin main
```

建议 topics：`awesome`、`awesome-list`、`embodied-ai`、`embodied-agents`、`robotics`、`vision-language-action`、`large-language-models`。

## 后续扩展

- 论文数量增加后，可按年份或更细主题拆分目录，并保留主页入口。
- 如需增加星标徽章、issue 快捷链接或项目主页，使用实际 GitHub 仓库地址。
- 初始收录用于搭建阅读框架；后续可以围绕自己的综述问题逐步补充新论文与详细笔记。
