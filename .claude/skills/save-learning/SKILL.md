---
name: save-learning
description: 将当前项目根目录中最新导出的对话记录 .txt 保存为 learning-records 下的 Markdown 学习记录，并自动执行 git add、commit、push。触发词：归档学习记录、保存学习记录、保存本次学习记录、保存当前会话记录、导出学习记录、保存对话记录、归档对话记录、保存会话到 learning-records、save learning、archive learning record。
---

# save-learning

将当前会话的学习记录保存到 learning-records 目录，并 git push 到远程仓库。

## 依赖

- 对话记录已通过 `/export` 导出到当前项目根目录（`.txt` 文件）

## 操作步骤

1. 在项目根目录创建 `learning-records/` 文件夹（若不存在）
2. 将根目录下最新的 `.txt` 导出文件移动到 `learning-records/` 目录
3. 将文件后缀从 `.txt` 改为 `.md`
4. 执行 `git add` → `git commit` → `git push`
5. 删除源 `.txt` 文件
