# Domain Docs

本仓库采用 single-context 布局。

## Before working

开始规划或执行任务前，读取：

- 根目录的 `CONTEXT.md`（如果存在）；
- `docs/adr/` 中与当前任务有关的决策记录（如果存在）。

不存在时直接继续，不要求预先创建。

## Vocabulary

写 spec、ticket、反馈和复盘时，应使用 `CONTEXT.md` 中已经确定的学习术语，
避免同一能力使用多个名称。如果所需概念尚未定义，应先判断它是真正的概念
缺口，还是不必要的新说法。

## ADR conflicts

如果工作方案与已有 ADR 冲突，应明确指出冲突，而不是静默覆盖已有决定。
