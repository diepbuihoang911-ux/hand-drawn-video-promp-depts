# Hand-Drawn Video Prompts

[English](README.md) · 简体中文

把一段中文口播稿，拆成可以直接复制到 Flow / Nano Banana 的 9:16 视觉提示词。

Hand-Drawn Video Prompts 面向 AI 解说、财经观察、科技评论和知识型短视频创作者，默认输出：

- 4–6 秒一个的语义镜头
- 英文 Flow 生图提示词
- 英文 Flow 图生视频提示词
- 画面内嵌的中文短关键词
- 中文口播对应关系和镜头视觉隐喻
- 实体准确性提醒：国旗、公司、Logo、知名人物和数字

## 为什么做这个 Skill

很多 AI 视频工作流卡在两个地方：

1. 文案有观点，但不知道每 5 秒应该画什么；
2. 提示词能生成画面，却很难保持统一风格、固定背景和可用的字幕安全区。

这个 Skill 把“文案理解 → 视觉隐喻 → 静帧 → 图生视频”的中间层固定下来，让创作者可以批量复制、生成和组装。

## 视觉基线

默认风格是现代 Q 版蜡笔社论插画：

- 9:16 竖版
- 固定暖白画布：`#F8F6EF`
- 极轻微纸张颗粒
- 粗黑手绘线
- 向日葵黄、钴蓝、番茄红
- 自然、克制的 Q 版人物比例
- 2–4 个清晰视觉组，避免海报式堆叠
- 关键词直接写在纸面或物件旁，不使用便签纸、标签卡或独立白卡
- 底部留给视频字幕

## 快速使用

1. 打开 Codex，并加载这个 Skill。
2. 粘贴一段中文口播稿。
3. 指定“只写提示词”或“生成完整视频”。
4. 将每个英文提示词复制到 Flow / Nano Banana。
5. 使用完成静帧作为图生视频的 Last Frame；使用固定的 `#F8F6EF` 空白纸作为 First Frame。

示例请求：

```text
请把下面这段中文口播稿拆成 Flow 生图和图生视频提示词，关键词直接写在画面里，背景固定为 #F8F6EF，底部留字幕区：

AI 让想法变得更便宜，但现实验证仍然很慢。
```

## 输出格式

```text
镜头 01
对应口播：
建议时长：
视觉隐喻：
画面中文关键词：

【Flow 生图提示词】
<copy-ready English prompt>

【Flow 图生视频提示词】
<copy-ready English prompt>

【实体准确性提醒】
<what needs a reference image or deterministic overlay>
```

## 重要设计决定

### 中文关键词不是贴纸

关键词是插画的一部分，直接写在暖白纸面、留白处或相关物件旁。默认使用小号手写字，文字区域不超过画面高度的 10%–12%，绝不占用底部字幕区。

### 真实实体要分层处理

生成模型可以负责 Q 版构图、动作和环境，但不能保证精确复刻每一个 Logo、国旗、公司字标或知名人物脸部。

- 国旗：写明官方结构、颜色、比例和符号；核心镜头建议使用参考图或原始素材叠加。
- Logo：建议使用原始 Logo 作为参考图或后期叠加。
- 知名人物：使用明显非写实的 Q 版漫画化身份锚点，不规避安全限制，不做写实人脸克隆。
- 数字、日期和长句：优先留给确定性字幕层。

### 背景颜色要固定

“Warm white paper”不是精确色号。Skill 默认使用 `#F8F6EF`，并明确禁止黑色背景、灰褐偏色、米黄色渐变、暗角和镜头间底色漂移。若需要像素级一致，应使用固定 First Frame 或在后处理中统一填色。

## 目录

```text
hand-drawn-video-prompts/
├── SKILL.md                         # Skill 主规则
├── references/
│   ├── style-guide.md               # 风格、色彩、构图、运动语法
│   ├── output-example.md            # 标准输出示例
│   └── automation-workflow.md       # 自动成片工作流边界
├── outputs/                         # 公开示例提示词与测试输出
└── work/                            # 研究过程与测试记录
```

## 公开示例

- [AI CapEx Flow 图生视频提示词](outputs/flow-image-to-video-prompts-ai-capex-01-07.md)
- [AI CapEx Skill 测试输出](outputs/q-doodle-flow-skill-v1-ai-capex-test.md)
- [Nano Banana / Flow 提示词示例](outputs/flow-nano-q-doodle-prompts.md)
- [视觉风格参考图](outputs/q-doodle-style-reference.png)

## 当前边界

这是一个提示词和视觉拆解 Skill，不包含：

- Flow / Nano Banana API 自动调用
- 自动生图服务部署
- 自动生成视频服务部署
- 复杂版本管理
- 对生成结果的像素级一致性保证

它可以与 Flow、Nano Banana、ChatCut 等工具配合使用。自动成片模式的可用能力取决于当前账号、工具权限和浏览器连接状态。

## License

MIT License。欢迎 fork、改进和提交新的风格参考或输出示例。
