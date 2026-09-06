# Git 单文件练习

只操作这一个文件。每次只填写当前阶段的空白，然后提交；这样 `git diff` 显示的就是本次学习新增的内容。

## 0. 第一次提交

我的 Git 用户名：LuoCaiNeng

我学习 Git 的目标：通过单文件的提交历史，理解暂存、分支、合并与 worktree 的差异。

执行：`git add git-learning.md`，然后执行 `git commit -m "chore: 开始 Git 单文件练习"`。

## 1. 工作区、暂存区、提交

填写：我理解 `git add` 的作用是：____________________________

依次执行：`git diff` → `git add git-learning.md` → `git diff --staged` → `git commit -m "docs: 记录暂存区理解"`。

## 2. 分支

先执行：`git switch -c feature/greeting`。

在功能分支填写：发布标题：欢迎页：____________________________

填写后执行：`git add git-learning.md`，再执行 `git commit -m "feat: 添加欢迎语方案"`。

接着执行：`git switch main`。

在主线把同一行“发布标题”改为：发布标题：稳定版：____________________________

填写后执行：`git add git-learning.md`，再执行 `git commit -m "docs: 更新主线发布计划"`。

## 3. 合并冲突

执行：`git merge feature/greeting`。Git 会因为两条分支修改了同一行“发布标题”而提示冲突。

手动删除冲突标记，并写下最终版本：发布标题：____________________________

填写：我选择这个版本的理由：____________________________

然后执行：`git add git-learning.md`，再执行 `git commit -m "merge: 整合欢迎语方案"`。

## 4. 查看历史

执行：`git log --oneline --graph --decorate --all`。

填写：我观察到功能分支和主线如何汇合：____________________________

执行：`git add git-learning.md`，然后执行 `git commit -m "docs: 复盘 Git 分支练习"`。

## 5. 可选：worktree

在仓库根目录执行：`git worktree add ..\git-learning-hotfix -b hotfix/quick-copy`。

进入新目录后，在本文件填写：这个 worktree 的作用：____________________________

执行：`git add git-learning.md`，然后执行 `git commit -m "docs: 记录 worktree 练习"`。

完成后，在任一工作目录执行：`git worktree list`。
