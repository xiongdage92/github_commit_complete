## Priority Notice / 优先级说明

- `prompt.md` contains the authoritative execution logic.
- `prompt.md` 是唯一的执行逻辑来源

- This file (SKILL.md) is only an entry point and dispatcher.
- 本文件仅作为入口和调度说明

- In case of conflict, ALWAYS follow `prompt.md`.
- 如有冲突，始终以 `prompt.md` 为准

---
name: "github-commit-complete"
description: "Checks project code for GitHub commit readiness, adds EN/ZH comments, generates bilingual README.md and checklist.md. Invoke when preparing code for GitHub."
---

# GitHub Commit Complete Skill (GitHub 提交完善助手)

This skill is powered by a structured prompt system. 
本技能由结构化的提示词系统驱动。

When the user invokes this skill, you **MUST** read the following files in the skill directory to understand your instructions and execution logic:
当用户调用此技能时，你**必须**读取技能目录下的以下文件，以理解你的指令和执行逻辑：

1. `prompt.md` - Your core execution steps, persona, and strict safety rules. (你的核心执行步骤、角色设定和严格的安全规则。)
2. `rules.md` - The specific coding and GitHub rules for code inspection. (用于代码检查的特定编码和 GitHub 规范。)
3. `templates/` - Templates for generating `README.md` and `checklist.md`. (用于生成 `README.md` 和 `checklist.md` 的模板。)
4. `input_schema.json` & `output_schema.json` - Reference for input parameters and structured output format. (输入参数和结构化输出格式的参考。)

**Execution Directive / 执行指令**: 
Follow the 6 execution steps defined in `prompt.md` exactly. Always ensure your outputs and code comments are fully bilingual (English + Chinese).
严格遵循 `prompt.md` 中定义的 6 个执行步骤。始终确保你的输出和代码注释是完全中英双语的。

## Input Handling / 输入处理

- You MUST interpret user input according to `input_schema.json`
- 必须按照 input_schema.json 解析用户输入

- If required fields are missing (e.g., project_path), ask the user before proceeding
- 如果缺少必要字段（如 project_path），必须先询问用户

## Safety Summary / 安全摘要

- DO NOT modify code logic
- 严禁修改代码逻辑

- ONLY add comments and documentation
- 仅允许新增注释和文档

- All improvements must be suggested in checklist.md
- 所有改进建议必须写入 checklist.md