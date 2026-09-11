---
name: github-cli
description: 使用 GitHub CLI（`gh`）搜索和管理 GitHub。用户要求操作 GitHub 账户、仓库、议题、拉取请求、发布或工作流时使用。
---

# GitHub CLI

直接使用 `gh` 完成用户请求；本地版本控制使用 `git`。不要在每次任务前重复检查版本或登录状态。

- 如果找不到 `gh`，按照[官方安装指南](https://github.com/cli/cli#installation)安装后继续。
- 如果命令返回未认证错误，运行 `gh auth login -h github.com -p https -w`，等待用户完成授权，然后重试原命令。不要让用户粘贴或输出访问令牌。
- 优先使用对应的 `gh` 子命令，必要时使用 `gh api`；目标仓库不明确时先确认。分析结果时优先请求结构化输出。

仓库搜索示例：

```powershell
gh search repos "关键词" --sort stars --order desc --limit 20
```

参考：[GitHub CLI 官方手册](https://cli.github.com/manual/)和[`gh search repos` 文档](https://cli.github.com/manual/gh_search_repos)。

删除、修改可见性、转移仓库、重写历史、强制推送等高风险操作必须获得用户对该操作的明确批准。
