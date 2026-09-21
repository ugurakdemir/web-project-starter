---
name: project-starter
description: Turn a website or web application brief into a project-specific PROJECT-SPEC.md covering stack decisions, visual tokens, component behavior, responsive rules, and an implementation plan. Use when starting a project or formalizing its foundations, design system, and development plan before coding.
---

# Project starter

Produce an actionable `PROJECT-SPEC.md` from the user's brief and available project evidence. This skill defines the project; implementation follows only when requested. Preserve explicit technology, brand, scope, and language choices.

## Understand the project

Read the brief and relevant existing project instructions, dependencies, styles, and components, if available. Reuse established decisions rather than treating an existing project as a blank slate. Do not overwrite an existing project specification or design system without reading it and retaining valid project-specific content.

Establish the product purpose, audience, primary user task, required pages, core interactions, content ownership, integrations, responsive expectations, and relevant constraints. Ask a compact batch of questions only for gaps that materially change scope or architecture. Continue drafting independent sections while questions are open.

Distinguish **Confirmed**, **Proposed**, **Open**, and **Not applicable** decisions. Infer low-impact defaults and label them Proposed. Do not invent business requirements, brand assets, project claims, integration credentials, or user approvals. Unanswered architectural questions remain Open; do not silently resolve them by choosing a favorite stack.

If the request contains only this template and no product brief, return a reusable template with clearly identified input fields, not a fictional project specification.

## Make coherent decisions

- Treat framework/platform, styling, motion, icons, CMS, database, and deployment as independent decisions with compatibility implications. CMS and database may be unnecessary. A platform can fulfill several roles; do not add a duplicate service by default.
- Record the reason and constraints for stack choices. Verify current versions, compatibility, hosting limitations, and licensing against official sources when making those claims; if verification is unavailable, identify the uncertainty instead of guessing.
- Define Heading, Body, and Mono (monospace) font roles. Specify where Mono is used, or mark it Not applicable when unnecessary. Keep font families separate from motion behavior.
- Treat supplied font sizes as starting values unless explicitly fixed. Define responsive sizes, weights, line heights, tracking, fallbacks, and intended roles. Visual text roles do not determine semantic HTML heading levels.
- Separate primitive color values from semantic roles. Map each semantic token to explicit light and dark values when both themes are in scope. Define foreground/background pairs and interaction states. Use the 60/30/10 rule as optional visual direction, not an enforced pixel ratio or accessibility test.
- Define spacing, layout widths, gutters, radii, borders, shadows, and layering with reusable tokens. Specify values and usage, avoiding unexplained token lists.
- Derive the component inventory from required pages and interactions. Specify relevant variants, states, keyboard/focus behavior, responsive behavior, and token use. Include loading, empty, success, and error states where the actual flow requires them.
- Give motion a purpose, duration, easing, trigger, and reduced-motion alternative. Never require animation to access essential content or actions.
- Derive responsive rules from content and layout needs. If using framework breakpoints, state their exact values and intended layout changes. Include touch, keyboard, long content, and zoom behavior.

## Write the deliverable

Read and adapt [assets/PROJECT-SPEC.template.md](assets/PROJECT-SPEC.template.md). Write `PROJECT-SPEC.md` at the requested location, otherwise at the project root. Preserve its three top-level sections in this order: Foundations, Design System, Development Plan. Add detail as subsections. Foundations contains project context, stack, scope, and requirements. Design System contains Typography, Colors, Spacing, Components, Animations, and Responsive Rules.

For a project-specific document, replace input fields with decisions, explicitly Open items, or Not applicable items. For a reusable template, retain clearly labeled input fields. Put scope and the requirements checklist under Foundations; put dependencies, phases, open decisions, and acceptance criteria under Development Plan.

Keep this document usable as an implementation contract: specify actual token names and values where selected, trace pages and interactions to components and development phases, and separate planned verification from completed checks. Include source links for externally verified claims. Do not claim a working integration, performance score, or accessibility conformance from a specification alone.

## Review and hand off

Check for contradictory stack choices, unresolved token references, missing theme mappings, omitted required pages or interactions, and development tasks without an observable completion condition. Resolve inconsistencies supported by evidence and list remaining blockers with their impact.

Return the document location, a brief account of the key decisions, and any questions that must be resolved before implementation. Do not install packages, provision services, publish, or start implementation solely because a technology appears in the document.
