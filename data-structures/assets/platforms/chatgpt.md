# ChatGPT 适配

核验日期：2026-10-28。ChatGPT 与 Codex 的界面入口和技能引用方式应分别按当前宿主处理。

## 支持 Skills 的界面

官方文档说明 ChatGPT 和 Codex 可以使用包含指令与资源的 Skills。将完整技能通过当前支持的入口添加并启用；ChatGPT 可在选择器中使用 @ 引用，Codex 使用 $ 引用。技能尚未添加时，单独输入名称不能使本地文件自动出现在普通聊天中。[官方 Skills 文档](https://learn.chatgpt.com/docs/skills-and-plugins)

本包保留 agents/openai.yaml 作为 UI 元数据，不自动修改全局技能目录。

## 普通聊天或项目

复制[通用启动指令](../portable-core.md)，或提供完整单文件版并明确要求按其中教学规则工作。持续学习可将规则、学习摘要和相关文件放在可用项目中；不要假设模型已经读取另一项目或其他 AIGC 的记录。[官方项目与文件说明](https://learn.chatgpt.com/docs/use-chatgpt)

## 启动示例

> 按附件中的数据结构学习规则帮助我，不输出代码。我主要用 Java，今天想理解哈希计数。请先使用本对话实际可读的学习记录，再推荐适合的 LeetCode 和 Codeforces 题目。

## 接入后检查

检查当前会话是否实际具有联网、文件和记忆能力。若没有，不声称题目已核验或进度已保存。用[验收场景](../../references/acceptance-scenarios.md)观察真实回答。
