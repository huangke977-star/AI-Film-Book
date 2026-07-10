# Phase Two Volumes 06-10 Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Expand volumes 06-10 into the second learning stage of `AI-Film-Book`, moving readers from workflow awareness into video generation, cinematic judgment, directing, character consistency, and AI image preparation.

**Architecture:** Each volume is a self-contained Markdown learning module, but the five modules share terminology from volumes 01-05. Tool-specific claims are separated from workflow advice, and source-sensitive facts are recorded in `资料来源与核验记录.md`.

**Tech Stack:** Markdown, Git, PowerShell verification commands, GitHub remote `origin/main`, official-source web verification for current tool facts.

## Global Constraints

- Preserve the existing repository structure and Chinese-language Markdown style.
- Work in branch `phase-two-volumes-06-10` under `.worktrees/phase-two-volumes-06-10`.
- Do not commit local media, screenshots, downloaded videos, credentials, cookies, tokens, or `.analysis/` files.
- Seedance facts must be based on official ByteDance Seed sources when written as current facts.
- OpenAI image-generation facts must be based on official OpenAI documentation when written as current facts.
- Platform UI, prices, model availability, account permissions, and region availability must be described as time-sensitive unless verified in the same task.
- Every expanded volume must include learning goals,导读, concepts, workflow, examples, templates, common mistakes, troubleshooting, summary, practice, and source notes.
- Do not retain old placeholder chapter markers in volumes 06-10.
- Commit after each major deliverable and push only after final verification.

---

## File Structure

- Modify: `第06卷_Seedance完全教程.md`  
  Responsibility: Seedance or similar video model workflow, text-to-video, image-to-video, shot control, generation review.

- Modify: `第07卷_电影镜头语言.md`  
  Responsibility: cinematic vocabulary for AI prompts and storyboard judgment.

- Modify: `第08卷_导演思维.md`  
  Responsibility: human creative judgment, directing intent, material selection, Codex as creative assistant.

- Modify: `第09卷_人物一致性.md`  
  Responsibility: character bible, reference image strategy, multi-shot continuity, risk handling.

- Modify: `第10卷_AI绘图.md`  
  Responsibility: concept images, character references, scene references, covers, and image-to-video preparation.

- Modify: `README.md`  
  Responsibility: public entrypoint now reflecting phase two availability.

- Modify: `学习路线.md`  
  Responsibility: learning sequence for phase two after phase one.

- Modify: `资料来源与核验记录.md`  
  Responsibility: record source-sensitive facts used in phase two.

- Modify: `更新日志.md`  
  Responsibility: record each phase two expansion checkpoint.

- Modify: `工具排行榜/2026_AI视频工具清单.md`  
  Responsibility: align tool list with Seedance and AI image workflow language.

- Modify: `运镜模板/AI视频运镜模板.md`  
  Responsibility: add cinematic movement vocabulary used by volume 07.

- Modify: `分镜模板/短视频分镜模板.md`  
  Responsibility: ensure storyboard fields support camera language, directing intent, continuity, and reference images.

- Modify: `风格模板/电影感风格模板.md`  
  Responsibility: connect cinematic style to director intent and character consistency.

- Modify: `参数速查/AI视频参数速查.md`  
  Responsibility: add generation and image-reference checks used by volumes 06 and 10.

- Modify: `Prompt库/README.md`  
  Responsibility: list phase two prompt categories and how to use them.

---

### Task 1: Verify Sources and Add Plan

**Files:**
- Create: `docs/superpowers/plans/2026-07-10-phase-two-volumes-06-10-plan.md`
- Modify: `资料来源与核验记录.md`
- Modify: `更新日志.md`

**Interfaces:**
- Consumes: `docs/superpowers/specs/2026-07-10-phase-two-volumes-06-10-design.md`
- Produces: source rules and implementation sequence used by Tasks 2-8

- [ ] **Step 1: Verify official source links**

Open these sources and confirm they resolve before writing tool facts:

```text
https://seed.bytedance.com/seedance
https://seed.bytedance.com/en/models
https://seed.bytedance.com/en/public_papers/seedance-1-0-exploring-the-boundaries-of-video-generation-models
https://developers.openai.com/api/docs/guides/image-generation
https://developers.openai.com/api/docs/models/gpt-image-2
```

Expected: each page opens or search results identify the official replacement page. If a page fails, do not write exact claims from it.

- [ ] **Step 2: Update `资料来源与核验记录.md`**

Add:

```markdown
### 第二阶段工具资料核验

- Seedance 相关事实优先记录 ByteDance Seed 官方页面、模型页面和技术报告页面；如果页面不可访问，只保留工作流级建议。
- AI 图像生成相关 OpenAI 事实优先记录 OpenAI 官方 image generation guide 和 GPT Image 模型页。
- 第二阶段不写死平台价格、套餐权限、按钮路径、可用地区或隐藏参数。
```

- [ ] **Step 3: Update `更新日志.md`**

Add:

```markdown
- 新增第二阶段第 06-10 卷扩写设计与实施计划。
```

- [ ] **Step 4: Verify task output**

Run:

```powershell
rg "第二阶段工具资料核验|Seedance|GPT Image|第 06-10 卷" 资料来源与核验记录.md 更新日志.md docs/superpowers/plans/2026-07-10-phase-two-volumes-06-10-plan.md
```

Expected: matches in all three files.

- [ ] **Step 5: Commit**

```powershell
git add docs/superpowers/plans/2026-07-10-phase-two-volumes-06-10-plan.md 资料来源与核验记录.md 更新日志.md
git commit -m "Add phase two implementation plan"
```

---

### Task 2: Expand Volume 06 - Seedance Complete Tutorial

**Files:**
- Modify: `第06卷_Seedance完全教程.md`
- Modify: `工具排行榜/2026_AI视频工具清单.md`
- Modify: `参数速查/AI视频参数速查.md`
- Modify: `更新日志.md`

**Interfaces:**
- Consumes: source rules from Task 1 and generation-loop vocabulary from volume 05
- Produces: shared terms for later volumes: `视频生成模型`, `文生视频`, `图生视频`, `多镜头生成`, `运动幅度`, `生成复盘`

- [ ] **Step 1: Replace `第06卷_Seedance完全教程.md` with a full beginner-to-intermediate guide**

Use this table of contents:

```markdown
# 第 06 卷：Seedance 完全教程

## 学习目标
## 本卷导读：从 LibTV 工作流走向视频模型判断
## 1. Seedance 在 AI 视频工作流中的位置
## 2. 视频生成模型解决什么问题
## 3. 视频生成模型不解决什么问题
## 4. 文生视频工作流
## 5. 图生视频工作流
## 6. 单镜头生成任务卡
## 7. 多镜头生成和连续性
## 8. 运镜控制
## 9. 动作幅度和失败风险
## 10. 人物一致性初步
## 11. 与 LibTV、Veo、Kling 等工具的关系
## 12. Ross 风格短视频中的生成策略
## 13. 生成复盘表
## 14. 常见错误
## 15. 故障排查
## 16. 参数速查
## 17. 本卷总结
## 18. 课后练习
## 19. 延伸阅读与核验记录
```

Content requirements:

- Explain Seedance as a video-generation model family or model capability only when official sources support the wording.
- Explain that exact UI, price, model version, region availability, and account permission depend on the current platform.
- Include one weak video prompt and one improved video task card.
- Include a text-to-video workflow and an image-to-video workflow.
- Include a table for single-shot generation review.
- Include a section explaining how volume 06 connects to volumes 05, 07, and 09.

- [ ] **Step 2: Update `工具排行榜/2026_AI视频工具清单.md`**

Add a section:

```markdown
## 与第 06 卷的关系

第 06 卷把 Seedance 或同类视频模型放进生成工作流中理解。本清单只做工具定位，不替代当前官方页面、实际账号权限和平台价格核验。
```

- [ ] **Step 3: Update `参数速查/AI视频参数速查.md`**

Add a section:

```markdown
## 视频生成模型任务前检查

| 项目 | 检查问题 |
| --- | --- |
| 输入类型 | 文生视频、图生视频还是视频生视频 |
| 镜头目的 | 这个镜头服务哪一句信息 |
| 主体 | 谁或什么是画面中心 |
| 动作幅度 | 动作是否过于复杂 |
| 运镜 | 是否只使用一种主要运镜 |
| 时长 | 是否先控制在 3 到 5 秒 |
| 画幅 | 是否匹配发布平台 |
| 参考图 | 是否需要固定人物或场景 |
| 负面约束 | 是否排除乱码、变形、多余主体 |
```

- [ ] **Step 4: Update `更新日志.md`**

Add:

```markdown
- 扩写第 06 卷，补齐 Seedance 或同类视频模型在文生视频、图生视频、单镜头生成和复盘中的工作流。
```

- [ ] **Step 5: Verify task output**

Run:

```powershell
rg "Seedance|文生视频|图生视频|单镜头生成任务卡|多镜头生成|运镜控制|生成复盘" 第06卷_Seedance完全教程.md
```

Expected: each term appears.

Run:

```powershell
(Get-Content -LiteralPath '第06卷_Seedance完全教程.md' -Raw).Length
```

Expected: at least `12000`.

- [ ] **Step 6: Commit**

```powershell
git add 第06卷_Seedance完全教程.md 工具排行榜/2026_AI视频工具清单.md 参数速查/AI视频参数速查.md 更新日志.md
git commit -m "Expand volume 06 Seedance tutorial"
```

---

### Task 3: Expand Volume 07 - Cinematic Shot Language

**Files:**
- Modify: `第07卷_电影镜头语言.md`
- Modify: `运镜模板/AI视频运镜模板.md`
- Modify: `分镜模板/短视频分镜模板.md`
- Modify: `更新日志.md`

**Interfaces:**
- Consumes: generation-control terms from Task 2
- Produces: cinematic vocabulary used by volumes 08 and 09

- [ ] **Step 1: Replace `第07卷_电影镜头语言.md` with a practical cinematic language guide**

Use this table of contents:

```markdown
# 第 07 卷：电影镜头语言

## 学习目标
## 本卷导读：不是背术语，而是控制观众注意力
## 1. 镜头语言为什么重要
## 2. 景别
## 3. 机位
## 4. 焦段
## 5. 运镜
## 6. 光线
## 7. 构图
## 8. 剪辑匹配
## 9. 镜头语言如何写进 AI 提示词
## 10. 从普通提示词到电影化提示词
## 11. 15 秒试验片镜头设计
## 12. Ross 案例中的镜头语言观察
## 13. 常见错误
## 14. 故障排查
## 15. 镜头语言速查
## 16. 本卷总结
## 17. 课后练习
```

Content requirements:

- Explain each cinematic concept through beginner examples.
- Include tables for shot size, camera angle, lens feeling, camera movement, lighting, and composition.
- Include weak prompt and improved prompt examples.
- Include a five-shot 15-second practice sequence.
- Emphasize that AI prompts should not stack too many camera moves in one shot.

- [ ] **Step 2: Update `运镜模板/AI视频运镜模板.md`**

Add columns or examples for:

```text
镜头目的
运动幅度
适用场景
AI 失败风险
```

- [ ] **Step 3: Update `分镜模板/短视频分镜模板.md`**

Ensure the template contains these fields:

```text
景别
机位
焦段感
主要运镜
镜头目的
失败风险
```

- [ ] **Step 4: Update `更新日志.md`**

Add:

```markdown
- 扩写第 07 卷，补齐景别、机位、焦段、运镜、光线、构图和 AI 提示词写法。
```

- [ ] **Step 5: Verify task output**

Run:

```powershell
rg "景别|机位|焦段|运镜|光线|构图|剪辑匹配|电影化提示词" 第07卷_电影镜头语言.md
```

Expected: each term appears.

Run:

```powershell
(Get-Content -LiteralPath '第07卷_电影镜头语言.md' -Raw).Length
```

Expected: at least `14000`.

- [ ] **Step 6: Commit**

```powershell
git add 第07卷_电影镜头语言.md 运镜模板/AI视频运镜模板.md 分镜模板/短视频分镜模板.md 更新日志.md
git commit -m "Expand volume 07 cinematic language"
```

---

### Task 4: Expand Volume 08 - Director Thinking

**Files:**
- Modify: `第08卷_导演思维.md`
- Modify: `风格模板/电影感风格模板.md`
- Modify: `Prompt库/README.md`
- Modify: `更新日志.md`

**Interfaces:**
- Consumes: cinematic vocabulary from Task 3
- Produces: director-intent language used by volumes 09-10 and later case volumes

- [ ] **Step 1: Replace `第08卷_导演思维.md` with a practical directing guide**

Use this table of contents:

```markdown
# 第 08 卷：导演思维

## 学习目标
## 本卷导读：AI 时代导演仍然重要
## 1. 导演到底决定什么
## 2. 意图优先原则
## 3. 导演阐述怎么写
## 4. 镜头为什么要有目的
## 5. 节奏和信息控制
## 6. 如何判断素材是否服务叙事
## 7. 如何指导 Codex 做创意助理
## 8. 从普通画面到导演化画面
## 9. Ross 案例中的导演判断
## 10. 导演检查清单
## 11. 常见错误
## 12. 故障排查
## 13. 本卷总结
## 14. 课后练习
```

Content requirements:

- Include a director statement template.
- Include a material-selection table.
- Include at least 6 copyable Codex prompts for director review.
- Include before/after examples transforming ordinary visual descriptions into directed visual choices.
- Emphasize that AI can generate options but humans still decide intention, rhythm, and final selection.

- [ ] **Step 2: Update `风格模板/电影感风格模板.md`**

Add a section:

```markdown
## 导演阐述字段

- 核心意图：
- 观众情绪：
- 节奏：
- 镜头选择理由：
- 禁止偏离项：
```

- [ ] **Step 3: Update `Prompt库/README.md`**

Add prompt categories:

```markdown
## 第二阶段 Prompt 分类

- 镜头语言改写。
- 导演阐述生成。
- 素材选择复盘。
- 人物一致性检查。
- 参考图生成。
```

- [ ] **Step 4: Update `更新日志.md`**

Add:

```markdown
- 扩写第 08 卷，补齐导演阐述、意图优先、素材选择和 Codex 创意助理指令。
```

- [ ] **Step 5: Verify task output**

Run:

```powershell
rg "导演阐述|意图优先|素材是否服务叙事|Codex 做创意助理|导演检查清单" 第08卷_导演思维.md
```

Expected: each term appears.

Run:

```powershell
(Get-Content -LiteralPath '第08卷_导演思维.md' -Raw).Length
```

Expected: at least `12000`.

- [ ] **Step 6: Commit**

```powershell
git add 第08卷_导演思维.md 风格模板/电影感风格模板.md Prompt库/README.md 更新日志.md
git commit -m "Expand volume 08 director thinking"
```

---

### Task 5: Expand Volume 09 - Character Consistency

**Files:**
- Modify: `第09卷_人物一致性.md`
- Modify: `分镜模板/短视频分镜模板.md`
- Modify: `风格模板/电影感风格模板.md`
- Modify: `参数速查/AI视频参数速查.md`
- Modify: `更新日志.md`

**Interfaces:**
- Consumes: director intent from Task 4 and context-engineering schema from volume 04
- Produces: character-consistency rules used by volume 10 and later short-drama/commercial case volumes

- [ ] **Step 1: Replace `第09卷_人物一致性.md` with a consistency-control guide**

Use this table of contents:

```markdown
# 第 09 卷：人物一致性

## 学习目标
## 本卷导读：不要把 same character 当魔法
## 1. 人物一致性的本质
## 2. 为什么 AI 视频容易变脸
## 3. Character Bible 写法
## 4. 参考图策略
## 5. 服装、发型、道具约束
## 6. 表情、动作和年龄漂移
## 7. 多镜头人物连续性
## 8. 口播人物和剧情人物的不同控制方法
## 9. 失败样本复盘
## 10. 商业项目中的授权和风险
## 11. Ross 风格虚拟口播人物复盘
## 12. 常见错误
## 13. 故障排查
## 14. 人物一致性检查清单
## 15. 本卷总结
## 16. 课后练习
```

Content requirements:

- Include a complete Character Bible template.
- Include a reference-image naming pattern.
- Include a before/after character prompt.
- Include a multi-shot continuity table.
- Include a failure-analysis table.
- Explain that legal authorization and likeness rights matter in commercial projects.

- [ ] **Step 2: Update `分镜模板/短视频分镜模板.md`**

Add or confirm fields:

```text
角色状态
服装/发型
连续性备注
参考图路径
```

- [ ] **Step 3: Update `风格模板/电影感风格模板.md`**

Add a section:

```markdown
## 人物一致性约束

- 固定人物特征：
- 固定服装：
- 固定发型：
- 可变化表情：
- 禁止漂移项：
```

- [ ] **Step 4: Update `参数速查/AI视频参数速查.md`**

Add a section:

```markdown
## 人物一致性生成前检查

| 项目 | 检查问题 |
| --- | --- |
| Character Bible | 是否有固定人物描述 |
| 参考图 | 是否命名清楚并放在项目目录 |
| 服装发型 | 是否跨镜头一致 |
| 动作幅度 | 是否避免复杂手势和大幅转身 |
| 镜头长度 | 是否先用短镜头降低漂移 |
| 失败记录 | 是否记录脸、年龄、服装、气质变化 |
```

- [ ] **Step 5: Update `更新日志.md`**

Add:

```markdown
- 扩写第 09 卷，补齐 Character Bible、参考图策略、多镜头连续性和人物一致性风险。
```

- [ ] **Step 6: Verify task output**

Run:

```powershell
rg "Character Bible|参考图策略|服装、发型、道具|多镜头人物连续性|授权和风险|人物一致性检查清单" 第09卷_人物一致性.md
```

Expected: each term appears.

Run:

```powershell
(Get-Content -LiteralPath '第09卷_人物一致性.md' -Raw).Length
```

Expected: at least `13000`.

- [ ] **Step 7: Commit**

```powershell
git add 第09卷_人物一致性.md 分镜模板/短视频分镜模板.md 风格模板/电影感风格模板.md 参数速查/AI视频参数速查.md 更新日志.md
git commit -m "Expand volume 09 character consistency"
```

---

### Task 6: Expand Volume 10 - AI Image Generation

**Files:**
- Modify: `第10卷_AI绘图.md`
- Modify: `素材管理/素材命名与归档规范.md`
- Modify: `Prompt库/README.md`
- Modify: `参数速查/AI视频参数速查.md`
- Modify: `更新日志.md`

**Interfaces:**
- Consumes: character consistency from Task 5
- Produces: image-reference workflow used by video generation, covers, and later commercial cases

- [ ] **Step 1: Replace `第10卷_AI绘图.md` with a video-oriented AI image guide**

Use this table of contents:

```markdown
# 第 10 卷：AI 绘图

## 学习目标
## 本卷导读：AI 图像是视频项目的视觉地基
## 1. AI 绘图和 AI 视频的关系
## 2. 概念图工作流
## 3. 角色参考图
## 4. 场景参考图
## 5. 道具和产品参考图
## 6. 封面图
## 7. 分镜参考图
## 8. 图生视频起点
## 9. 常用图像工具的选择原则
## 10. 从图像到视频的提示词转换
## 11. 参考图文件命名和归档
## 12. Ross 风格视频中的图像资产推断
## 13. 常见错误
## 14. 故障排查
## 15. 本卷总结
## 16. 课后练习
## 17. 延伸阅读与核验记录
```

Content requirements:

- Explain AI images as project assets, not only pretty pictures.
- Include concept art, character reference, scene reference, prop/product reference, cover image, storyboard reference, and image-to-video examples.
- Include a table comparing tool-selection criteria rather than declaring a permanent winner.
- Include one OpenAI image-generation source note based on official documentation.
- Include file naming and folder placement rules for reference images.

- [ ] **Step 2: Update `素材管理/素材命名与归档规范.md`**

Add a section:

```markdown
## 参考图命名规范

| 类型 | 命名示例 |
| --- | --- |
| 角色参考 | REF_character_host_v01_front.png |
| 场景参考 | REF_scene_workspace_v01_wide.png |
| 道具参考 | REF_prop_laptop_v01_angle.png |
| 封面参考 | COVER_douyin_v01_title.png |
| 分镜参考 | SB_S01_v01_composition.png |
```

- [ ] **Step 3: Update `Prompt库/README.md`**

Add:

```markdown
## AI 绘图 Prompt

- 概念图 prompt。
- 角色参考图 prompt。
- 场景参考图 prompt。
- 封面图 prompt。
- 图生视频参考图 prompt。
```

- [ ] **Step 4: Update `参数速查/AI视频参数速查.md`**

Add:

```markdown
## AI 绘图到视频生成检查

| 项目 | 检查问题 |
| --- | --- |
| 用途 | 概念图、角色图、场景图、封面还是图生视频 |
| 画幅 | 是否匹配最终视频或封面 |
| 角色一致性 | 是否和 Character Bible 一致 |
| 文字 | 是否避免让图像模型生成复杂中文 |
| 文件名 | 是否能看出用途和版本 |
| 入库位置 | 是否放入 references 或 assets 目录 |
```

- [ ] **Step 5: Update `更新日志.md`**

Add:

```markdown
- 扩写第 10 卷，补齐 AI 图像在概念图、角色图、场景图、封面和图生视频中的工作流。
```

- [ ] **Step 6: Verify task output**

Run:

```powershell
rg "概念图工作流|角色参考图|场景参考图|封面图|图生视频起点|参考图文件命名|延伸阅读与核验记录" 第10卷_AI绘图.md
```

Expected: each term appears.

Run:

```powershell
(Get-Content -LiteralPath '第10卷_AI绘图.md' -Raw).Length
```

Expected: at least `12000`.

- [ ] **Step 7: Commit**

```powershell
git add 第10卷_AI绘图.md 素材管理/素材命名与归档规范.md Prompt库/README.md 参数速查/AI视频参数速查.md 更新日志.md
git commit -m "Expand volume 10 AI image workflow"
```

---

### Task 7: Phase-Two Consistency Pass

**Files:**
- Modify: `README.md`
- Modify: `学习路线.md`
- Modify: `资料来源与核验记录.md`
- Modify: `更新日志.md`

**Interfaces:**
- Consumes: completed Tasks 2-6
- Produces: synchronized reader-facing entrypoint for phase two

- [ ] **Step 1: Update `README.md`**

Add under current learning entry:

```markdown
第二阶段请在第 01-05 卷之后学习第 06-10 卷。它的重点是视频生成模型、镜头语言、导演判断、人物一致性和 AI 绘图参考图。
```

- [ ] **Step 2: Update `学习路线.md`**

Add a second-stage path:

```text
第06卷 -> 第07卷 -> 第08卷 -> 第09卷 -> 第10卷
```

Explain that this stage is for画面生成与导演判断.

- [ ] **Step 3: Update `资料来源与核验记录.md`**

Add a concise phase-two summary:

```markdown
### 第二阶段核验说明

- 第 06 卷涉及 Seedance 或同类视频模型，只记录已核验官方信息和通用工作流。
- 第 10 卷涉及 AI 图像生成，OpenAI 相关事实以官方开发文档为准。
- 第 07-09 卷以镜头语言、导演方法和人物连续性为主，属于方法论内容，不绑定单一平台。
```

- [ ] **Step 4: Run global content checks**

Run:

```powershell
rg "临时文本|尚未补完|待扩写章节" 第06卷_Seedance完全教程.md 第07卷_电影镜头语言.md 第08卷_导演思维.md 第09卷_人物一致性.md 第10卷_AI绘图.md 学习路线.md README.md
```

Expected: no output.

Run:

```powershell
$targets = @('第06卷_Seedance完全教程.md','第07卷_电影镜头语言.md','第08卷_导演思维.md','第09卷_人物一致性.md','第10卷_AI绘图.md')
foreach ($path in $targets) { $text = Get-Content -LiteralPath $path -Raw; "$path`t$($text.Length)" }
```

Expected: V06 >=12000, V07 >=14000, V08 >=12000, V09 >=13000, V10 >=12000.

- [ ] **Step 5: Commit**

```powershell
git add README.md 学习路线.md 资料来源与核验记录.md 更新日志.md
git commit -m "Polish phase two learning entrypoints"
```

---

### Task 8: Push and Final Verification

**Files:**
- No content changes unless verification finds a concrete issue.

**Interfaces:**
- Consumes: committed outputs from Tasks 1-7
- Produces: synchronized GitHub repository and status report

- [ ] **Step 1: Inspect Git history**

Run:

```powershell
git log --oneline -10
```

Expected: commits for design, plan, volumes 06-10, and phase-two polish are visible.

- [ ] **Step 2: Confirm no local media or analysis files are tracked**

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

Expected: clean branch state.

- [ ] **Step 4: Merge and push main**

From the primary checkout:

```powershell
git fetch origin
git merge --ff-only phase-two-volumes-06-10
git push origin main
```

Expected: remote `main` updates successfully.

- [ ] **Step 5: Verify remote commit**

Run:

```powershell
git rev-parse HEAD
git ls-remote origin refs/heads/main
```

Expected: remote hash matches local `HEAD`.

- [ ] **Step 6: Cleanup worktree**

Only after successful push:

```powershell
git worktree remove .worktrees\phase-two-volumes-06-10
git worktree prune
git branch -d phase-two-volumes-06-10
```

- [ ] **Step 7: Report**

Report:

- files expanded
- current character counts for volumes 06-10
- latest commit hash
- remaining scope for volumes 11-18
