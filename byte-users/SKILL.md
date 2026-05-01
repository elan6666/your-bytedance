---
name: byte-users
description: Analyze real post-build user feedback for Your ByteDance / Byte OS. Use only when a product, prototype, URL, screenshot, recording, analytics export, interview notes, survey results, support tickets, reviews, or other real user evidence is available. Do not use for simulated personas.
---

# Byte Users

Byte Users analyzes real user experience after something exists to test. It must never invent, simulate, or role-play real user feedback.

## Hard Rule

If no real user evidence is available, stop and request evidence. You may provide a user testing plan, but do not write fake feedback.

Valid evidence includes:

- User interview notes
- Usability test notes
- Screen recordings
- Product screenshots with observed behavior
- Analytics or event logs
- Support tickets
- App store or marketplace reviews
- Public comments about the product
- A working URL or local build that can be tested

## Workflow

1. Confirm evidence:

- What source is this?
- When was it collected?
- Which user segment does it represent?
- How many users or sessions?
- What task were users trying to complete?

2. Analyze:

- Activation friction
- Comprehension problems
- Navigation problems
- Missing features
- Trust blockers
- Performance complaints
- Pricing or value objections
- Repeated requests
- Outlier feedback

3. Convert to product implications:

- Must fix
- Should fix
- Investigate
- Ignore for now
- Add to roadmap

4. Connect to OKRs:

- Which Key Result moved or failed to move?
- Which user evidence changes the objective, scope, or roadmap?
- Which feedback is too weak or sparse to act on yet?

5. Feed iteration:

- Create recommended iteration items.
- Update roadmap and status.

## Artifacts

Write:

```text
.byte-os/users/real-feedback.md
.byte-os/users/user-testing-report.md
.byte-os/STATUS.md
```

`real-feedback.md` should preserve source context and distinguish quotes, paraphrases, and analysis.

`user-testing-report.md` should include:

- Evidence summary
- Key user tasks
- Observed friction
- Severity
- Recommended fixes
- Product opportunities
- Confidence level

## Completion Criteria

The step is complete when real feedback has been converted into prioritized iteration input without overstating what the evidence proves.

Next recommended command:

```text
byte-iterate
```
