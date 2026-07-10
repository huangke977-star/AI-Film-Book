# Phase Four Volumes 14-18 Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Expand volumes 14-18 into complete beginner-friendly chapters covering commercial ad cases, AI short drama, n8n automation, MCP workflows, and commercial monetization.

**Architecture:** This is the final Markdown knowledge-base expansion. Each volume is a separate tutorial deliverable, followed by entrypoint/support-file updates that mark the book as complete through volume 18.

**Tech Stack:** Markdown, Git, PowerShell verification commands, official web documentation for time-sensitive automation/protocol/commercial facts.

## Global Constraints

- Keep the reader profile as complete beginner.
- Do not write platform revenue promises, ad ROI guarantees, viral guarantees, gray-hat tactics, review bypasses, scraping abuse, stolen-material workflows, or fake engagement methods.
- Do not write exact n8n, MCP, platform API, marketplace, ad-platform, or short-drama platform pricing, entitlements, UI paths, or revenue rules unless verified from official current sources.
- n8n and MCP content must emphasize credentials, least privilege, logs, failures, manual review, and security boundaries.
- Commercial content must emphasize scope, authorization, client confirmation, delivery records, and maintenance.
- Keep all content in Chinese Markdown.
- Commit each major deliverable separately.

---

## File Structure

Files to modify:

- `第14卷_商业广告案例.md`: complete commercial ad project tutorial.
- `第15卷_AI短剧案例.md`: complete AI short-drama pilot tutorial.
- `第16卷_n8n自动化.md`: complete automation tutorial.
- `第17卷_MCP工作流.md`: complete MCP workflow tutorial.
- `第18卷_商业变现.md`: complete monetization tutorial.
- `README.md`: full book learning entry and delivered content.
- `学习路线.md`: fourth-stage route.
- `资料来源与核验记录.md`: phase-four source records.
- `更新日志.md`: phase-four changes.
- `工具排行榜/2026_AI视频工具清单.md`: automation/MCP/business tool positioning.
- `参数速查/AI视频参数速查.md`: commercial, short-drama, automation, MCP, monetization checks.
- `发布运营/商业交付检查清单.md`: quotation, authorization, maintenance, renewal checks.
- `故障排查/README.md`: client revision, short-drama continuity, automation/MCP failures.

Files already created:

- `docs/superpowers/specs/2026-07-10-phase-four-volumes-14-18-design.md`: design source for this plan.

## Task 1: Source Verification Notes

**Files:**
- Modify: `资料来源与核验记录.md`
- Modify: `更新日志.md`

**Interfaces:**
- Consumes: official source links from current web verification.
- Produces: stable source section referenced by volumes 14-18.

- [ ] **Step 1: Verify official source categories**

Use official sources for:

```text
n8n workflows, nodes, credentials, executions, error handling, security
Model Context Protocol tools, resources, prompts, security principles
OpenAI Codex or platform MCP documentation when referenced
FTC advertising/AI claims and endorsement guidance when discussing ad claims
U.S. Copyright Office AI/copyright guidance when discussing copyright boundary
China Advertising Law or internet-ad management sources only as high-level reference, not legal advice
```

Expected: only official domains are recorded; if a platform rule is not verified, content stays workflow-level.

- [ ] **Step 2: Add phase-four source policy**

Append a `第四阶段商业、自动化与变现核验` section to `资料来源与核验记录.md` with links and the 2026-07-10 verification date.

- [ ] **Step 3: Add changelog entry**

Add one bullet in `更新日志.md`:

```markdown
- 新增第四阶段第 14-18 卷扩写设计与实施计划，范围为商业广告案例、AI 短剧案例、n8n 自动化、MCP 工作流和商业变现。
```

- [ ] **Step 4: Commit**

```powershell
git add 资料来源与核验记录.md 更新日志.md
git commit -m "Record phase four source policy"
```

Expected: one source-prep commit.

## Task 2: Expand Volume 14 Commercial Ad Case

**Files:**
- Modify: `第14卷_商业广告案例.md`

**Interfaces:**
- Consumes: earlier volumes 01-13 and phase-four source policy.
- Produces: complete commercial ad case chapter.

- [ ] **Step 1: Replace placeholder with complete chapter**

Write `第14卷_商业广告案例.md` with these sections:

```text
学习目标
本卷导读：商业广告不是炫技样片
1. 商业广告项目的完整流程
2. 客户需求访谈
3. 广告 Brief
4. 报价边界和交付范围
5. 脚本和卖点结构
6. 商业广告分镜
7. 产品镜头和品牌风格
8. AI 生成任务拆解
9. 配音、音乐、字幕和剪辑
10. 客户修改管理
11. 交付文件包
12. 合规和授权提醒
13. 完整案例
14. 常见错误
15. 故障排查
16. 7 天练习路线
17. 本卷总结
18. 课后练习
19. 延伸阅读与核验记录
```

- [ ] **Step 2: Verify volume 14 content**

```powershell
$text = Get-Content -Raw '.\第14卷_商业广告案例.md'
"chars=$($text.Length)"
rg -n "待扩写章节|TODO|TBD|稳赚|保证投放|绕过审核|刷量" '.\第14卷_商业广告案例.md'
```

Expected: `chars` is at least 12000. No placeholders or unsafe commercial claims.

- [ ] **Step 3: Commit**

```powershell
git add 第14卷_商业广告案例.md
git commit -m "Expand volume 14 commercial ad case"
```

## Task 3: Expand Volume 15 AI Short Drama Case

**Files:**
- Modify: `第15卷_AI短剧案例.md`

**Interfaces:**
- Consumes: character consistency, director thinking, voice/music/editing chapters.
- Produces: complete short-drama pilot chapter.

- [ ] **Step 1: Replace placeholder with complete chapter**

Write `第15卷_AI短剧案例.md` with these sections:

```text
学习目标
本卷导读：短剧先做试播集
1. AI 短剧和普通短视频的区别
2. 短剧最小闭环
3. 人设表
4. 人物关系表
5. 世界观和场景表
6. 分集大纲
7. 单集剧本
8. 镜头连续性
9. 对话和配音
10. 低成本试播集
11. 数据复盘
12. 是否继续制作
13. 完整案例
14. 常见错误
15. 故障排查
16. 7 天练习路线
17. 本卷总结
18. 课后练习
19. 延伸阅读与核验记录
```

- [ ] **Step 2: Verify volume 15 content**

```powershell
$text = Get-Content -Raw '.\第15卷_AI短剧案例.md'
"chars=$($text.Length)"
rg -n "待扩写章节|TODO|TBD|抄袭|搬运|洗稿|必爆" '.\第15卷_AI短剧案例.md'
```

Expected: `chars` is at least 11000. No placeholders or unsafe content-production claims.

- [ ] **Step 3: Commit**

```powershell
git add 第15卷_AI短剧案例.md
git commit -m "Expand volume 15 AI short drama case"
```

## Task 4: Expand Volume 16 n8n Automation

**Files:**
- Modify: `第16卷_n8n自动化.md`

**Interfaces:**
- Consumes: official n8n source policy.
- Produces: beginner-safe automation chapter.

- [ ] **Step 1: Replace placeholder with complete chapter**

Write `第16卷_n8n自动化.md` with these sections:

```text
学习目标
本卷导读：自动化不是无人生产
1. 自动化适合做什么
2. 不适合自动化的环节
3. n8n 基本概念
4. 工作流、节点、触发器、凭证和执行记录
5. AI 视频自动化流程图
6. 选题收集自动化
7. 脚本草稿自动化
8. 生成任务清单自动化
9. 下载和归档自动化
10. 失败重试和人工终审
11. 成本控制
12. 安全和密钥
13. 批量视频工作流案例
14. 常见错误
15. 故障排查
16. 7 天练习路线
17. 本卷总结
18. 课后练习
19. 延伸阅读与核验记录
```

- [ ] **Step 2: Verify volume 16 content**

```powershell
$text = Get-Content -Raw '.\第16卷_n8n自动化.md'
"chars=$($text.Length)"
rg -n "待扩写章节|TODO|TBD|无人审核|自动发布所有|泄露密钥|绕过限制" '.\第16卷_n8n自动化.md'
```

Expected: `chars` is at least 11000. No unsafe automation guidance.

- [ ] **Step 3: Commit**

```powershell
git add 第16卷_n8n自动化.md
git commit -m "Expand volume 16 n8n automation workflow"
```

## Task 5: Expand Volume 17 MCP Workflow

**Files:**
- Modify: `第17卷_MCP工作流.md`

**Interfaces:**
- Consumes: official MCP source policy.
- Produces: complete MCP workflow chapter for AI video projects.

- [ ] **Step 1: Replace placeholder with complete chapter**

Write `第17卷_MCP工作流.md` with these sections:

```text
学习目标
本卷导读：Agent 需要工具，但工具需要边界
1. MCP 基本概念
2. Agent 为什么需要工具
3. Tool、Resource、Prompt 的区别
4. 文件系统 MCP
5. 浏览器 MCP
6. 平台 API 和生成工具
7. LibTV Skill 或类似工作流
8. Codex + MCP 视频项目示例
9. 权限最小化
10. 密钥和账号安全
11. 日志、审计和回滚
12. MCP 能力清单
13. 常见错误
14. 故障排查
15. 7 天练习路线
16. 本卷总结
17. 课后练习
18. 延伸阅读与核验记录
```

- [ ] **Step 2: Verify volume 17 content**

```powershell
$text = Get-Content -Raw '.\第17卷_MCP工作流.md'
"chars=$($text.Length)"
rg -n "待扩写章节|TODO|TBD|全权限|泄露密钥|绕过登录|盗取" '.\第17卷_MCP工作流.md'
```

Expected: `chars` is at least 11000. No unsafe MCP/tooling guidance.

- [ ] **Step 3: Commit**

```powershell
git add 第17卷_MCP工作流.md
git commit -m "Expand volume 17 MCP workflow"
```

## Task 6: Expand Volume 18 Commercial Monetization

**Files:**
- Modify: `第18卷_商业变现.md`

**Interfaces:**
- Consumes: all previous volumes.
- Produces: final monetization chapter.

- [ ] **Step 1: Replace placeholder with complete chapter**

Write `第18卷_商业变现.md` with these sections:

```text
学习目标
本卷导读：变现来自可交付能力
1. AI 视频服务类型
2. 从样片到服务菜单
3. 报价方式
4. 成本核算
5. 项目周期和修改边界
6. 客户沟通
7. 版权、肖像、声音和音乐授权
8. 个人 IP 内容
9. 模板和课程产品化
10. 顾问和内训
11. 维护和复购
12. 不建议做的变现方式
13. 90 天成长路线
14. 常见错误
15. 故障排查
16. 本卷总结
17. 课后练习
18. 延伸阅读与核验记录
```

- [ ] **Step 2: Verify volume 18 content**

```powershell
$text = Get-Content -Raw '.\第18卷_商业变现.md'
"chars=$($text.Length)"
rg -n "待扩写章节|TODO|TBD|稳赚|月入|保证收益|刷量|搬运|洗稿|灰产" '.\第18卷_商业变现.md'
```

Expected: `chars` is at least 12000. No unsafe monetization claims.

- [ ] **Step 3: Commit**

```powershell
git add 第18卷_商业变现.md
git commit -m "Expand volume 18 commercial monetization"
```

## Task 7: Update Full-Book Entrypoints and Support Files

**Files:**
- Modify: `README.md`
- Modify: `学习路线.md`
- Modify: `更新日志.md`
- Modify: `工具排行榜/2026_AI视频工具清单.md`
- Modify: `参数速查/AI视频参数速查.md`
- Modify: `发布运营/商业交付检查清单.md`
- Modify: `故障排查/README.md`

**Interfaces:**
- Consumes: completed volumes 14-18.
- Produces: full-book entrypoint.

- [ ] **Step 1: Update README**

Add volumes 14-18 to the learning route and delivered content list.

- [ ] **Step 2: Update 学习路线**

Add a fourth-stage section titled:

```markdown
## 第四阶段：商业案例、自动化与变现
```

Include:

```text
第14卷 -> 第15卷 -> 第16卷 -> 第17卷 -> 第18卷
```

- [ ] **Step 3: Update support files**

Add compact checks for:

```markdown
商业广告项目检查
AI 短剧试播集检查
n8n 自动化检查
MCP 权限检查
商业变现检查
```

- [ ] **Step 4: Verify entrypoint consistency**

```powershell
rg -n "第14卷|第15卷|第16卷|第17卷|第18卷|第四阶段|商业案例、自动化与变现" README.md 学习路线.md 更新日志.md 工具排行榜 参数速查 发布运营 故障排查
```

Expected: fourth-stage route appears in README and learning route; support files mention commercial/automation/MCP checks.

- [ ] **Step 5: Commit**

```powershell
git add README.md 学习路线.md 更新日志.md 工具排行榜/2026_AI视频工具清单.md 参数速查/AI视频参数速查.md 发布运营/商业交付检查清单.md 故障排查/README.md
git commit -m "Polish full book learning entrypoints"
```

## Task 8: Final Verification, Merge, Push

**Files:**
- Verify all modified files.

**Interfaces:**
- Consumes: all phase-four commits.
- Produces: pushed GitHub repository.

- [ ] **Step 1: Run target placeholder scan**

```powershell
rg -n "待扩写章节|TODO|TBD|临时文本|尚未补完" '.\第14卷_商业广告案例.md' '.\第15卷_AI短剧案例.md' '.\第16卷_n8n自动化.md' '.\第17卷_MCP工作流.md' '.\第18卷_商业变现.md'
```

Expected: no hits.

- [ ] **Step 2: Run character counts**

```powershell
Get-ChildItem '.\第14卷_商业广告案例.md','.\第15卷_AI短剧案例.md','.\第16卷_n8n自动化.md','.\第17卷_MCP工作流.md','.\第18卷_商业变现.md' | ForEach-Object {
  $text = Get-Content -Raw $_.FullName
  [PSCustomObject]@{ File = $_.Name; Chars = $text.Length }
}
```

Expected:

```text
第14卷_商业广告案例.md >= 12000
第15卷_AI短剧案例.md >= 11000
第16卷_n8n自动化.md >= 11000
第17卷_MCP工作流.md >= 11000
第18卷_商业变现.md >= 12000
```

- [ ] **Step 3: Check git status**

```powershell
git status --short --branch
git log --oneline -12
```

Expected: clean branch after commits, latest commits are phase-four commits.

- [ ] **Step 4: Push**

```powershell
git push origin main
git rev-parse HEAD
git ls-remote origin refs/heads/main
```

Expected: remote `main` hash equals local `HEAD`.

