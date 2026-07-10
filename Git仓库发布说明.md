# Git 仓库发布说明

这个目录已经按 Git 仓库的形态准备。你创建远程仓库后，把仓库地址发给我，我可以继续帮你推送。

## 远程仓库创建建议

仓库名可以使用：

- `AI-Film-Book`
- `ai-video-production-guide`
- `2026-ai-video-guide`

仓库描述可以写：

```text
2026 AI 视频制作百科：Codex、LibTV、AI 视频工作流、Prompt 库、分镜模板与商业交付指南。
```

## 本地推送命令

如果远程仓库是空仓库，可以在本目录执行：

```bash
git remote add origin <你的远程仓库地址>
git branch -M main
git push -u origin main
```

如果远程仓库已经有 README 或其他提交，需要先拉取并处理合并：

```bash
git remote add origin <你的远程仓库地址>
git pull origin main --allow-unrelated-histories
git push -u origin main
```

## 后续维护分支建议

- `main`：稳定可发布版本。
- `draft/volume-xx`：某一卷正在扩写时使用。
- `case/ross-codex-libtv`：案例复刻和素材补充。

