# Web Project Starter

An AI agent skill that turns a website or web application brief into an actionable `PROJECT-SPEC.md` before implementation.

**Skill name:** `project-starter`

## What it produces

The specification has three main sections:

1. **Foundations** — project context, technology stack, pages, interactions, integrations, and constraints.
2. **Design System** — typography (Heading, Body, and Mono), colors and themes, spacing, components, animations, and responsive rules.
3. **Development Plan** — unresolved decisions, implementation phases, dependencies, acceptance criteria, and verification records.

The agent distinguishes Confirmed, Proposed, Open, and Not applicable decisions. It preserves existing project choices and asks focused questions when missing information affects architecture or scope.

## Repository structure

```text
skills/
└── project-starter/
    ├── SKILL.md
    └── assets/
        └── PROJECT-SPEC.template.md
```

`SKILL.md` defines the workflow. The template defines the generated document's structure. No runtime dependencies are required.

## Installation

### Codex

Clone this repository, then copy `skills/project-starter` into your Codex skills directory, usually `~/.codex/skills/`. If you use a custom `CODEX_HOME`, use its `skills/` directory instead. Preserve any existing installation before replacing it.

### Claude Code

Clone this repository, then copy the complete `skills/project-starter` folder into `~/.claude/skills/` for use across projects. For a project-specific installation, copy it into `.claude/skills/` inside your target project instead. Preserve any existing installation before replacing it.

The resulting structure should contain `project-starter/SKILL.md` and `project-starter/assets/PROJECT-SPEC.template.md` inside the chosen skills directory.

In Claude Code, invoke the skill with your brief:

```text
/project-starter Create PROJECT-SPEC.md for a bilingual corporate website. Next.js and DatoCMS are confirmed. Propose the remaining choices and identify architectural questions before implementation.
```

See the [official Claude Code skills documentation](https://code.claude.com/docs/en/skills).

### Gemini CLI

Install the skill directly from this repository:

```bash
gemini skills install https://github.com/ugurakdemir/web-project-starter.git --path skills/project-starter
```

The default installation scope is your user account. Add `--scope workspace` to install it for the current project instead. Review and accept any installation prompts.

In an existing Gemini CLI session, run `/skills reload`, then `/skills list` to check that `project-starter` is available. Ask Gemini to use it:

```text
Use the project-starter skill to create PROJECT-SPEC.md for a bilingual corporate website. Next.js and DatoCMS are confirmed. Propose the remaining choices and identify architectural questions before implementation.
```

See the [official Gemini CLI skills documentation](https://geminicli.com/docs/cli/skills/).

Both tools support this skill's file structure. Runtime behavior in Claude Code and Gemini CLI has not yet been tested.

## Usage

In Codex, invoke the skill in a project with your brief (use the platform-specific invocation above for Claude Code or Gemini CLI):

> Use $project-starter to create PROJECT-SPEC.md for a bilingual corporate website. Required pages: home, about, products, product details, and contact. Next.js and DatoCMS are confirmed. Propose the remaining choices, explain the rationale, and identify architectural questions before implementation.

Provide whatever is available: audience, primary user task, brand guidelines, required pages, interactions, technology constraints, integrations, and reference material.

The skill writes `PROJECT-SPEC.md` at the project root unless you request another location. With no project brief, it produces a reusable template instead of inventing a project.

## Scope

Designed for websites and web applications, including portfolios, corporate sites, e-commerce, SaaS interfaces, dashboards, and internal tools. Product-specific workflows still need to be supplied or defined in the brief.

This is a planning skill. Implementation, package installation, service provisioning, and deployment require a corresponding user request. A completed specification is not evidence of tested accessibility, performance, or working integrations.

## Validation

The skill has passed Codex skill-creator's structural validator. Behavioral evaluation against real project briefs remains a next step.
