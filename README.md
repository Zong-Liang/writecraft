# Writecraft

**Think clearly. Structure logically. Write precisely.**

Writecraft 是一个内容构建与专业写作 Skill，涵盖从材料整理、结构组织到文本编辑的工作。它结合作者意图、读者的使用方式、材料和交付要求选择结构与表达，根据授权决定修改幅度，将主题、零散材料或已有文稿处理成可用的内容。

适用于中文、英文和双语内容，包括技术方案、需求与接口文档、操作指南、调研报告、论文与研究摘要、工作汇报、会议纪要、观点文章、个人表达、邮件和日常消息。

## 能做什么

| 任务 | 处理方式 | 交付 |
| --- | --- | --- |
| 从主题或零散材料写作 | 确定用途与必需覆盖，组织材料及其关系，识别影响交付的缺口 | 提纲或完整正文 |
| 梳理思路、重组文稿 | 按通读、查阅或执行等需要调整顺序与详略，补齐有依据的解释 | 结构方案或重组后的文稿 |
| 校对、润色、去 AI 味或改写 | 按要求修正错误、调整措辞和衔接，处理空话与语体失配 | 可直接使用的文本 |
| 翻译或总结 | 保留术语、归因、语气和决定结论的条件 | 译文或摘要 |
| 审查文稿 | 定位事实、论证、结构和表达问题，说明原因与修复建议 | 审查意见 |

## 如何处理内容

- **按任务选择标准。** 先辨认本次是起草、润色、翻译还是审查，再结合用途、阅读方式、材料状态与适用要求处理。信息充分时直接交付，无需用户填写文种或风格问卷。
- **允许一份文档承担多个任务。** 技术方案中的评审摘要、接口定义和迁移步骤可以采用不同结构，同时保持事实、术语和状态一致。文档不必收束成一个论点。
- **兼顾完整性与使用方式。** 连续论述讲清关系，参考资料便于定位和独立查阅，操作材料保留前提与分支，研究内容保留影响判断的方法、结果和限制。教学、查阅或执行所需的重复可以保留。
- **修改幅度随授权确定。** 语言润色、去 AI 味和翻译保留作者立场与结论力度；重组或改写也不意味着可以替换作者判断。允许实质性纠错时，依据材料修改。准确自然的内容可以保留原样。
- **事实、来源与冲突保持清楚。** 区分事实、来源自述、推断和建议，不补造实验、引文或经历。来源暂时无法核实，不把引述改成无来源断言；冲突无法消解时具体指出。
- **表达服务具体场景。** 根据用途、双方关系和媒介选择语气，保留有作用的细节、声音和节奏。说明文字按实际作用取舍，省去空泛提醒与自我评价。

只有缺口实质影响交付的正确性、完整性、可执行性、适用要求或作者意图，且无法核实或合理推断时，才提出具体问题；其余部分先完成。

Writecraft 可配合全局 Custom instructions 使用，在具体写作任务中落实材料处理、修改幅度、结构选择和交付检查。具体规则见 [SKILL.md](skills/writecraft/SKILL.md)。

## 在 Codex 中使用

在 Codex 对话中发送下面这句话。

```text
$skill-installer 从 https://github.com/Zong-Liang/writecraft/tree/main/skills/writecraft 安装 Writecraft
```

安装完成后，直接描述写作需求。如果 Skill 列表没有显示 Writecraft，可重启 Codex。

已下载仓库时，也可以将整个 `skills/writecraft/` 目录复制到 `~/.agents/skills/`。项目内共享时，复制到项目的 `.agents/skills/`。已安装过 Writecraft 时，在原安装目录更新即可。[Codex Skill 文档](https://learn.chatgpt.com/docs/build-skills) · [Agent Skills 格式规范](https://agentskills.io/specification)

### 作为 Codex 插件安装

把仓库添加为 marketplace 后安装，之后可直接拉取更新：

```bash
codex plugin marketplace add Zong-Liang/writecraft
codex plugin add writecraft@writecraft
```

更新时先刷新 marketplace，再重新安装新版本：

```bash
codex plugin marketplace upgrade writecraft
codex plugin add writecraft@writecraft
```

## 在 Claude Code 中使用

把仓库添加为 marketplace 后安装：

```bash
claude plugin marketplace add Zong-Liang/writecraft
claude plugin install writecraft@writecraft
```

更新后重启 Claude Code 生效：

```bash
claude plugin marketplace update writecraft
claude plugin update writecraft@writecraft
```

会话内也可使用对应的 `/plugin` 命令。开发时可把 `Zong-Liang/writecraft` 换成本地仓库路径。也可将 `skills/writecraft/` 复制到 `~/.claude/skills/` 作为独立技能使用，但这种方式需要手动更新。

插件以 `version` 判断是否有新版本。发布时同步更新 `.claude-plugin/plugin.json`、`.codex-plugin/plugin.json` 和 `skills/writecraft/version.json` 中的版本号。

## 使用示例

在对话中直接描述你想完成的事，有材料就一起提供。可以说明读者、用途，以及希望获得正文、提纲还是审查意见；已有文稿时，说明需要润色还是调整论证。

- 我想给工程经理写一份 E2E 自动化测试试点方案，附件是团队现状和约束。
- 把这份订单事件投递材料写成两版说明，一版供初学者学习，一版供值班工程师在恢复现场查用。
- 帮我把这份会议记录整理成一封发给项目组的简短邮件。
- 这段英文摘要读起来不太自然，帮我润色一下。
- 只润色这段观点的措辞，保留我的立场和判断力度，直接给正文。
- 把这份会议纪要整理成摘要，保留已作出的决定、分歧、负责人和待办事项。
- 用这份材料写两个可以独立查阅的操作条目，每个条目保留各自的执行前提。
- 根据实验材料整理论文结果部分，保留负面结果，检查摘要与正文的口径是否一致。
- 检查这份报告的证据能否支持结论，指出具体位置、原因和修改建议。

## 文件与维护

安装所需内容都在 `skills/writecraft/` 中，无需额外脚本或依赖。参考资料按任务需要读取，行为验证材料供维护时使用。

| 文件 | 用途 |
| --- | --- |
| [SKILL.md](skills/writecraft/SKILL.md) | 技能入口：任务判断、修改授权、事实保真、组织表达和按用途复查 |
| [内容构建与结构设计](skills/writecraft/references/content-development.md) | 处理覆盖与取舍、解释与论证、混合用途、专业与学术内容、阅读路径和标题 |
| [专业编辑与双语表达](skills/writecraft/references/editing.md) | 按授权诊断问题，调整重心、细节与节奏，处理去 AI 味、翻译、压缩和保真 |
| [行为验证判据](evals/README.md)与[验证请求](evals/prompts.md) | 检查保真与实际可用性，以及用途、阅读方式和授权变化时的处理差异 |

修改 Skill 后，向执行者提供请求与技能，保存原始输出后再对照判据评审。当前包含 A–T 共 20 个案例，覆盖基础保真、用途对照、混合文档、材料冲突、双语、新文种迁移与证据充分时的表态。

## 许可

项目采用 [MIT 许可证](LICENSE)。
