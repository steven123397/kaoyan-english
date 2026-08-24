# Issue tracker: GitHub

本仓库的 specs 和 tickets 存放在 GitHub Issues 中，所有操作使用
`gh` CLI。

## Conventions

- 一个完整学习阶段或能力建设目标对应一份 spec。
- spec 拆分为若干可以独立完成、检查和关闭的 tickets。
- ticket 正文记录目标、练习材料、完成标准、依赖和反馈方式。
- 讨论和训练反馈追加到对应 Issue 的评论区。
- 完成标准满足后关闭 Issue；需要返工时重新打开。
- 使用标签记录 triage 状态。
- 不把 Pull Requests 作为任务入口。

## Operations

- 创建 Issue：`gh issue create --title "..." --body "..."`
- 读取 Issue：`gh issue view <number> --comments`
- 列出 Issue：`gh issue list --state open`
- 评论：`gh issue comment <number> --body "..."`
- 添加或移除标签：`gh issue edit <number> --add-label "..."` 或
  `gh issue edit <number> --remove-label "..."`
- 关闭：`gh issue close <number> --comment "..."`

仓库由当前目录的 Git remote 自动确定。

## Pull requests as a triage surface

**PRs as a request surface: no.**

## Skill operations

- 当技能要求“publish to the issue tracker”时，创建 GitHub Issue。
- 当技能要求“fetch the relevant ticket”时，运行
  `gh issue view <number> --comments`。

## Wayfinding operations

- Map 是一个带有 `wayfinder:map` 标签的 GitHub Issue。
- 决策 ticket 是 map 的子 Issue，并使用 `wayfinder:research`、
  `wayfinder:prototype`、`wayfinder:grilling` 或 `wayfinder:task` 标签。
- 优先使用 GitHub 原生 sub-issue 和 issue dependency；若仓库不支持，则在 map
  中使用任务列表，并在 ticket 正文写明 `Part of` 与 `Blocked by`。
- Claim ticket 时先把当前 GitHub 用户设为 assignee。
- Resolve ticket 时先把答案写入评论，再关闭 Issue，并在 map 的
  `Decisions so far` 中追加名称、链接和一句话结论。
- Frontier 是所有未关闭、未被阻塞且尚未分配负责人的子 Issue。
