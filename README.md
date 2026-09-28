# HF Paper Skills

Personal paper-writing skills for optimization, machine learning, and theoretical research.

面向优化、机器学习与理论研究论文的自用写作 skills。

本项目在 Codex 的帮助下创建与维护。  
This project is created and maintained with assistance from Codex.

[中文](#中文) · [English](#english)

## 中文

### 这是什么？

这是我在自己的论文修改过程中整理的两个 Codex skills：`hf-rewrite` 用于写作和润色，`hf-restruct` 用于论文整体结构调整。它们主要关注**优化、机器学习及相关理论论文**，尤其是包含数学定义、定理、证明、算法、伪代码和实验分析的稿件。

它们以已经确定的科学内容为基础，帮助改善表达和组织，不负责补做研究、编造结果或创造新的贡献。

> **自用说明：** 这些 skills 首先服务于我自己的研究和写作习惯，其中保留了个人偏好，以及从具体论文修改中总结的规则和例子。我将它们公开供参考，但无法保证其他人的使用体验、输出质量，或它们对其他学科、模型和工作流程的适用性。请根据自己的论文、投稿要求和写作偏好调整，并人工核对所有修改。

### 两个 skill 的区别

| Skill | 主要用途 | 范围 |
| --- | --- | --- |
| [`hf-rewrite`](hf-rewrite/SKILL.md) | 补写或润色已有科学内容，统一术语，改善段落逻辑、公式说明和伪代码表达 | 保持已有或作者提供的论文结构，不自动启动全文重构 |
| [`hf-restruct`](hf-restruct/SKILL.md) | 梳理论文主线，诊断结构问题，提出章节安排和内容迁移方案 | 调整整体组织；只有明确授权实施时才应用重构，不改变科学结论 |

两者可以单独使用。需要同时调整结构与表达时，可以先用 `hf-restruct` 确定组织方式，再用 `hf-rewrite` 润色。仅调用 `hf-rewrite` 不会自动调用 `hf-restruct`。

### 安装与使用

下载或克隆本仓库，将需要使用的 **skill 文件夹整体复制**到以下一个位置，保留其内部目录结构：

- 个人使用：`~/.agents/skills/`
- 项目内使用：`<project>/.agents/skills/`

例如，安装后应能找到 `~/.agents/skills/hf-rewrite/SKILL.md` 和 `~/.agents/skills/hf-restruct/SKILL.md`。如果已有同名 skill，先备份或比较内容再替换。Codex 未显示新安装的 skill 时，可尝试重启。安装位置与发现机制见 [OpenAI 官方文档](https://learn.chatgpt.com/docs/build-skills)。

这两个 skill 的配置均关闭了隐式调用。使用时请明确指定 skill，并提供稿件、需要处理的范围和约束。例如：

```text
使用 $hf-rewrite 润色这篇论文的 Method 部分。
保留现有章节结构、数学含义和算法行为，重点改善术语一致性与解释顺序。
```

```text
使用 $hf-restruct 检查这篇论文的整体组织。
先给出主要结构问题、建议大纲和内容迁移表，暂不修改源文件。
```

```text
使用 $hf-restruct，按刚才确定的方案实施重构。
保留所有科学结论，并报告内容移动、移除及其保存位置。
```

### 使用边界

- 输入应包含足够的已确定科学内容；缺失的假设、证明关系或实验结论应被指出，而不是靠措辞补齐。
- 这些 skills 中的数学和实验示例来自特定研究语境，不应直接套用到另一篇论文。
- 写作偏好不是所有期刊、会议或学科的通用标准，应以作者约束和投稿要求为准。
- 它们是编辑辅助工具，不能替代作者对数学正确性、引文支持和实验解释的核查。

## English

### What is this?

This repository contains two Codex skills developed through revisions of my own papers: `hf-rewrite` for drafting and polishing prose, and `hf-restruct` for reorganizing a manuscript. They focus on **optimization, machine learning, and related theoretical research**, particularly papers involving mathematical definitions, theorems, proofs, algorithms, pseudocode, and experimental analysis.

They work from established scientific content to improve expression and organization. They are not intended to conduct missing research, invent results, or create new contributions.

> **Personal-use notice:** These skills were built primarily for my own research and writing workflow. They retain personal preferences, as well as rules and examples derived from specific manuscript revisions. I am sharing them for reference, but I cannot guarantee other users' experience, output quality, or suitability for other disciplines, models, or workflows. Adapt them to your manuscript, venue requirements, and writing preferences, and review all changes yourself.

### The two skills

| Skill | Purpose | Scope |
| --- | --- | --- |
| [`hf-rewrite`](hf-rewrite/SKILL.md) | Draft or polish prose from established content; improve terminology, paragraph logic, equation explanations, and pseudocode presentation | Preserve the existing or author-supplied outline; do not automatically initiate whole-paper restructuring |
| [`hf-restruct`](hf-restruct/SKILL.md) | Identify the paper's central argument, diagnose structural problems, and propose an outline and content migrations | Reorganize the manuscript; apply changes only when implementation is authorized, while preserving scientific conclusions |

Use either skill independently. When both structure and prose need work, you can use `hf-restruct` first and `hf-rewrite` afterward. Invoking `hf-rewrite` alone does not activate `hf-restruct`.

### Installation and usage

Download or clone this repository, then copy each desired **complete skill folder**, including its supporting files, into either location:

- Personal scope: `~/.agents/skills/`
- Project scope: `<project>/.agents/skills/`

For example, the installed entry points should be `~/.agents/skills/hf-rewrite/SKILL.md` and `~/.agents/skills/hf-restruct/SKILL.md`. Back up or compare any existing same-named skills before replacing them. Restart Codex if the new skills do not appear. See the [official OpenAI documentation](https://learn.chatgpt.com/docs/build-skills) for local skill discovery.

Both skills disable implicit invocation in their configuration. Invoke the desired skill explicitly and provide your manuscript, editing scope, and constraints:

```text
Use $hf-rewrite to polish the Method section of this paper.
Preserve its structure, mathematical meaning, and algorithm behavior.
Focus on consistent terminology and the order of explanation.
```

```text
Use $hf-restruct to review this manuscript's organization.
First provide the main structural problems, a recommended outline,
and a content migration table. Do not edit the source files yet.
```

```text
Use $hf-restruct to implement the restructuring plan we just agreed on.
Preserve all scientific conclusions and report content moves,
removals, and where the removed material is preserved.
```

### Boundaries

- Supply enough established scientific content to support the requested edit. Missing assumptions, proof connections, or empirical conclusions should be flagged rather than filled with plausible prose.
- Mathematical and experimental examples come from particular research contexts and should not be copied into unrelated papers.
- Editorial preferences are not universal standards across venues or disciplines. Author constraints and submission requirements take precedence.
- These are editorial aids. They do not replace the author's verification of mathematical correctness, citation support, or experimental interpretation.

## Repository structure / 仓库结构

```text
hf-paper-skills/
├── README.md
├── hf-rewrite/
│   ├── SKILL.md
│   ├── agents/openai.yaml
│   └── references/
│       ├── algorithm-presentation.md
│       ├── edit-patterns.md
│       ├── revision-criteria.md
│       └── section-guides.md
└── hf-restruct/
    ├── SKILL.md
    └── agents/openai.yaml
```
