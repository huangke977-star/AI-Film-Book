# Phase Three Volumes 11-13 Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Expand volumes 11-13 into complete beginner-friendly chapters that teach AI voiceover, AI music, and editing/final delivery.

**Architecture:** This is a Markdown knowledge-base expansion. Each major volume is edited as an independent deliverable, then entrypoint/supporting documents are updated to connect the new phase into the full learning route.

**Tech Stack:** Markdown, Git, PowerShell verification commands, official web documentation for time-sensitive platform facts.

## Global Constraints

- Keep the reader profile as complete beginner.
- Do not write exact platform pricing, subscription entitlements, hidden settings, current permissions, or button paths unless verified from official current sources.
- Prefer stable workflow methods over tool rankings.
- Treat OpenAI, ElevenLabs, Suno, Udio, Adobe, CapCut/Jianying, DaVinci Resolve, and Final Cut Pro facts as time-sensitive.
- Do not provide instructions for unauthorized voice cloning, impersonation, copyright evasion, or license bypassing.
- Keep all content in Chinese Markdown.
- Commit each major deliverable separately.

---

## File Structure

Files to modify:

- `第11卷_AI配音.md`: full AI voiceover tutorial.
- `第12卷_AI音乐.md`: full AI music tutorial.
- `第13卷_剪映与PR.md`: full editing and export tutorial.
- `README.md`: current learning entry and delivered content list.
- `学习路线.md`: third-stage learning route.
- `资料来源与核验记录.md`: phase-three official source records.
- `更新日志.md`: phase-three changes.
- `工具排行榜/2026_AI视频工具清单.md`: voice/music/editing tool positioning.
- `参数速查/AI视频参数速查.md`: audio/music/edit/export quick checks.
- `发布运营/商业交付检查清单.md`: commercial delivery checks for voice, music, subtitles, export.
- `故障排查/README.md`: voice/music/editing troubleshooting notes.

Files already created:

- `docs/superpowers/specs/2026-07-10-phase-three-volumes-11-13-design.md`: design source for this plan.

## Task 1: Source Verification Notes

**Files:**
- Modify: `资料来源与核验记录.md`
- Modify: `更新日志.md`

**Interfaces:**
- Consumes: official source links from current web verification.
- Produces: stable source section referenced by volumes 11-13.

- [ ] **Step 1: Verify official source categories**

Run official-source searches for:

```text
OpenAI audio / text-to-speech
ElevenLabs voice cloning / terms / commercial use
Suno terms / commercial use
Udio terms / commercial use
Adobe Premiere Pro captions and export
CapCut or Jianying official help if accessible
Apple Final Cut Pro export/share support
Blackmagic Design DaVinci Resolve product/help pages
```

Expected: use only official domains or keep the statement workflow-level.

- [ ] **Step 2: Add phase-three source policy**

Append a `第三阶段声音、音乐、剪辑核验` section to `资料来源与核验记录.md` with links and the 2026-07-10 verification date.

- [ ] **Step 3: Add changelog entry**

Add one bullet in `更新日志.md`:

```markdown
- 新增第三阶段第 11-13 卷扩写设计与实施计划，范围为 AI 配音、AI 音乐、剪映与 PR 后期成片流程。
```

- [ ] **Step 4: Commit**

```powershell
git add 资料来源与核验记录.md 更新日志.md docs/superpowers/plans/2026-07-10-phase-three-volumes-11-13-plan.md
git commit -m "Plan phase three implementation"
```

Expected: one planning/source-prep commit.

## Task 2: Expand Volume 11 AI Voiceover

**Files:**
- Modify: `第11卷_AI配音.md`

**Interfaces:**
- Consumes: phase-three source policy, existing volume style from `第10卷_AI绘图.md`.
- Produces: complete chapter referenced by README, learning route, troubleshooting, and parameter checklist.

- [ ] **Step 1: Replace placeholder with complete chapter**

Write `第11卷_AI配音.md` with these sections:

```text
学习目标
本卷导读：声音是视频信息的时间轴
1. AI 配音在视频流程中的位置
2. 旁白、口播、角色配音和声音克隆
3. 口播稿改写
4. TTS 工作流
5. 中文配音工具选择原则
6. 英文配音工具选择原则
7. 声音克隆的边界
8. 配音 Brief 模板
9. TTS 任务卡
10. 声音版本评审
11. 音频清理和响度
12. 文件命名与入库
13. 和剪辑软件配合
14. Ross 风格案例中的配音推断
15. 商用授权检查
16. 常见错误
17. 故障排查
18. 7 天练习路线
19. 本卷总结
20. 课后练习
21. 延伸阅读与核验记录
```

- [ ] **Step 2: Verify volume 11 content**

Run:

```powershell
$text = Get-Content -Raw '.\第11卷_AI配音.md'
"chars=$($text.Length)"
rg -n "待扩写章节|TODO|TBD|价格|套餐" '.\第11卷_AI配音.md'
```

Expected: `chars` is at least 12000. No placeholder hits. Price/subscription hits only if used as warnings such as "不要写死".

- [ ] **Step 3: Commit**

```powershell
git add 第11卷_AI配音.md
git commit -m "Expand volume 11 AI voiceover workflow"
```

Expected: one volume-11 commit.

## Task 3: Expand Volume 12 AI Music

**Files:**
- Modify: `第12卷_AI音乐.md`

**Interfaces:**
- Consumes: completed volume 11 terminology for voice/music conflict.
- Produces: complete music chapter referenced by editing chapter and support files.

- [ ] **Step 1: Replace placeholder with complete chapter**

Write `第12卷_AI音乐.md` with these sections:

```text
学习目标
本卷导读：音乐是情绪和节奏的骨架
1. AI 音乐在视频项目中的位置
2. 背景音乐、主题曲、音效和氛围声
3. 音乐 Brief
4. AI 音乐 Prompt
5. Suno 或同类工具的工作流理解
6. Udio 或同类工具的工作流理解
7. 节奏、BPM 和剪辑点
8. 30 秒短视频音乐结构
9. 音乐与人声避让
10. 音效和转场声音
11. 音乐版本评审
12. 授权和商用风险
13. 文件命名与入库
14. Ross 风格案例中的音乐推断
15. 常见错误
16. 故障排查
17. 7 天练习路线
18. 本卷总结
19. 课后练习
20. 延伸阅读与核验记录
```

- [ ] **Step 2: Verify volume 12 content**

Run:

```powershell
$text = Get-Content -Raw '.\第12卷_AI音乐.md'
"chars=$($text.Length)"
rg -n "待扩写章节|TODO|TBD|破解|绕过版权" '.\第12卷_AI音乐.md'
```

Expected: `chars` is at least 11000. No placeholder or unsafe copyright bypass instructions.

- [ ] **Step 3: Commit**

```powershell
git add 第12卷_AI音乐.md
git commit -m "Expand volume 12 AI music workflow"
```

Expected: one volume-12 commit.

## Task 4: Expand Volume 13 Jianying and Premiere Pro

**Files:**
- Modify: `第13卷_剪映与PR.md`

**Interfaces:**
- Consumes: completed volume 11 and 12 assets, existing project naming conventions.
- Produces: complete editing chapter that closes the post-production loop.

- [ ] **Step 1: Replace placeholder with complete chapter**

Write `第13卷_剪映与PR.md` with these sections:

```text
学习目标
本卷导读：剪辑是最后的导演环节
1. AI 生成不是成片
2. 剪映、Premiere Pro、DaVinci Resolve、Final Cut Pro 的定位
3. 剪辑前文件整理
4. 工程目录和版本
5. 时间线轨道命名
6. 粗剪
7. 精剪
8. 字幕工作流
9. 配音、音乐和音效混音
10. 调色统一
11. AI 瑕疵处理
12. 封面和标题
13. 导出参数
14. 平台发布前检查
15. Ross 风格短视频剪辑结构
16. 商业交付文件包
17. 常见错误
18. 故障排查
19. 7 天练习路线
20. 本卷总结
21. 课后练习
22. 延伸阅读与核验记录
```

- [ ] **Step 2: Verify volume 13 content**

Run:

```powershell
$text = Get-Content -Raw '.\第13卷_剪映与PR.md'
"chars=$($text.Length)"
rg -n "待扩写章节|TODO|TBD|一键成片|永久最好" '.\第13卷_剪映与PR.md'
```

Expected: `chars` is at least 13000. No placeholder or one-click overpromise.

- [ ] **Step 3: Commit**

```powershell
git add 第13卷_剪映与PR.md
git commit -m "Expand volume 13 editing workflow"
```

Expected: one volume-13 commit.

## Task 5: Update Learning Entrypoints and Support Files

**Files:**
- Modify: `README.md`
- Modify: `学习路线.md`
- Modify: `更新日志.md`
- Modify: `工具排行榜/2026_AI视频工具清单.md`
- Modify: `参数速查/AI视频参数速查.md`
- Modify: `发布运营/商业交付检查清单.md`
- Modify: `故障排查/README.md`

**Interfaces:**
- Consumes: completed volumes 11-13.
- Produces: coherent third-stage entrypoint for the user.

- [ ] **Step 1: Update README**

Change the current learning entry from:

```text
第06卷 -> 第07卷 -> 第08卷 -> 第09卷 -> 第10卷
```

to include:

```text
第11卷 -> 第12卷 -> 第13卷
```

Add delivered-content bullets for volumes 11-13.

- [ ] **Step 2: Update 学习路线**

Add a third-stage section titled:

```markdown
## 第三阶段：声音、音乐、剪辑与成片
```

Include the route:

```text
第11卷 -> 第12卷 -> 第13卷
```

- [ ] **Step 3: Update support files**

Add compact tables:

```markdown
音频生成前检查
音乐生成前检查
剪辑导出前检查
商业项目声音与音乐授权检查
```

Keep entries workflow-level and source-aware.

- [ ] **Step 4: Verify entrypoint consistency**

Run:

```powershell
rg -n "第11卷|第12卷|第13卷|第三阶段|声音、音乐、剪辑" README.md 学习路线.md 更新日志.md 工具排行榜 参数速查 发布运营 故障排查
```

Expected: third-stage route appears in README and learning route; support files mention voice/music/editing checks.

- [ ] **Step 5: Commit**

```powershell
git add README.md 学习路线.md 更新日志.md 工具排行榜/2026_AI视频工具清单.md 参数速查/AI视频参数速查.md 发布运营/商业交付检查清单.md 故障排查/README.md
git commit -m "Polish phase three learning entrypoints"
```

Expected: one support-file commit.

## Task 6: Final Verification, Merge, Push

**Files:**
- Verify all modified files.

**Interfaces:**
- Consumes: all phase-three commits.
- Produces: pushed GitHub repository.

- [ ] **Step 1: Run full placeholder scan**

```powershell
rg -n "待扩写章节|TODO|TBD|临时文本|尚未补完" .
```

Expected: no hits in deliverable Markdown except historical plan/spec text where explicitly describing placeholder removal.

- [ ] **Step 2: Run character counts**

```powershell
Get-ChildItem '.\第11卷_AI配音.md','.\第12卷_AI音乐.md','.\第13卷_剪映与PR.md' | ForEach-Object {
  $text = Get-Content -Raw $_.FullName
  [PSCustomObject]@{ File = $_.Name; Chars = $text.Length }
}
```

Expected:

```text
第11卷_AI配音.md >= 12000
第12卷_AI音乐.md >= 11000
第13卷_剪映与PR.md >= 13000
```

- [ ] **Step 3: Check git status**

```powershell
git status --short --branch
git log --oneline -8
```

Expected: clean branch after commits, latest commits are phase-three commits.

- [ ] **Step 4: Push**

```powershell
git push origin main
git rev-parse HEAD
git ls-remote origin refs/heads/main
```

Expected: remote `main` hash equals local `HEAD`.

