# GitHub Commit Complete Skill

**GitHub 提交完善助手（双语代码审查与文档生成）**

---

## 📌 Overview | 项目简介

**English**

`github-commit-complete` is an AI-powered skill designed to prepare your codebase for a high-quality GitHub commit. It performs structured code inspection, adds bilingual (English & Chinese) comments, and generates essential repository documentation such as `README.md` and `checklist.md`.

This skill focuses on **safety and non-intrusive enhancement** — it does **not modify any existing code logic**, only adds comments and documentation.

---

**中文**

`github-commit-complete` 是一个用于提升代码仓库质量的 AI Skill，帮助开发者在提交 GitHub 之前完成代码检查、注释补充和文档生成。

该技能专注于**安全增强**：
👉 **不会修改任何代码逻辑**，只会补充注释和生成文档（README / checklist）

---

## 🌟 Key Features | 核心能力

### 🔍 Code Inspection | 代码检查

* Analyze code quality, readability, and maintainability
* 检查代码质量、可读性和可维护性
* Detect potential risks (e.g., hardcoded secrets)
* 检测潜在风险（如硬编码密钥）

---

### 💬 Bilingual Comments | 双语注释增强

* Automatically adds **English + Chinese comments**
* 自动添加**中英双语注释**
* Focus on:

  * Complex logic（复杂逻辑）
  * Core functions（核心函数）
  * Unclear code（不清晰代码）

⚠️ **Will NOT modify code logic**
⚠️ **不会修改代码逻辑**

---

### 📄 README Generation | 自动生成 README

* Generates a structured, bilingual `README.md`
* 自动生成结构化的中英双语 README

Includes:

* Project purpose（项目目的）
* File structure（项目结构）
* Core logic（核心逻辑）
* Usage instructions（使用方式）

---

### ✅ Checklist Generation | 检查清单生成

Generates `checklist.md` with:

* Code issues（代码问题）
* GitHub readiness issues（仓库规范问题）
* Actionable suggestions（可执行建议）

---

### 📊 Repo Scoring | 仓库评分

Provides a **GitHub readiness score (0–100)** based on:

* Documentation completeness
* Code quality
* Structure
* Security

提供仓库质量评分，便于快速评估项目成熟度。

---

## 🔒 Safety Policy | 安全策略（重要）

This skill follows strict safety rules:

* ❌ Does NOT modify existing code logic

* ❌ 不会修改任何已有代码逻辑

* ✅ Only adds comments and documentation

* ✅ 仅补充注释和文档

* ❌ Does NOT delete or refactor code

* ❌ 不会删除或重构代码

* 💡 Suggestions are provided in `checklist.md`

* 💡 所有改进建议仅在 checklist 中提出

---

## 🚀 Installation | 安装方式

### For Trae / AI IDE

```bash
mkdir -p .trae/skills/github-commit-complete
cp -r * .trae/skills/github-commit-complete/
```

确保以下文件被正确复制 (Ensure the following files are copied):

```text
SKILL.md (Entry point / 入口文件)
skill.yaml
prompt.md
input_schema.json
output_schema.json
rules.md
templates/
examples/
```

### Generic Usage (Other IDEs / Agents) | 通用使用方式（其他工具）

Copy this skill directory into your AI tool's skill/plugin folder.

将本技能目录复制到你的 AI 工具的 skill / plugin 目录中。

Minimum required files:

至少需要以下文件：

- SKILL.md (entry point)
- prompt.md
- input_schema.json
- output_schema.json
- rules.md
- templates/

The exact path depends on your tool (e.g., Claude Desktop, Cursor, custom agents).
具体路径取决于你的工具（如 Claude Desktop、Cursor 或自定义 Agent）。

### For Custom Agent Integration | 自定义 Agent 接入

This skill can be loaded as a modular capability:

本技能可作为模块化能力接入：

- Use `skill.yaml` for structured definition
- 使用 skill.yaml 作为结构化定义

- Use `prompt.md` as execution logic
- 使用 prompt.md 作为执行逻辑

- Use schemas for validation and orchestration
- 使用 schema 进行参数校验与编排


---

## 💡 Usage | 使用方式

### Example Prompts | 示例调用

#### 1️⃣ Basic Usage | 基础用法

```text
Use the github-commit-complete skill to analyze my project at /path/to/project
```

```text
使用 github-commit-complete 技能分析我的项目路径 /path/to/project
```

---

#### 2️⃣ Current Workspace | 当前项目

```text
Prepare my current workspace for a GitHub commit using github-commit-complete
```

```text
使用 github-commit-complete 为当前项目准备 GitHub 提交
```

---

#### 3️⃣ Structured Input（推荐）

```json
{
  "project_path": "/your/project",
  "mode": "dry_run",
  "language": "bilingual"
}
```

---

## ⚙️ Modes | 执行模式

| Mode / 模式 | Description / 说明 |
| --------------- | ---------------------------------- |
| `dry_run`       | Only analyze and suggest (default) / 仅分析，不修改文件（默认） |
| `apply_changes` | Apply comments and generate files / 写入注释并生成文档  |

---

## 📁 Output | 输出内容

After execution, the skill will produce:

执行后将生成：

* `README.md`（自动生成或优化）
* `checklist.md`（问题与建议）
* Code comments（代码注释增强）

And structured output:

```json
{
  "repo_score": 78,
  "issues_found": [],
  "suggestions": [],
  "generated_files": []
}
```

---

## 📦 Supported Languages | 支持语言

* Python
* JavaScript / TypeScript
* General support for other languages（其他语言基础支持）

---

## ⚠️ Limitations | 限制说明

* Not ideal for very large monorepos (>200 files)

* 不适用于超大规模仓库

* May not fully understand highly complex architectures

* 对复杂架构理解有限

* Comment quality depends on code clarity

* 注释质量依赖代码本身质量

---

## 🧠 Design Philosophy | 设计理念

> **Enhance, not modify.**
> **增强，而不是改变。**

This skill is designed to:

* Improve repository readability
* 提升仓库可读性
* Make projects GitHub-ready
* 让项目更符合开源规范
* Support global collaboration (EN + ZH)
* 支持中英文开发协作

---

## 📄 License | 许可证

MIT License (recommended)

---

## 🤝 Contributing | 贡献

Feel free to submit issues or PRs to improve:

* Rules (`rules.md`)
* Templates (`templates/`)
* Prompt strategies (`prompt.md`)

欢迎提交 Issue 或 PR 优化规则、模板和策略。

---

## ⭐ Final Note

This is not just a “README generator”.

👉 It is a **safe, structured, bilingual GitHub repo optimization tool**.

这不仅仅是一个 README 生成工具，而是一个：

👉 **安全、结构化、双语的 GitHub 仓库优化工具**

