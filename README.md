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

## Install in Codex

Clone this repository, then copy `skills/project-starter` into your Codex skills directory, usually `~/.codex/skills/`. If you use a custom `CODEX_HOME`, use its `skills/` directory instead. Preserve any existing installation before replacing it.

For other agents that support `SKILL.md` packages, use the same skill folder with that agent's installation mechanism. Compatibility with other agents has not been tested.

## Usage

Invoke the skill in a project with your brief:

> Use $project-starter to create PROJECT-SPEC.md for a bilingual corporate website. Required pages: home, about, products, product details, and contact. Next.js and DatoCMS are confirmed. Propose the remaining choices, explain the rationale, and identify architectural questions before implementation.

Provide whatever is available: audience, primary user task, brand guidelines, required pages, interactions, technology constraints, integrations, and reference material.

The skill writes `PROJECT-SPEC.md` at the project root unless you request another location. With no project brief, it produces a reusable template instead of inventing a project.

## Scope

Designed for websites and web applications, including portfolios, corporate sites, e-commerce, SaaS interfaces, dashboards, and internal tools. Product-specific workflows still need to be supplied or defined in the brief.

This is a planning skill. Implementation, package installation, service provisioning, and deployment require a corresponding user request. A completed specification is not evidence of tested accessibility, performance, or working integrations.

## Validation

The skill has passed Codex skill-creator's structural validator. Behavioral evaluation against real project briefs remains a next step.
