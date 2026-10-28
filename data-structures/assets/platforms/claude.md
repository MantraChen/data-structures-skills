# Claude 适配

核验日期：2026-10-28。教学规则来自本包，不随 Claude 的具体型号变化。

## 原生 Skill

Claude 官方说明支持将包含技能目录的 ZIP 上传为自定义 Skill。使用发布的 data-structures.zip；其顶层是 data-structures 文件夹，文件夹内含 SKILL.md 和配套资料。当前文档中的入口为 Customize → Skills → 创建技能 → 上传技能。功能前提以该账户界面为准。[官方使用说明](https://support.claude.com/en/articles/12512180-use-skills-in-claude)

不要只上传 SKILL.md 后就假定 references 全部可读。目录和相对路径需要完整保留。[官方打包说明](https://support.claude.com/en/articles/12512198-how-to-create-custom-skills)

## 普通聊天

若当前入口不使用原生 Skills，复制[通用启动指令](../portable-core.md)，再提供实际学习情况；需要完整配套内容时使用发布的单文件版。

## 启动示例

> 使用数据结构学习技能。我熟悉 C++，刚学完链表，只讲原理，不写代码。先解释为什么删除操作的成本取决于已知信息，再根据我提供的记录推荐练习。

## 接入后检查

确认能读取当前任务需要的参考资料，并用[验收场景](../../references/acceptance-scenarios.md)检查无代码输出、提示深度和无 memory 时的表现。安装成功不等于这些行为已经通过测试。
