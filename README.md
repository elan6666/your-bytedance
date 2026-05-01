# Your ByteDance Skills

Your ByteDance Skills is a Codex skill suite for taking a product from a rough idea to a deliverable result.

It simulates your own ByteDance-inspired product squad: product, market research, UX, design, engineering, QA, growth, review, delivery, and post-build user feedback. It is not affiliated with ByteDance. It uses public ByteDance, Lark, Feishu, and BytePlus materials as inspiration for a fast, transparent, data-driven product operating system.

The underlying skill names stay `byte-*` so they remain easy to invoke from Codex.

## What It Does

Your ByteDance helps you:

- Start a new product from a rough idea.
- Research competitors, alternatives, pricing, trends, and user complaints.
- Shape product positioning, MVP scope, user flows, UX, and technical direction.
- Split work into dependency-aware executable plans.
- Build by execution waves instead of blindly running plan 1, plan 2, plan 3.
- Review the product like a cross-functional project team.
- Run automatic iteration loops before delivery.
- Analyze real user feedback after the product exists.
- Package final delivery notes, run instructions, verification, and risks.

## Operating Model

Your ByteDance applies these operating principles:

- **Always Day 1:** keep an entrepreneurial mindset, reduce unnecessary process, and prefer fast learning.
- **Context, not control:** write shared context into `.byte-os/` so agents can make better decisions without repeated permission checks.
- **Candid and clear:** expose problems directly, separate facts from assumptions, and avoid vague product language.
- **Seek truth and be pragmatic:** use market research, first-hand user evidence, tests, and measurable impact.
- **Aim high with ROI:** take calculated risks, compare alternatives, and push for a higher-standard deliverable.
- **Transparent OKRs:** connect product goals, plans, and build work to visible objectives and key results.
- **Experimentation culture:** turn uncertain product decisions into hypotheses, metrics, tests, or iteration loops.
- **Cross-functional squads:** product, design, engineering, QA, research, and growth work in parallel where dependencies allow.

## Core Flow

Your ByteDance has two operating modes.

### Step-by-Step Mode

Use this when you want control over each stage:

```text
byte-start
byte-shape
byte-plan
byte-build
byte-review
byte-iterate
byte-deliver
```

Each command advances the project one major stage while preserving the full internal process.

### Auto Mode

Use this when you want the system to run end to end:

```text
byte-auto
```

Auto mode runs the same stages as step-by-step mode, then performs at least 3 iteration loops before delivery.

## Skill List

| Skill | Purpose |
|---|---|
| `byte-do` | Natural-language router for the whole Byte OS suite. |
| `byte-start` | Initialize `.byte-os/`, understand the idea, and create the product foundation. |
| `byte-research` | Research competitors, market signals, pricing, trends, and user complaints. |
| `byte-shape` | Define positioning, MVP, scope, UX structure, technical direction, and roadmap. |
| `byte-plan` | Convert specs into dependency-aware plan files. |
| `byte-build` | Execute plans by dependency-ready waves. |
| `byte-review` | Run a cross-functional product, UX, tech, QA, and growth review. |
| `byte-iterate` | Run structured iteration loops based on review findings, research, tests, or real feedback. |
| `byte-users` | Analyze real post-build user feedback only. It does not simulate users. |
| `byte-status` | Show current Byte OS state, progress, blockers, and next action. |
| `byte-next` | Infer and execute the next step from `.byte-os/` state. |
| `byte-auto` | Run from idea to delivery automatically with at least 3 iterations. |
| `byte-deliver` | Package final delivery notes, run instructions, verification, and known risks. |

## Byte State

Your ByteDance writes byte state into:

```text
.byte-os/
  BYTE.md
  STATUS.md
  OKRS.md
  DECISIONS.md
  RESEARCH.md
  COMPETITORS.md
  USER_ASSUMPTIONS.md
  PRODUCT_SPEC.md
  UX_SPEC.md
  TECH_SPEC.md
  ROADMAP.md
  BUILD_LOG.md
  DELIVERY.md
  plans/
  reviews/
  iterations/
  users/
```

This byte state directory lets the skills resume work, route the next action, track decisions, expose OKRs, and avoid asking the user to repeat context.

## Installation

Copy the `byte-*` skill folders into your Codex skills directory:

```text
~/.codex/skills/
```

On Windows, this is usually:

```text
C:\Users\<you>\.codex\skills\
```

Example:

```text
cp -r byte-* ~/.codex/skills/
```

## Usage Examples

Start from a rough idea:

```text
$byte-do I want to build an AI study assistant for university students
```

Run the full process automatically:

```text
$byte-auto Build a web app for solo founders to validate product ideas. Iterate 4 times.
```

Research competitors:

```text
$byte-research Compare this product against Notion, Linear, and Trello
```

Continue the next step:

```text
$byte-next
```

Check progress:

```text
$byte-status
```

Analyze real user feedback after the product exists:

```text
$byte-users Here are user interview notes and session recordings from our prototype test
```

## Important Rules

- `byte-users` is only for real post-build user evidence.
- Your ByteDance may use user assumptions before build, but it must not pretend those are real users.
- `byte-build` executes the next dependency-ready wave by default, not simply the first plan.
- `byte-auto` uses the same staged workflow as manual mode; it just runs the stages continuously.
- Modern competitor, pricing, market, or "latest" claims require current web research and citations.
- Every product stage should update or respect the current objective, key results, decision log, and evidence level.

## Public Research Basis

This suite is ByteDance-inspired, not ByteDance-official. The current operating model is based on public materials:

- [ByteDance Culture](https://joinbytedance.com/culture) describes ByteStyle values including Always Day 1, candid and clear communication, seeking truth, pragmatism, high standards, and growth together.
- [Lark OKR](https://larksuite.my/okr) materials emphasize transparent OKRs, alignment across teams, and health dashboards for monitoring progress and risks.
- [TechNode reporting on Feishu People](https://technode.com/2022/05/26/bytedance-launches-hr-management-tool-feishu-people/) describes ByteDance's use of OKR-oriented management tooling.
- [BytePlus A/B testing material](https://www.byteplus.com/downloads/How-to-Avoid-Common-Mistakes-When-AB-Testing.pdf) emphasizes experimentation, sufficient test duration, enough traffic, statistical confidence, and data-driven product improvement.

## Recommended First Test

Use a real product idea and run:

```text
$byte-auto <your product idea>
```

Then inspect `.byte-os/` to see the generated foundation, specs, plans, reviews, iterations, and delivery notes.
