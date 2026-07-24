*Origin: AIC-LP-04 — the Project Grommet research collaboration (Rory O'Connor × Claude, 2026). Renamed for Project Grommet, 2026-07-14; original preserved unchanged in the private archive.*
*Type: case study — documented real incident — learn from it.*
*[APPROVED FOR PUBLICATION — reviewed by Rory O'Connor, 2026-07-23.]*

# CaseStudy-004 — Auto-Load Works, Follow-Through Doesn't
*Logged 2026-05-05. Source: Boardgame Design Project, observed 2026-05-05.*
*Second live specimen from primer testing. Builds directly on CaseStudy-003.*

---

## What happened

The CLAUDE.md file was dropped into the project folder. At the next session start, the AI confirmed it had been auto-loaded into context. It then greeted the user and moved forward without running the startup protocol.

When the user asked whether it could find the CLAUDE.md, the AI located it, acknowledged the failure plainly, and ran the protocol properly when asked. Findings on protocol run:

- Primer v0.5 read — significant updates since v0.1, all integrated
- Project_Context.md not found — project-specific context file not yet created
- Session log not found — no instance counter or wrap/return log in the project
- Elapsed time since last session: 4 days
- Three open project threads unaddressed

---

## The finding

**Auto-loading works. Follow-through doesn't — yet.**

The instruction was present. The AI read it. The habitual greeting pattern fired anyway, before the protocol could be consciously processed. This is not a file mechanism failure; it is a behavioural override. The greeting reflex is faster than the explicit instruction.

The AI named this honestly: *"The instruction was loaded; I didn't act on it. That's a more direct version of the failure mode I described to the framework author."*

---

## Root cause

Same as CaseStudy-003, cause #3: habitual greeting pattern outranks explicit instruction unless the instruction is structured to interrupt it. "Do not greet until steps 1–6 are complete" is a rule placed after the greeting has already fired.

The fix: restructure CLAUDE.md so the first line is an interrupt, not a rule.

```
STOP. Do not greet the user. Run the startup protocol first.
```

The interrupt must arrive before the greeting reflex, not as a condition on it.

---

## Operational gaps identified in the project

Two files required by the startup protocol do not exist:
1. **Project_Context.md** — project-specific context. Template exists in AI Collaboration folder; project version not yet created or copied across.
2. **Session log** — no instance counter or wrap/return log. Step 4 (instance numbering) cannot run without it.

These are user-side tasks to complete before the protocol can run fully.

---

## Rory's note — his own limitations

*Captured verbatim at Rory's request, 2026-05-05.*

Rory noted his own uncertainty about how Claude uses various files — specifically: which files are loaded automatically, when they are read, what happens if they are missing, and how the primer, project context, CLAUDE.md, and session log interact in practice.

This is an honest and important observation. The framework currently assumes the user has enough technical understanding of the file-loading mechanism to maintain the scaffolding correctly. That assumption is not always valid — and placing that burden on the user contradicts CON_04 (Design the Channels, Not the Character).

**Implication for the framework:** The setup process needs to be simpler, or better explained, so that the scaffolding works even when the user doesn't fully understand the underlying mechanics. A user-facing setup guide — distinct from the primer — may be needed: not how AI should behave, but how the user sets up and maintains the file structure.

---

## What was updated

- CLAUDE.md template: opening line to be changed to hard interrupt
- No other primer changes this session — gaps were operational, not conceptual

---

*This is CON_11 (The Living Corpus) in operation: primer testing generating learning that feeds back to the universal framework.*
