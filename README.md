# Writecraft

**Think clearly. Structure logically. Write precisely.**

Writecraft 是一个内容构建与专业写作 Skill。它从读者需要解决的问题出发，整理材料、判断证据能支持什么、组织论述并完成写作。已有文稿时，它按任务范围做结构重组、校对、润色、改写、翻译、总结或审查，保留原意、术语和结论的适用条件。

适用于中文、英文和双语内容，包括技术方案、调研报告、研究摘要、工作汇报、博客和邮件。

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

在对话中直接描述你想完成的事，有材料就一起提供。Writecraft 会结合请求和材料判断交付形式、结构和修改幅度。

- 我想给工程经理写一份 E2E 自动化测试试点方案，附件是团队现状和约束。
- 帮我把这份会议记录整理成一封发给项目组的邮件。
- 这段英文摘要读起来不太自然，帮我润色一下。

Skill 的入口是 [SKILL.md](skills/writecraft/SKILL.md)。[内容构建与结构设计](skills/writecraft/references/content-development.md)和[专业编辑与双语表达](skills/writecraft/references/editing.md)按任务需要读取。安装无需额外脚本或依赖。

## 许可

采用 [MIT 许可证](LICENSE)。
