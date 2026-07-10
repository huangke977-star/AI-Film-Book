# Phase One Volumes 01-05 Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Expand the first five volumes of `AI-Film-Book` from starter drafts into a coherent first-stage learning course for beginners who want to understand and reproduce the Codex + LibTV AI video workflow.

**Architecture:** Treat each volume as a self-contained learning module with shared examples, repeated terminology, and a consistent chapter structure. The Ross Douyin case acts as the running example, while templates and workflows serve as reusable practice assets.

**Tech Stack:** Markdown, Git, PowerShell verification commands, GitHub remote `origin/main`.

## Global Constraints

- Preserve the existing repository structure and Chinese-language Markdown style.
- First-stage scope is limited to `第01卷_AI视频基础.md`, `第02卷_环境搭建.md`, `第03卷_ChatGPT与Codex.md`, `第04卷_ContextEngineering.md`, `第05卷_LibTV完全教程.md`, `学习路线.md`, and closely related templates/checklists.
- Do not commit local media, screenshots, downloaded videos, credentials, cookies, tokens, or `.analysis/` files.
- OpenAI/Codex facts must be based on official OpenAI documentation or clearly framed as workflow advice.
- LibTV, Seedance, Kling, GPT, Banana, Midjourney, and similar tool details must be framed as time-sensitive when not verified in the current turn.
- Every volume must include learning goals, concepts, workflow, examples, templates, common mistakes, troubleshooting, summary, and practice.
- Avoid empty encouragement and avoid presenting AI as fully automatic production.
- Commit after each major deliverable and push after verified checkpoints.

---

## File Structure

- Modify: `第01卷_AI视频基础.md`  
  Responsibility: beginner foundation, terminology, AI video production map, first 15-second project mental model.

- Modify: `第02卷_环境搭建.md`  
  Responsibility: local project setup, Git, directory conventions, asset naming, security, Codex workspace habits.

- Modify: `第03卷_ChatGPT与Codex.md`  
  Responsibility: explain ChatGPT/Codex division of labor and practical Codex commands for AI video production.

- Modify: `第04卷_ContextEngineering.md`  
  Responsibility: transform prompt writing into reusable context engineering with file-based project memory.

- Modify: `第05卷_LibTV完全教程.md`  
  Responsibility: explain LibTV's role in the workflow, input/output patterns, generation loop, cost and failure tracking.

- Modify: `学习路线.md`  
  Responsibility: guide the user from no background to first workflow comprehension before hands-on production.

- Create: `14天入门训练营.md`  
  Responsibility: day-by-day path for after the first five volumes are ready; each day has reading, practice, and output.

- Modify: `Prompt库/Ross案例_端到端提示词模板.md`  
  Responsibility: align reusable prompts with the expanded first five volumes.

- Modify: `工作流/Codex_LibTV_端到端视频制作流程.md`  
  Responsibility: serve as the short operational SOP that readers use after completing the first five volumes.

- Modify: `更新日志.md`  
  Responsibility: record each expansion checkpoint.

---

### Task 1: Create First-Stage Learning Spine

**Files:**
- Modify: `学习路线.md`
- Create: `14天入门训练营.md`
- Modify: `更新日志.md`

**Interfaces:**
- Consumes: phase-one design from `docs/superpowers/specs/2026-07-10-ai-film-book-completion-design.md`
- Produces: a reader-facing order that all expanded volumes reference

- [ ] **Step 1: Replace `学习路线.md` with a first-stage-first reading path**

Write these sections in order:

```markdown
# 学习路线

## 先说结论

## 第一阶段：先学第 01-05 卷

## 你不需要先懂什么

## 第 1 周：建立基本认知

## 第 2 周：理解 Codex + LibTV 工作流

## 不建议一开始做的事

## 学完第一阶段后应该能做到什么

## 后续阶段如何继续
```

The copy must tell the beginner not to read all 18 volumes first. It must tell them to wait for the phase-one course if they want to learn after completion.

- [ ] **Step 2: Create `14天入门训练营.md`**

Use this exact daily structure for all 14 days:

```markdown
## Day 01：主题

阅读：

练习：

产出：

检查：
```

Day themes must be:

1. AI 视频全局地图
2. 从一句话到项目 brief
3. 认识脚本和分镜
4. 认识镜头语言
5. 搭建本地项目目录
6. 建立素材命名和版本管理
7. ChatGPT 与 Codex 分工
8. 让 Codex 读取项目文件
9. Prompt 到 Context 的升级
10. 建立风格手册和角色圣经
11. LibTV 工作流定位
12. 单镜头生成和失败记录
13. Ross 案例复盘
14. 完成第一个 15 秒试验片方案

- [ ] **Step 3: Update `更新日志.md`**

Add a top entry:

```markdown
## 2026-07-10

- 新增第一阶段扩写实施计划。
- 新增 `14天入门训练营.md`，用于第 01-05 卷完成后的学习路径。
```

- [ ] **Step 4: Verify task output**

Run:

```powershell
rg "第一阶段|14天|Day 01|Day 14|第 01-05 卷" 学习路线.md 14天入门训练营.md 更新日志.md
```

Expected: matches in all three files.

- [ ] **Step 5: Commit**

```powershell
git add 学习路线.md 14天入门训练营.md 更新日志.md
git commit -m "Add phase one learning spine"
```

---

### Task 2: Expand Volume 01 - AI Video Foundation

**Files:**
- Modify: `第01卷_AI视频基础.md`
- Modify: `工作流/Codex_LibTV_端到端视频制作流程.md`
- Modify: `更新日志.md`

**Interfaces:**
- Consumes: learning spine from Task 1
- Produces: shared vocabulary for later volumes: `创意层`, `叙事层`, `镜头层`, `生产层`, `最小闭环`, `失败样本`

- [ ] **Step 1: Replace `第01卷_AI视频基础.md` with a full beginner foundation**

Use this table of contents:

```markdown
# 第 01 卷：AI 视频基础

## 学习目标
## 本卷导读：先建立地图
## 1. AI 视频不是一个按钮
## 2. AI 视频制作的四层结构
## 3. AI 视频和传统视频制作的关系
## 4. 文生视频、图生视频、视频生视频、数字人和口播视频
## 5. 为什么很多 AI 视频没有电影感
## 6. 人物一致性、空间连续性和剪辑节奏
## 7. 从手搓提示词到项目化工作流
## 8. Ross 案例在本卷中的位置
## 9. 一个 15 秒试验片的最小闭环
## 10. 常见错误
## 11. 故障排查
## 12. 参数与概念速查
## 13. 本卷总结
## 14. 课后练习
## 15. 延伸阅读与核验记录
```

Content requirements:

- Explain every concept with beginner-friendly examples.
- Include at least one weak prompt and one improved prompt.
- Include a table comparing text-to-video, image-to-video, video-to-video, digital human, and talking-head video.
- Include a 15-second practice project that does not require the reader to generate video immediately.
- Mention that tool names and model capabilities change, but the workflow map remains useful.

- [ ] **Step 2: Update `工作流/Codex_LibTV_端到端视频制作流程.md`**

Add a short section near the top:

```markdown
## 与第 01 卷的关系

第 01 卷负责建立全局地图。本流程文档负责把地图压缩成可执行 SOP。读者如果看不懂这里的 brief、分镜、提示词、失败样本，应先回到第 01 卷。
```

- [ ] **Step 3: Update `更新日志.md`**

Add:

```markdown
- 扩写第 01 卷，建立 AI 视频制作全局地图和 15 秒试验片最小闭环。
```

- [ ] **Step 4: Verify task output**

Run:

```powershell
rg "四层结构|文生视频|图生视频|人物一致性|15 秒试验片|最小闭环" 第01卷_AI视频基础.md
```

Expected: each term appears.

Run:

```powershell
(Get-Content -LiteralPath '第01卷_AI视频基础.md' -Raw).Length
```

Expected: at least `12000` characters for the first expansion pass.

- [ ] **Step 5: Commit**

```powershell
git add 第01卷_AI视频基础.md 工作流/Codex_LibTV_端到端视频制作流程.md 更新日志.md
git commit -m "Expand volume 01 AI video foundation"
```

---

### Task 3: Expand Volume 02 - Environment Setup

**Files:**
- Modify: `第02卷_环境搭建.md`
- Modify: `素材管理/素材命名与归档规范.md`
- Modify: `API配置/LibTV_Codex配置说明.md`
- Modify: `更新日志.md`

**Interfaces:**
- Consumes: shared vocabulary from Task 2
- Produces: reusable project directory conventions for Tasks 4-6

- [ ] **Step 1: Replace `第02卷_环境搭建.md` with a practical setup guide**

Use this table of contents:

```markdown
# 第 02 卷：环境搭建

## 学习目标
## 本卷导读：先把创作放进文件夹
## 1. 为什么环境搭建是创作能力的一部分
## 2. 推荐电脑和软件准备
## 3. Git 的作用：记录创作而不是只上传代码
## 4. AI 视频项目目录结构
## 5. Brief、Script、Storyboard、Style Guide、Prompts、Outputs 的职责
## 6. 素材命名规范
## 7. `.env`、密钥和账号安全
## 8. Codex 工作区准备
## 9. LibTV 或同类平台准备
## 10. 剪辑软件和导出目录准备
## 11. Ross 案例项目目录示例
## 12. 常见错误
## 13. 故障排查
## 14. 环境检查清单
## 15. 本卷总结
## 16. 课后练习
```

Content requirements:

- Include a complete folder tree for one video project.
- Include a table explaining each folder.
- Include a table of safe and unsafe files to commit.
- Include beginner-safe Git commands and explain what each command does.
- State clearly that API keys, cookies, tokens, and downloaded media should not be committed.

- [ ] **Step 2: Update `素材管理/素材命名与归档规范.md`**

Add a section:

```markdown
## 与第 02 卷的关系

第 02 卷讲环境搭建，本文件是可复制的素材命名规范。实际项目中可以直接复制本文件作为团队规则。
```

- [ ] **Step 3: Update `API配置/LibTV_Codex配置说明.md`**

Add a section:

```markdown
## 与第 02 卷的关系

第 02 卷只讲安全原则和准备动作；本文件记录更具体的配置字段和连接方式。真实密钥只放本地 `.env`，不要写进 Markdown。
```

- [ ] **Step 4: Update `更新日志.md`**

Add:

```markdown
- 扩写第 02 卷，补齐项目目录、Git、素材管理、密钥安全和环境检查清单。
```

- [ ] **Step 5: Verify task output**

Run:

```powershell
rg "项目目录|Git|素材命名|\\.env|密钥|Ross 案例项目目录|环境检查清单" 第02卷_环境搭建.md
```

Expected: each term appears.

Run:

```powershell
(Get-Content -LiteralPath '第02卷_环境搭建.md' -Raw).Length
```

Expected: at least `10000` characters for the first expansion pass.

- [ ] **Step 6: Commit**

```powershell
git add 第02卷_环境搭建.md 素材管理/素材命名与归档规范.md API配置/LibTV_Codex配置说明.md 更新日志.md
git commit -m "Expand volume 02 environment setup"
```

---

### Task 4: Expand Volume 03 - ChatGPT and Codex

**Files:**
- Modify: `第03卷_ChatGPT与Codex.md`
- Modify: `Prompt库/Ross案例_端到端提示词模板.md`
- Modify: `更新日志.md`

**Interfaces:**
- Consumes: project directory conventions from Task 3
- Produces: Codex command patterns used in Task 5 and Task 6

- [ ] **Step 1: Replace `第03卷_ChatGPT与Codex.md` with an agent workflow guide**

Use this table of contents:

```markdown
# 第 03 卷：ChatGPT 与 Codex

## 学习目标
## 本卷导读：聊天助手和项目 Agent 的区别
## 1. ChatGPT 适合做什么
## 2. Codex 适合做什么
## 3. 为什么视频项目需要文件上下文
## 4. Codex 在 AI 视频制作中的 12 个典型任务
## 5. 给 Codex 下任务的基本格式
## 6. 让 Codex 先读文件再生成
## 7. 用 Codex 写 brief、脚本和分镜
## 8. 用 Codex 生成镜头提示词
## 9. 用 Codex 维护失败样本和迭代记录
## 10. 用 Codex 管理 Git 提交
## 11. 如何避免 Codex 编造工具能力
## 12. Ross 案例中的 Codex 角色
## 13. 常见错误
## 14. 故障排查
## 15. 本卷总结
## 16. 课后练习
```

Content requirements:

- Include a table comparing ChatGPT and Codex.
- Include 12 concrete Codex tasks for AI video.
- Include at least 8 copyable Codex prompts.
- State that Codex should not be asked to invent current prices, hidden platform abilities, or private account details.
- Include a beginner workflow for asking Codex to generate and then revise prompts.

- [ ] **Step 2: Update `Prompt库/Ross案例_端到端提示词模板.md`**

Add a section:

```markdown
## 与第 03 卷的关系

第 03 卷讲如何指挥 Codex；本模板是 Ross 案例的可复制指令库。读者可以先照抄，再逐步替换主题、风格和镜头。
```

- [ ] **Step 3: Update `更新日志.md`**

Add:

```markdown
- 扩写第 03 卷，补齐 ChatGPT/Codex 分工、12 个 Codex 视频任务和可复制指令。
```

- [ ] **Step 4: Verify task output**

Run:

```powershell
rg "12 个典型任务|先读文件|失败样本|Git 提交|避免 Codex 编造|Ross 案例" 第03卷_ChatGPT与Codex.md
```

Expected: each term appears.

Run:

```powershell
(Get-Content -LiteralPath '第03卷_ChatGPT与Codex.md' -Raw).Length
```

Expected: at least `12000` characters for the first expansion pass.

- [ ] **Step 5: Commit**

```powershell
git add 第03卷_ChatGPT与Codex.md Prompt库/Ross案例_端到端提示词模板.md 更新日志.md
git commit -m "Expand volume 03 ChatGPT and Codex"
```

---

### Task 5: Expand Volume 04 - Context Engineering

**Files:**
- Modify: `第04卷_ContextEngineering.md`
- Modify: `工作流/Codex_LibTV_端到端视频制作流程.md`
- Modify: `分镜模板/短视频分镜模板.md`
- Modify: `风格模板/电影感风格模板.md`
- Modify: `更新日志.md`

**Interfaces:**
- Consumes: Codex command patterns from Task 4
- Produces: context file schema used by Volume 05

- [ ] **Step 1: Replace `第04卷_ContextEngineering.md` with a context engineering guide**

Use this table of contents:

```markdown
# 第 04 卷：Context Engineering

## 学习目标
## 本卷导读：从手搓提示词到上下文工程
## 1. Prompt、Context、Workflow 的区别
## 2. 为什么单条提示词不够
## 3. AI 视频项目的上下文文件系统
## 4. Brief：项目的方向盘
## 5. Script：声音和信息节奏
## 6. Storyboard：镜头层的工程图
## 7. Style Guide：统一画面气质
## 8. Character Bible：人物一致性的最低保障
## 9. Iteration Log：失败样本如何变成资产
## 10. 上下文污染和上下文丢失
## 11. 多模型共享上下文
## 12. Ross 案例上下文结构复原
## 13. 可复制上下文模板
## 14. 常见错误
## 15. 故障排查
## 16. 本卷总结
## 17. 课后练习
```

Content requirements:

- Include one complete mini project context example.
- Include schemas for `brief.md`, `script.md`, `storyboard.md`, `style_guide.md`, `character_bible.md`, and `iteration_log.md`.
- Explain context pollution with concrete examples.
- Explain how to update only one file without changing the whole project.
- Include Ross case reconstruction as a table.

- [ ] **Step 2: Update `工作流/Codex_LibTV_端到端视频制作流程.md`**

Add a section:

```markdown
## 与第 04 卷的关系

第 04 卷负责解释每个上下文文件为什么存在。本 SOP 默认这些文件已经创建完成。
```

- [ ] **Step 3: Update `分镜模板/短视频分镜模板.md`**

Add fields `镜头目的`, `上下文依赖`, `失败风险`.

- [ ] **Step 4: Update `风格模板/电影感风格模板.md`**

Add fields `固定元素`, `可变化元素`, `禁止漂移项`.

- [ ] **Step 5: Update `更新日志.md`**

Add:

```markdown
- 扩写第 04 卷，建立 Brief、Script、Storyboard、Style Guide、Character Bible、Iteration Log 的上下文工程体系。
```

- [ ] **Step 6: Verify task output**

Run:

```powershell
rg "Prompt、Context、Workflow|Brief|Character Bible|Iteration Log|上下文污染|Ross 案例上下文结构" 第04卷_ContextEngineering.md
```

Expected: each term appears.

Run:

```powershell
(Get-Content -LiteralPath '第04卷_ContextEngineering.md' -Raw).Length
```

Expected: at least `12000` characters for the first expansion pass.

- [ ] **Step 7: Commit**

```powershell
git add 第04卷_ContextEngineering.md 工作流/Codex_LibTV_端到端视频制作流程.md 分镜模板/短视频分镜模板.md 风格模板/电影感风格模板.md 更新日志.md
git commit -m "Expand volume 04 context engineering"
```

---

### Task 6: Expand Volume 05 - LibTV Complete Tutorial

**Files:**
- Modify: `第05卷_LibTV完全教程.md`
- Modify: `API配置/LibTV_Codex配置说明.md`
- Modify: `故障排查/README.md`
- Modify: `参数速查/AI视频参数速查.md`
- Modify: `更新日志.md`

**Interfaces:**
- Consumes: context schemas from Task 5
- Produces: generation loop and failure-analysis workflow for first practical projects

- [ ] **Step 1: Replace `第05卷_LibTV完全教程.md` with a complete workflow tutorial**

Use this table of contents:

```markdown
# 第 05 卷：LibTV 完全教程

## 学习目标
## 本卷导读：LibTV 在工作流里的位置
## 1. LibTV 解决什么问题
## 2. LibTV 不解决什么问题
## 3. 手动复制、Skill/Agent、API/MCP 三种使用方式
## 4. 文生图、图生视频、文生视频和虚拟口播素材
## 5. 从 Codex 输出到 LibTV 任务
## 6. 单镜头生成流程
## 7. 多版本筛选
## 8. 失败样本记录
## 9. 成本记录
## 10. 人物一致性处理
## 11. 背景切换和风格统一
## 12. Ross 案例复刻流程
## 13. 常见错误
## 14. 故障排查
## 15. 参数速查
## 16. 本卷总结
## 17. 课后练习
```

Content requirements:

- State clearly that platform UI, prices, model names, and permissions are time-sensitive.
- Explain manual-copy workflow first because it is safest for beginners.
- Explain Skill/Agent and API/MCP as advanced workflow options.
- Include a single-shot generation checklist.
- Include a multi-version review table.
- Include a cost log template.
- Include a Ross-style virtual talking-head reproduction plan without claiming exact hidden tool settings.

- [ ] **Step 2: Update `API配置/LibTV_Codex配置说明.md`**

Add a `第 05 卷实践配置` section with fields:

```markdown
LIBTV_API_KEY=
LIBTV_OUTPUT_DIR=outputs/raw
DEFAULT_VIDEO_RATIO=9:16
DEFAULT_VIDEO_DURATION=5
DEFAULT_GENERATION_MODE=manual
```

Explain that these are example names and should be adapted to the actual platform.

- [ ] **Step 3: Update `故障排查/README.md`**

Add a `LibTV 生成循环问题` section covering:

- prompt too broad
- model mismatch
- character drift
- background drift
- unreadable text
- cost overrun

- [ ] **Step 4: Update `参数速查/AI视频参数速查.md`**

Add a `LibTV 或同类工具生成前检查` section with ratio, duration, input type, reference image, negative prompt, output folder, and cost note.

- [ ] **Step 5: Update `更新日志.md`**

Add:

```markdown
- 扩写第 05 卷，补齐 LibTV 在 Codex 工作流中的定位、单镜头生成、多版本筛选、失败记录和 Ross 案例复刻流程。
```

- [ ] **Step 6: Verify task output**

Run:

```powershell
rg "手动复制|Skill/Agent|API/MCP|单镜头生成|多版本筛选|成本记录|Ross 案例复刻" 第05卷_LibTV完全教程.md
```

Expected: each term appears.

Run:

```powershell
(Get-Content -LiteralPath '第05卷_LibTV完全教程.md' -Raw).Length
```

Expected: at least `15000` characters for the first expansion pass.

- [ ] **Step 7: Commit**

```powershell
git add 第05卷_LibTV完全教程.md API配置/LibTV_Codex配置说明.md 故障排查/README.md 参数速查/AI视频参数速查.md 更新日志.md
git commit -m "Expand volume 05 LibTV tutorial"
```

---

### Task 7: Phase-One Consistency Pass

**Files:**
- Modify: `README.md`
- Modify: `学习路线.md`
- Modify: `14天入门训练营.md`
- Modify: `资料来源与核验记录.md`
- Modify: `更新日志.md`

**Interfaces:**
- Consumes: completed Tasks 1-6
- Produces: synchronized public entrypoint for the first-stage course

- [ ] **Step 1: Update `README.md`**

Add a section:

```markdown
## 当前推荐学习入口

第一阶段请先学第 01-05 卷，再进入 14 天训练营。不要从第 06-18 卷开始，因为这些卷仍属于后续阶段。
```

- [ ] **Step 2: Update `学习路线.md`**

Ensure it points to:

```text
第01卷 -> 第02卷 -> 第03卷 -> 第04卷 -> 第05卷 -> 14天入门训练营 -> Ross 案例复盘
```

- [ ] **Step 3: Update `资料来源与核验记录.md`**

Add a `第一阶段核验说明` section listing:

- Ross Douyin page is verified on 2026-07-10.
- OpenAI/Codex facts require official-source checks when expanded.
- LibTV platform facts require current-page or user-provided evidence when exact UI/price details are added.

- [ ] **Step 4: Run global content checks**

Run:

```powershell
rg "临时文本|尚未补完|后续补充" 第01卷_AI视频基础.md 第02卷_环境搭建.md 第03卷_ChatGPT与Codex.md 第04卷_ContextEngineering.md 第05卷_LibTV完全教程.md 学习路线.md 14天入门训练营.md
```

Expected: no output.

Run:

```powershell
$targets = @('第01卷_AI视频基础.md','第02卷_环境搭建.md','第03卷_ChatGPT与Codex.md','第04卷_ContextEngineering.md','第05卷_LibTV完全教程.md')
foreach ($path in $targets) { $text = Get-Content -LiteralPath $path -Raw; "$path`t$($text.Length)" }
```

Expected: each file meets its first-pass target from Tasks 2-6.

- [ ] **Step 5: Commit**

```powershell
git add README.md 学习路线.md 14天入门训练营.md 资料来源与核验记录.md 更新日志.md
git commit -m "Polish phase one learning entrypoints"
```

---

### Task 8: Push and Final Verification

**Files:**
- No content changes unless verification finds a concrete issue.

**Interfaces:**
- Consumes: committed outputs from Tasks 1-7
- Produces: synchronized GitHub repository and a concise status report

- [ ] **Step 1: Inspect Git history**

Run:

```powershell
git log --oneline -8
```

Expected: commits for Tasks 1-7 are visible.

- [ ] **Step 2: Confirm no local media is tracked**

Run:

```powershell
git ls-files .analysis
```

Expected: no output.

- [ ] **Step 3: Confirm working tree is clean**

Run:

```powershell
git status --short --branch
```

Expected: `## main...origin/main` before push, or clean branch state after push.

- [ ] **Step 4: Push**

Run:

```powershell
git push
```

Expected: remote `main` updates successfully.

- [ ] **Step 5: Verify remote commit**

Run:

```powershell
git ls-remote origin refs/heads/main
```

Expected: remote hash matches local `git rev-parse HEAD`.

- [ ] **Step 6: Report**

Report:

- files expanded
- approximate current character count
- latest commit hash
- remaining scope for volumes 06-18
