# Data Structures Skills

**中文数据结构学习 · 无代码讲解 · 个性化刷题 · 8 个 AIGC 平台 · 12 种语言背景**

一套可复用的数据结构学习 Skill：解释概念、提供分层提示，根据实际可用的 memory 或用户提供的信息推荐 LeetCode、Codeforces 题目，并通过复盘调整下一步。

**教学输出不包含程序、伪代码、SQL 查询语句或图形源码。** 语言背景用于解释语义和选择练习，不用于代写答案。

[开始使用](#快速开始) · [支持平台](#支持的-aigc) · [内容目录](#内容目录) · [验收场景](data-structures/references/acceptance-scenarios.md) · [检查记录](dist/VALIDATION.md)

## 快速开始

### 方式一：普通聊天

1. 复制[通用启动指令](data-structures/assets/portable-core.md)到你使用的 AIGC。
2. 提供当前学习目标、熟悉语言及已知学习情况；有学习摘要时一起提供。
3. 需要完整教学规则时，附上或粘贴[通用单文件版](dist/data-structures-portable.md)。

不需要先填写完整问卷。没有长期 memory 时，使用[跨会话交接模板](data-structures/assets/templates/memory-handoff.md)延续学习。

### 方式二：原生 Skill

下载[标准 Skill ZIP](dist/data-structures.zip)，按目标平台的接入说明添加。保留 data-structures 顶层目录和其中的相对路径；[SKILL.md](data-structures/SKILL.md)是主入口。

本仓库提供技能源文件和发布产物，不会自动安装到个人技能目录或外部账户。不同平台的具体方式见下表。

## 支持的 AIGC

| 平台 | 本包提供的接入方式 | 使用说明 |
| --- | --- | --- |
| Claude | 原生 Skill ZIP / 通用文本 | [Claude](data-structures/assets/platforms/claude.md) |
| ChatGPT | 支持的 Skills 入口 / 项目资料 / 通用文本 | [ChatGPT](data-structures/assets/platforms/chatgpt.md) |
| Grok | 通用文本，按界面能力提供资料 | [Grok](data-structures/assets/platforms/grok.md) |
| Gemini | Gems 指令与知识资料 / 通用文本 | [Gemini](data-structures/assets/platforms/gemini.md) |
| DeepSeek | 通用文本 / 支持的 API 指令消息 | [DeepSeek](data-structures/assets/platforms/deepseek.md) |
| Qwen | 通用文本 / 按具体模型支持的指令接入 | [Qwen](data-structures/assets/platforms/qwen.md) |
| GLM | 通用文本 / 对话 API 指令消息 | [GLM](data-structures/assets/platforms/glm.md) |
| Kimi | 通用文本 / 按官方对话协议接入 | [Kimi](data-structures/assets/platforms/kimi.md) |

这是适配方式说明，不代表所有平台使用同一安装机制，也不表示已在八个平台完成实测。官方依据、核验日期和能力不足时的处理方式见[平台支持矩阵](data-structures/references/platform-support.md)。

## 学习范围

- **基础结构**：数组、字符串、链表、栈、队列、哈希表。
- **树与图**：树的遍历、搜索树、堆、字典树、图的表示与遍历、并查集等。
- **应用思维**：双指针、滑动窗口、前缀和、二分、单调结构及按需进阶主题。
- **个性化练习**：按先修、薄弱点、已做题、时间和提示依赖筛选题目。
- **学习复盘**：区分题意、建模、结构选择、正确性和复杂度方面的卡点。

**语言背景**：C++、Java、Python、C、JavaScript、Go、Rust、C#、TypeScript、R、Visual Basic、SQL。平台题目能否用指定语言提交，需要单独核验。

**练习平台**：LeetCode、Codeforces。实际推荐前核验官方题面和相关限制；不维护一份宣称永远正确的静态题库，不把两个平台的难度机械换算。

## 内容目录

标准技能目录包含 24 个源文件：主入口、UI 元数据、9 份参考资料、8 份平台说明、4 份记录模板和通用启动指令。dist 目录提供可分享的发布产物。

| 部分 | 文件 | 作用 |
| --- | --- | --- |
| 主入口 | SKILL.md | 触发范围、输出边界、任务路由与共通规则 |
| UI 元数据 | agents/openai.yaml | 展示名称、简短说明与默认提示词 |
| 学习画像 | [learner-profile.md](data-structures/references/learner-profile.md) | memory 来源、冲突处理与掌握证据 |
| 教学方法 | [teaching-playbook.md](data-structures/references/teaching-playbook.md) | 概念推演、常见误区与分层提示 |
| 知识路线 | [topic-roadmap.md](data-structures/references/topic-roadmap.md) | 基础结构、树图、常见方法与按需进阶 |
| 语言背景 | [language-backgrounds.md](data-structures/references/language-backgrounds.md) | 十二种语言的理解重点与限制 |
| 题目推荐 | [problem-recommendation.md](data-structures/references/problem-recommendation.md) | 候选筛选、官方核验、去重与难度控制 |
| 复盘进阶 | [review-and-progression.md](data-structures/references/review-and-progression.md) | 卡点分类、变式、复习和下一步 |
| 平台适配 | references/platform-support.md 与 assets/platforms 下的八份说明 | 接入区别、官方依据和启动示例 |
| 使用示例 | [usage-examples.md](data-structures/references/usage-examples.md) | 七种真实使用形态的虚构示范 |
| 记录模板 | assets/templates 下的四份模板 | 学习画像、练习计划、复盘与跨会话交接 |
| 验收 | [acceptance-scenarios.md](data-structures/references/acceptance-scenarios.md) | 二十四个行为场景和包装检查要求 |

## 可以这样开始

> 我使用 Java，只学过数组和哈希表。今天有三十分钟，请根据这些信息安排练习，不输出代码。

> 只给我一层提示，先不要透露解题结构。

> 我看题解后才做出这道题，帮我复盘理解缺口，再推荐一个合适的变式。

> 我只想用 SQL 练分组和窗口概念，请筛选可用题目，不输出查询语句。

## 维护与发布

优先修改技能入口和 references 中的对应规则，平台接入变动只修改对应说明。重新发布时，将核心教学参考、使用示例和记录模板展开到单文件版，并将整个 data-structures 目录打包为 ZIP；ZIP 不包含发布目录本身。

发布前检查 frontmatter、UI 配置、本地链接、ZIP 内容和单文件版一致性。真实学习记录应另存于用户指定位置，不能填写到公共模板后重新分发。

兼容性说明以 2026-10-28 核验的官方文档为依据。文档和包装检查不等于在八个平台逐一运行；实际模型效果按验收场景记录，不宣称未经执行的测试通过。

## 反馈与贡献

欢迎通过 Issues 反馈缺失主题、说明错误或平台接入变化；提交修改时附上具体使用情境、预期行为和观察结果。涉及平台能力的变化请提供官方来源，并保留“不输出代码、核验题目信息、不编造 memory”的核心约束。

反馈中不要包含账户凭据或未经授权分享的个人学习记录。仓库中的模板和示例都是公共资料，不代表任何人的真实 memory。

## 许可证

本仓库暂未指定开源许可证。
