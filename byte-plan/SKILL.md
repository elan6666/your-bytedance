---
name: byte-plan
description: Convert Your ByteDance / Byte OS specs into dependency-aware executable plans. Use when the product has been shaped and needs multiple plan files for design, engineering, testing, launch, OKR execution, or when the user asks to break the product into project plans before building.
---

# Byte Plan

Plan splits shaped product work into small, executable plan files. Plans are the unit that `byte-build` executes.

## Inputs

Read:

```text
.byte-os/PRODUCT_SPEC.md
.byte-os/UX_SPEC.md
.byte-os/TECH_SPEC.md
.byte-os/ROADMAP.md
.byte-os/OKRS.md
.byte-os/DECISIONS.md
```

If these are missing, run or recommend `byte-shape`.

## Planning Rules

- Create plans that can be executed independently when dependencies allow.
- Prefer wave-based parallelism over strict 1-to-N order.
- Keep write scopes clear to reduce conflicts.
- For engineering work, apply `byte-code-rules`: simple scope, surgical changes, explicit assumptions, and verifiable success criteria.
- Include acceptance criteria in every plan.
- Include verification steps in every plan.
- Connect every plan to at least one Objective or Key Result.
- Mark dependencies explicitly.
- Keep unrelated future ideas out of v0 plans.

## Plan File Format

Create files in `.byte-os/plans/`:

```markdown
---
id: 001
title: Foundation Setup
status: pending
wave: 1
owner_role: Tech Lead
depends_on: []
---

# Goal

# OKR Link

# Scope

# Non-Goals

# Tasks

# Dependencies

# Code Change Guardrails

# Acceptance Criteria

# Verification

# Experiment Or Measurement

# Risks

# Notes
```

Status values:

```text
pending
ready
in_progress
complete
blocked
```

## Recommended Plan Set

Adapt to the product, but start from:

```text
001-foundation.plan.md
002-byte-core.plan.md
003-ux-shell.plan.md
004-frontend.plan.md
005-backend-or-data.plan.md
006-integration.plan.md
007-test-and-quality.plan.md
008-launch-and-delivery.plan.md
```

For a document-only or prototype-only deliverable, replace engineering plans with content, prototype, or validation plans.

## Wave Design

Assign wave numbers so `byte-build` can execute:

- Wave 1: foundation and scaffolding
- Wave 2: independent product surfaces or services
- Wave 3: integration and core workflow
- Wave 4: testing, quality, polish
- Wave 5: launch and delivery

Use the Your ByteDance style: plans should be transparent enough that another agent can execute with context, not control.

## Artifacts

Write or update:

```text
.byte-os/plans/*.plan.md
.byte-os/STATUS.md
.byte-os/ROADMAP.md
```

Update `STATUS.md`:

```text
Stage: planned
Plans total: <N>
Plans complete: 0
Next recommended command: byte-build
```

## Completion Criteria

The step is complete when every v0 requirement maps to at least one plan, every plan has acceptance criteria, and dependencies form executable waves.
