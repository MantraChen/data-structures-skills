# AIGC 平台支持与接入方式

文档核验日期：2026-10-28（Asia/Shanghai）。本包面向 Claude、ChatGPT、Grok、Gemini、DeepSeek、Qwen、GLM、Kimi 提供教学指令和接入说明。下表表示交付的适配方式，不代表八个平台都已完成账户内安装或模型实测。

## 支持矩阵

| AIGC | 本包提供的接入方式 | 平台说明 |
| --- | --- | --- |
| Claude | 原生 Skill ZIP；普通聊天可用通用文本 | [Claude](../assets/platforms/claude.md) |
| ChatGPT | 当前界面支持时使用 Skills；也可用项目资料或普通聊天文本 | [ChatGPT](../assets/platforms/chatgpt.md) |
| Grok | 普通聊天粘贴指令，按界面能力附加资料 | [Grok](../assets/platforms/grok.md) |
| Gemini | Gems 指令和知识资料；普通聊天文本 | [Gemini](../assets/platforms/gemini.md) |
| DeepSeek | 普通聊天文本；API 集成时使用其支持的指令消息 | [DeepSeek](../assets/platforms/deepseek.md) |
| Qwen | 普通聊天文本；Model Studio 中按具体模型的指令支持接入 | [Qwen](../assets/platforms/qwen.md) |
| GLM | 普通聊天文本；对话 API 的指令消息 | [GLM](../assets/platforms/glm.md) |
| Kimi | 普通聊天文本；对话 API 按官方消息协议接入 | [Kimi](../assets/platforms/kimi.md) |

原生 Skill 由宿主读取 SKILL.md 和相关文件；普通聊天中的 Markdown 是用户提供的教学指令，不会自动获得文件系统、联网或长期记忆。没有确认导入流程的平台使用通用文本路径，不宣称它支持原生 ZIP 安装，也不宣称它永远不支持 Skills。

## 选择合适的交付形式

- **标准技能目录或 ZIP**：保留 data-structures 目录及其内部相对路径。agents/openai.yaml 是可选的 OpenAI UI 元数据，其他宿主不必将它当成运行依赖。
- **通用启动指令**：[portable-core.md](../assets/portable-core.md) 可以直接复制到普通对话，包含关键边界和工作方式。
- **完整单文件版**：发布目录中的 data-structures-portable.md 已合并教学参考、语言背景、记录模板和例子，不需要宿主读取引用文件。资料较长时优先作为可访问附件或知识资料提供；不能附加时，按当前主题提供相关内容，不静默截掉输出边界。
- **平台说明**：八份说明只负责接入。通用教学规则不因品牌改变，也不依赖某个固定型号或付费套餐。

## 能力适配

只根据当前会话可见的工具和成功结果判断能力，不要求模型猜测自己的账号权限。联网、文件读取、图形和 memory 四种能力分别处理；拥有其中一种不代表同时拥有其余能力。

无联网时保留概念学习、用户题面分析和明确标注的待核验候选。无长期记忆时使用交接摘要；切换平台不会自动同步个人记录。无文件读取时使用已展开的文本，不声称已经读取附件中未能访问的段落。

## 官方依据

以下来源只支持接入能力说明，不为本技能的教学质量或所有模型的一致行为背书。具体账户界面与可用功能仍需实际确认。

- Claude：[使用 Skills](https://support.claude.com/en/articles/12512180-use-skills-in-claude)、[创建和打包自定义 Skills](https://support.claude.com/en/articles/12512198-how-to-create-custom-skills)。
- ChatGPT：[Skills 与 Plugins](https://learn.chatgpt.com/docs/skills-and-plugins)、[项目、文件与对话使用方式](https://learn.chatgpt.com/docs/use-chatgpt)。
- Grok：[聊天与文件功能概览](https://docs.x.ai/grok/overview)。
- Gemini：[创建 Gems、编写指令和添加资料](https://support.google.com/gemini/answer/15235603?hl=en)。
- DeepSeek：[Chat Completions 消息协议](https://api-docs.deepseek.com/api/create-chat-completion/)。
- Qwen：[Model Studio 对话与 System Message](https://www.alibabacloud.com/help/en/model-studio/qwen-api-via-openai-chat-completions)。
- GLM：[Z.AI 对话消息协议](https://docs.z.ai/api-reference/llm/chat-completion)。
- Kimi：[Kimi 对话消息协议](https://platform.kimi.ai/docs/api/chat)。

## 验收范围

本地可检查目录、格式、引用、语言覆盖和发布产物一致性。实际平台行为需在目标会话运行[验收场景](acceptance-scenarios.md)后记录；没有运行就保留“未实测”，不使用“全平台测试通过”等说法。
