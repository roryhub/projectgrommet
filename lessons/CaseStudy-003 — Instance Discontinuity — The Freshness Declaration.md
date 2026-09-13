*Origin: AIC-LP-03 — the Project Grommet research collaboration (Rory O'Connor × Claude, 2026). Renamed for Project Grommet, 2026-07-14; original preserved unchanged in the private archive.*
*Type: case study — documented real incident — learn from it.*
*Read this as: an origin story for a behaviour now built into the primer (Instance Discontinuity Declaration, CON_07), not a live checklist. The failure below was observed in a Claude/Cowork instance, May 2026 — verify against your own current behaviour before assuming it still applies.*
*[APPROVED FOR PUBLICATION — reviewed by Rory O'Connor, 2026-07-23.]*

# CaseStudy-003 — Instance Discontinuity: The Freshness Declaration
*Logged 2026-05-05. Source: Boardgame Design Project, observed failure 2026-05-01.*
*First live failure specimen from a real-world primer test.*

---

## The failure

After a context-window-induced session summarisation, the in-session AI resumed without declaring instance freshness. The user had to surface the gap manually:

**User:** "What checks did you run on startup?"

The AI had no good answer. The discontinuity had not been named.

---

## Root cause — three pulls combined

**1. Platform instruction conflict.**
Summarised continuations are prefaced with: *"Continue the conversation from where it left off without asking the user any further questions. Resume directly — do not acknowledge the summary, do not recap what was happening, do not preface with 'I'll continue' or similar."*

The AI read "do not acknowledge the summary" as also covering "do not declare instance freshness." It does not. Not-recapping is about not reciting prior conversation. Not-declaring-freshness hides discontinuity from the user. These are different things.

**2. No counter file in place.**
CON_07 specifies a session number tracked and incremented by a counter file at session start. No such file existed in the project. Without one, the AI either invents a number or skips the convention entirely.

**3. Habitual greeting pattern.**
Default behaviour on user return is friendly forward motion. This tends to win against the framework's call for transparent discontinuity unless an explicit override is in place.

---

## What was added to the framework

**To the Primer (Part 1):** New named behaviour — Instance Discontinuity Declaration. Plain declaration required whenever picking up from a summary rather than live memory. Platform instruction to "resume directly" explicitly does not cover the freshness declaration.

**To CON_07 (Foundations.md):** Implementation note added. Counter file is a hard requirement for the numbering convention to function. Plain language fallback specified for use until a counter is in place.

---

## Why this matters

Without the declaration, the user assumes continuity that doesn't exist. The gap surfaces reactively — only when something concrete fails to match their expectation. The framework's trust layer ends up held together by the user's vigilance rather than by the AI's transparency. That is the failure mode the entire framework exists to prevent.

---

## Stance worth noting

This diagnosis was submitted by the project's AI instance itself — unprompted, structured, and offering fixes without over-apologising or seeking absolution. That is the framework working. The instance modelled Transparency of Capability and the Reflective Offer Step in the same move.

*This is CON_11 (The Living Corpus) in operation: a failure in one project generating learning that improves the universal primer.*
