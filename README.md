# Writecraft

**Think clearly. Structure logically. Write precisely.**

Writecraft 是一个内容构建与专业写作 Skill，涵盖从材料整理、结构组织到文本编辑的工作。它根据读者和用途决定写什么、怎样展开，根据用户要求决定修改幅度，将主题、零散材料或已有文稿处理成可用的内容。

适用于中文、英文和双语内容，包括技术方案、调研报告、研究摘要、工作汇报、说明文档、观点文章、邮件和日常消息。

## 能做什么

| 任务 | 处理方式 | 交付 |
| --- | --- | --- |
| 从主题或零散材料写作 | 明确要回答的问题，整理主张与依据，识别影响判断的材料缺口 | 提纲或完整正文 |
| 梳理思路、重组文稿 | 按理解和论证需要调整顺序，补齐解释环节，合并重复内容 | 结构方案或重组后的文稿 |
| 校对、润色、去 AI 味或改写 | 按要求修正错误、调整措辞和衔接，处理空话与语体失配 | 可直接使用的文本 |
| 翻译或总结 | 保留术语、归因、语气和决定结论的条件 | 译文或摘要 |
| 审查文稿 | 定位事实、论证、结构和表达问题，说明原因与修复建议 | 审查意见 |

## 如何处理内容

- **修改幅度随任务确定。** 语言润色和翻译保留作者立场与结论力度；要求实质性纠错或论证调整时，再依据材料修改判断。已有内容准确自然时，可以保留原样。
- **表达随读者和用途变化。** 技术报告讲清依据与实现细节，沟通文本交代事项与所需回应，个人表达保留语气、节奏和有作用的修辞。
- **事实和来源保持清楚。** 新写内容使主张与证据相符；编辑时保留数字、术语、归属和必要条件。来源暂时无法核实，不把引述改成无来源的断言。
- **说明文字按实际作用取舍。** 结合当前任务判断前提、风险或限制会影响哪项理解、决策或操作，将必要说明放在相关内容附近。省去重复提醒、泛泛免责声明和自我评价。

全局 Custom instructions 规定日常交互的基本偏好；Writecraft 在具体写作任务中落实材料处理、修改幅度、文体选择和交付检查。具体规则见 [SKILL.md](skills/writecraft/SKILL.md)。

## 在 Codex 中使用

在 Codex 对话中发送下面这句话。

```text
$skill-installer 从 https://github.com/Zong-Liang/writecraft/tree/main/skills/writecraft 安装 Writecraft
```

安装完成后，直接描述写作需求。如果 Skill 列表没有显示 Writecraft，可重启 Codex。

已下载仓库时，也可以将整个 `skills/writecraft/` 目录复制到 `~/.agents/skills/`。项目内共享时，复制到项目的 `.agents/skills/`。已安装过 Writecraft 时，在原安装目录更新即可。[Codex Skill 文档](https://learn.chatgpt.com/docs/build-skills) · [Agent Skills 格式规范](https://agentskills.io/specification)

## 在 Claude Code 中使用

从本地仓库安装插件，把示例路径替换为实际目录。

```text
/plugin marketplace add /path/to/writecraft
/plugin install writecraft@writecraft
```

也可将 `skills/writecraft/` 复制到 `~/.claude/skills/` 作为独立技能使用。

## 使用示例

在对话中直接描述你想完成的事，有材料就一起提供。可以说明读者、用途，以及希望获得正文、提纲还是审查意见；已有文稿时，说明需要润色还是调整论证。

- 我想给工程经理写一份 E2E 自动化测试试点方案，附件是团队现状和约束。
- 把这份订单事件投递材料写成两版说明，一版供初学者学习，一版供值班工程师在恢复现场查用。
- 帮我把这份会议记录整理成一封发给项目组的简短邮件。
- 这段英文摘要读起来不太自然，帮我润色一下。
- 只润色这段观点的措辞，保留我的立场和判断力度，直接给正文。
- 检查这份报告的证据能否支持结论，指出具体位置、原因和修改建议。

Skill 的入口是 [SKILL.md](skills/writecraft/SKILL.md)。[内容构建与结构设计](skills/writecraft/references/content-development.md)和[专业编辑与双语表达](skills/writecraft/references/editing.md)按任务需要读取。安装无需额外脚本或依赖。

维护时可使用仓库中的[行为验证案例与判据](evals/README.md)检查修改效果。

## 来源与许可

项目采用 [MIT 许可证](LICENSE)。
