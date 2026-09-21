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

### One-line installation (recommended)

With Node.js/npm installed, use the [Vercel Labs Skills CLI](https://github.com/vercel-labs/skills):

```bash
npx skills add ugurakdemir/web-project-starter --skill project-starter
```

Follow the prompts to select agents and installation scope. To target Codex, Claude Code, Gemini CLI, and Cursor globally:

```bash
npx skills add ugurakdemir/web-project-starter --skill project-starter -g -a codex claude-code gemini-cli cursor
```

`-g` installs for use across projects on your machine. Omit it to install into the current project. You can also select just one agent with `-a`, as shown for Cursor below. The following sections provide platform-specific alternatives and usage instructions.

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

### Cursor

Install globally for Cursor:

```bash
npx skills add ugurakdemir/web-project-starter --skill project-starter -g -a cursor
```

For a project-specific installation, run the command from your target project and omit `-g`.

Alternatively, clone this repository and copy the complete `skills/project-starter` folder into `~/.cursor/skills/` for local use across projects, or `.cursor/skills/` inside your target project. Preserve any existing installation before replacing it. Include both `SKILL.md` and the `assets/` directory.

Restart Cursor after installation if the skill is not discovered. In Agent chat, type `/`, select `project-starter`, and provide your brief:

```text
/project-starter Create PROJECT-SPEC.md for a bilingual corporate website. Next.js and DatoCMS are confirmed. Propose the remaining choices and identify architectural questions before implementation.
```

See the [official Cursor skills documentation](https://cursor.com/docs/skills).

Claude Code, Gemini CLI, and Cursor support this skill's file structure. Installation commands and runtime behavior in these agents have not yet been tested for this repository.

## Usage

In Codex, invoke the skill in a project with your brief (use the platform-specific invocation above for Claude Code, Gemini CLI, or Cursor):

> Use $project-starter to create PROJECT-SPEC.md for a bilingual corporate website. Required pages: home, about, products, product details, and contact. Next.js and DatoCMS are confirmed. Propose the remaining choices, explain the rationale, and identify architectural questions before implementation.

Provide whatever is available: audience, primary user task, brand guidelines, required pages, interactions, technology constraints, integrations, and reference material.

The skill writes `PROJECT-SPEC.md` at the project root unless you request another location. With no project brief, it produces a reusable template instead of inventing a project.

## Scope

Designed for websites and web applications, including portfolios, corporate sites, e-commerce, SaaS interfaces, dashboards, and internal tools. Product-specific workflows still need to be supplied or defined in the brief.

This is a planning skill. Implementation, package installation, service provisioning, and deployment require a corresponding user request. A completed specification is not evidence of tested accessibility, performance, or working integrations.

## Validation

The skill has passed Codex skill-creator's structural validator. Behavioral evaluation against real project briefs remains a next step.
