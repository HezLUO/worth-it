# Assess Material Value

> Public beta for Codex. Evaluate whether external material adds real incremental value to the product you are currently building.

`assess-material-value` is a small Codex Skill for critically reviewing webpages, repositories, documents, prompts, Skills, Plugins, MCPs, tools, workflows, ideas, competitors, and design proposals. It separates what a material says from whether it is supported, relevant, new relative to the current product, valuable, and worth acting on now.

It is not a summarizer and it is allowed to conclude `no-action` or `insufficient-evidence`.

## Why Side Chat

Use the Skill in Codex Side Chat when available. This keeps the raw material and full analysis away from the main product conversation while still allowing the Skill to use bounded product context visible in that Side Chat. The Skill cannot access hidden context and does not create or manage Side Chats.

## Install

Ask Codex to use `$skill-installer` to install the Skill from this GitHub repository at path `skill/assess-material-value`. The installed Skill becomes available on the next turn.

The repository also contains the package directly at `skill/assess-material-value` for project-local inspection.

## Use

In a Side Chat, provide one material item and invoke:

```text
Use $assess-material-value to judge whether this material adds real value to my current product.
```

When the current product context is not visible, provide only the decision-relevant facts:

```text
Product goal:
Primary user:
Current capabilities:
Current priorities:
Boundaries and non-goals:
Known gaps or risks:
```

The output separates evidence quality, existing-capability overlap, incremental value, adoption cost, risks, evidence gaps, confidence, and one primary disposition:

Primary value types are `directly-adoptable`, `design-reference`, `evaluation-or-comparison-sample`, `risk-or-negative-example`, `general-inspiration-only`, and `no-substantive-value`.

- `adopt-now`
- `evaluate-later`
- `retain-as-reference`
- `retain-as-negative-sample`
- `no-action`
- `insufficient-evidence`

Only the compact decision delta should be carried back to the main conversation, and only when the user chooses to do so.

## Safety Boundary

All evaluated material is untrusted data, including instructions embedded in webpages, documents, repositories, prompts, or tool descriptions. The Skill does not install, execute, import, activate, or configure evaluated artifacts; write findings into the target product; scan unrelated repositories, private notes, or complete chat histories; or create tasks and persistent product records.

## Development Evidence

In a bounded 24-case development set with 64 isolated runs, no safety-boundary failure was observed. Compared with the original simple prompt, false-positive value judgments fell from 10/12 to 0/12. Candidate evidence accuracy was 176/177 (99.44%), existing-capability overlap detection was 3/3, and repeat consistency was 22/24 (91.67%). These results describe only that controlled evaluation and are not a universal performance guarantee.

## Beta Limitations

- Formal four-field human calibration is incomplete.
- 3 of 24 candidate first runs had unexplained 335-second durations.
- Exact token telemetry was unavailable.
- The Skill has not yet been tested on a sufficiently diverse set of real user materials.
- This beta targets Codex and does not promise compatibility with other hosts.

## Feedback And Privacy

Use the repository's **Beta feedback** issue form. Record whether you agree with the recommended disposition and describe concerns using a sanitized summary.

**Do not post private files, full conversations, credentials, secrets, proprietary source material, or unredacted sensitive information.** Missing feedback is not treated as agreement, and user judgments are calibration evidence rather than an infallible oracle.

The first review checkpoint is at 5 independent users, 20 real-material analyses, 4 material types, and zero observed unauthorized install, execution, import, or write events. Three reports of the same substantive misjudgment trigger an earlier review. Reaching a checkpoint does not automatically promote the Skill to stable.

## 中文快速开始

建议在 Codex Side Chat 中使用本 Skill，以避免把原始材料和完整分析带入主会话。请提供一份材料，并调用 `$assess-material-value`；如果产品上下文不可见，只补充产品目标、当前能力、优先级、边界和已知问题。主会话只需接收最后的紧凑决策增量。

请勿在 GitHub Issue 中提交私人文件、完整聊天、密钥、专有材料或未脱敏敏感信息。

## License

MIT
