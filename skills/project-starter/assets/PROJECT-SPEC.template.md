# Project specification

## Foundations

### Project context

Project: [Input: name]
Purpose and primary user task: [Input]
Audience: [Input]
Status: Draft
Decision labels: Confirmed / Proposed / Open / Not applicable

### Stack

| Layer | Choice and version, if verified | Status | Rationale / constraints / source |
| --- | --- | --- | --- |
| Framework / platform | [Input] | Open | [Input] |
| Styling | [Input] | Open | [Input] |
| Motion | [Input: e.g. Framer Motion, GSAP, CSS, or none] | Open | [Input] |
| Icons | [Input or none] | Open | [Input] |
| CMS | [Input or none] | Open | [Input] |
| Database | [Input or none] | Open | [Input] |
| Deployment | [Input] | Open | [Input] |

### Scope and requirements

| ID | Required page / route | User task and content | Core interactions | Components | Completion condition |
| --- | --- | --- | --- | --- | --- |
| PAGE-01 | [Input] | [Input] | [Input] | [Input] | [Observable result] |

| ID | Integration | Purpose and data flow | Configuration / ownership | Failure behavior | Status |
| --- | --- | --- | --- | --- | --- |
| INT-01 | [Input or none] | [Input] | [Names only; no secrets] | [Input] | Open |

- Content source and editor workflow: [Input]
- Authentication and roles: [Input or Not applicable]
- Responsive expectations: [Input; detailed rules below]
- Animation requirements: [Input; detailed rules below]
- Accessibility target: [Input]
- SEO, performance, privacy, localization, and browser constraints: [Relevant requirements only]
- Out of scope: [Input]

## Design System

### Typography

| Family role | Family | Fallbacks | Weights | Source / license status |
| --- | --- | --- | --- | --- |
| Heading | [Input] | [Input] | [Input] | [Input] |
| Body | [Input] | [Input] | [Input] | [Input] |
| Mono (monospace) | [Input or Not applicable] | [Input] | [Input] | [Input] |

The values below are supplied starting points, not confirmed responsive rules. Express final sizes in rem or a documented fluid expression. Define line heights as unitless ratios. Assign HTML headings by document hierarchy.

| Role / token | Supplied starting point | Small-screen value | Large-screen value | Weight | Line height | Tracking |
| --- | --- | --- | --- | --- | --- | --- |
| Hero / text-hero | 64px | [Input] | [Input] | 700 | 1.2 | [Input] |
| Section / text-section | 40px | [Input] | [Input] | 700 | 1.2 | [Input] |
| Subheading / text-subheading | 28px | [Input] | [Input] | 700 | 1.2 | [Input] |
| Body / text-body | 16px | [Input] | [Input] | [Input] | 1.4 | [Input] |
| Body large / text-body-lg | 18px | [Input] | [Input] | [Input] | 1.4 | [Input] |
| Small / text-small | 14px | [Input] | [Input] | [Input] | 1.2 | [Input] |
| Eyebrow / text-eyebrow | 10px | [Input] | [Input] | 400 | 1.1 | [Input] |

Reading width, wrapping, text zoom, font-loading behavior: [Input]
Small text review: [Evaluate the 10px eyebrow in context; propose an adjustment if readability suffers.]

### Colors

Theme scope and initial theme selection: [Input]
Theme persistence and control: [Input or Not applicable]
60/30/10 composition direction: [Optional qualitative guidance]

#### Primitive palette

| Token | Value | Purpose |
| --- | --- | --- |
| [palette token] | [Hex / OKLCH value] | [Input] |

#### Semantic mappings

Use exact values or references to defined primitive tokens. Remove unsupported theme columns.

| Semantic token | Light | Dark | Usage / foreground pair |
| --- | --- | --- | --- |
| color-primary | [Input] | [Input] | Main brand or action role; define which |
| color-on-primary | [Input] | [Input] | Text and icons on primary |
| color-secondary | [Input] | [Input] | Secondary role; define foreground |
| color-accent | [Input] | [Input] | Emphasis; define foreground |
| color-background | [Input] | [Input] | Page canvas |
| color-surface | [Input] | [Input] | Cards and panels |
| color-surface-muted | [Input] | [Input] | Subtle backgrounds |
| color-text | [Input] | [Input] | Primary text |
| color-text-muted | [Input] | [Input] | Secondary text |
| color-border | [Input] | [Input] | Boundaries |
| color-focus | [Input] | [Input] | Keyboard focus indicator |
| color-success | [Input] | [Input] | Success; define foreground and surface |
| color-error | [Input] | [Input] | Error; define foreground and surface |
| color-warning | [Input] | [Input] | Warning; define foreground and surface |

Hover, active, selected, disabled, and link tokens: [Define required mappings]
Contrast verification: [Pairs, target, measured result if actually checked, otherwise Pending]
Non-color status cues: [Icons, labels, or other cues]

### Spacing

| Token group | Names and exact values | Usage |
| --- | --- | --- |
| Spacing scale | [Input] | Insets, gaps, stacks |
| Layout | [Input] | Max widths, columns, gutters, section padding |
| Radius | [Input] | Component corners |
| Borders | [Input] | Widths and styles |
| Elevation | [Input] | Shadows and overlays |
| Layering | [Input] | Navigation, overlays, dialogs, notifications |

### Components

Create entries only for components required by the project. Repeat this contract per component:

#### [Component name / ID]

- Purpose and consuming pages: [Input]
- Anatomy and content rules: [Input]
- Variants and sizes: [Input]
- Tokens: [References to defined tokens]
- Interaction and state behavior: [Relevant default, hover, focus, active, disabled, loading, empty, error, success states]
- Semantics and keyboard behavior: [Input]
- Responsive behavior: [Input]
- Acceptance criteria: [Observable result]

### Animations

| ID / element | Purpose and trigger | Property / from-to | Duration / easing | Reduced-motion behavior |
| --- | --- | --- | --- | --- |
| [Input or none] | [Input] | [Input] | [Input] | [Input] |

Motion tokens and interruption/repetition rules: [Input or Not applicable]

### Responsive Rules

| Layout condition / exact breakpoint | Layout changes | Typography / spacing changes | Component changes |
| --- | --- | --- | --- |
| Base layout | [Input] | [Input] | [Input] |
| [Content-driven threshold] | [Input] | [Input] | [Input] |

- Minimum supported viewport and target browsers: [Input]
- Navigation transformation: [Input]
- Media sizing, cropping, and aspect ratios: [Input]
- Touch and keyboard operation: [Input]
- Long text, localization, zoom, overflow, and reflow: [Input]
- Verification widths and representative pages: [Input; include intermediate widths]

## Development Plan

### Decisions to resolve

| Open decision | Why it matters | Blocks | Next step / owner |
| --- | --- | --- | --- |
| [Input or none] | [Input] | [Phase / task or non-blocking] | [Input] |

### Implementation sequence

| Phase | Deliverable | Requirement IDs | Dependencies | Acceptance criteria |
| --- | --- | --- | --- | --- |
| 1. Foundations | [Stack configuration and tokens] | [IDs] | [Decisions] | [Observable checks] |
| 2. Components | [Required component contracts implemented] | [IDs] | Phase 1 | [Observable checks] |
| 3. Pages and integrations | [Routes, content, interactions] | [IDs] | Phase 2 / external setup | [Observable checks] |
| 4. Validation and release readiness | [Relevant verification] | [IDs] | Phase 3 | [Project-specific criteria] |

### Verification record

| Check | Method and scope | Status | Evidence / outstanding issue |
| --- | --- | --- | --- |
| Scope and interaction coverage | [Input] | Planned | [Input] |
| Responsive and content edge cases | [Input] | Planned | [Input] |
| Accessibility and reduced motion | [Input] | Planned | [Input] |
| Integration failure and recovery | [Input or Not applicable] | Planned | [Input] |
| Performance / SEO as required | [Input or Not applicable] | Planned | [Input] |

Document review is distinct from implementation verification. Release work is performed only within the user's requested scope.
