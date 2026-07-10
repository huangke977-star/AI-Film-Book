# Ross 案例端到端提示词模板

本模板用于复刻“Codex + LibTV 完成 AI 视频”的工作流型短视频。

## 与第 03 卷的关系

第 03 卷讲如何指挥 Codex；本模板是 Ross 案例的可复制指令库。读者可以先照抄，再逐步替换主题、风格和镜头。

## 1. 项目初始化

```text
你是我的 AI 视频项目制片助理。
我要制作一条 30 秒竖屏短视频，主题是“用 Codex 和 LibTV 完成一条 AI 视频”。
目标观众是 AI 创作者和短视频创作者。
请在当前目录创建 brief.md、script.md、storyboard.md、style_guide.md、iteration_log.md。

要求：
1. 风格是真实电影摄影、创作者工作室、冷暖对比、低饱和。
2. 视频结构要展示：想法 -> Codex 拆解 -> LibTV 生成 -> 剪辑 -> 成片。
3. 不要写成散文，所有关键内容用表格或清单。
```

## 2. 分镜生成

```text
请读取 brief.md 和 script.md。
生成 6 个镜头的分镜表，保存到 storyboard.md。

每个镜头必须包含：
- 镜头编号
- 时长
- 画面
- 主体
- 动作
- 镜头类型
- 运镜
- 声音
- 镜头目的

限制：
- 每个镜头只表达一个主要动作。
- 全片必须适合 9:16 竖屏。
- 不要出现无法生成的复杂 UI 文字。
```

## 3. 风格手册生成

```text
请根据 brief.md 和 storyboard.md，写一份 style_guide.md。

必须包含：
- 画幅
- 色彩
- 光线
- 镜头质感
- 场景元素
- 禁止项
- 统一角色或创作者形象

风格目标：真实、专业、有未来感，但不要科幻过度。
```

## 4. LibTV 镜头提示词生成

```text
请读取 brief.md、storyboard.md、style_guide.md。
为每个镜头生成单独的 LibTV 视频提示词文件：
prompts/shot_01.md
prompts/shot_02.md
prompts/shot_03.md
...

每个文件必须包含：
1. 镜头目的
2. 中文提示词
3. English Prompt
4. Negative Prompt
5. 参数建议
6. 可能失败点

每条提示词必须包含主体、场景、动作、镜头类型、运镜、光线、色彩、风格、画幅。
```

## 5. 失败样本复盘

```text
我已经完成第一轮生成，下面是问题记录：

S01：
S02：
S03：
S04：
S05：
S06：

请根据这些问题更新对应 prompts 文件，并把本轮问题和修改理由追加到 iteration_log.md。

要求：
1. 只修改有问题的镜头。
2. 保留可用镜头。
3. 不改变整体风格。
4. 每条修改都说明原因。
```

## 6. 发布文案生成

```text
请根据 brief.md、storyboard.md、iteration_log.md，生成 5 个抖音标题和 3 版发布文案。

要求：
- 标题强调“Codex + LibTV”和“从手搓提示词到 Agent 工作流”。
- 不夸大工具能力。
- 文案要有过程感和结果证明。
- 输出话题标签建议。
```

