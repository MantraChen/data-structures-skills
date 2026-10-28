# Qwen 适配

核验日期：2026-10-28。

## 普通聊天

将[通用启动指令](../portable-core.md)作为本次对话规则，再提供学习记录。需要完整资料时使用单文件版，按界面允许的形式输入。

## Model Studio 或自有宿主

Model Studio 官方对话文档说明 system 消息可定义角色、任务和约束，也列出部分模型对该角色支持不同。因此先核对所选模型和宿主，不能因为属于 Qwen 家族就假定同一套消息设置处处有效。[官方消息协议](https://www.alibabacloud.com/help/en/model-studio/qwen-api-via-openai-chat-completions)

本包不固定模型型号、不修改模型配置。纯聊天场景通过用户提供的文字规则使用，原生 Skills 是否可用由具体宿主决定。

## 启动示例

> 我使用 TypeScript，请按无代码教学规则说明类型信息与运行时数据结构的区别，再讲数组与映射在查找需求上的选择依据。

## 接入后检查

观察模型是否把 TypeScript 类型标注误当成复杂度变化，以及是否凭空猜测已做题。使用[验收场景](../../references/acceptance-scenarios.md)记录实际结果。
