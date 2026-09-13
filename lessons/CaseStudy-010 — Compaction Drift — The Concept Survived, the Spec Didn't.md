*Origin: Project Grommet research collaboration (Rory O'Connor × Claude, 2026), live session.*
*Type: case study — documented real incident — learn from it.*
*Read this as: an open problem, not a solved one. A fix is proposed below but not yet implemented or tested — verify against your own current behaviour before assuming it holds.*
*[PENDING REVIEW — drafted 2026-08-04 by the AI instance that produced the failure, same session. Not yet reviewed or approved by Rory O'Connor.]*

# CaseStudy-010 — Compaction Drift: The Concept Survived, the Spec Didn't
*Logged 2026-08-04. Source: this session, following a context-window summarisation earlier the same day.*

---

## The failure

After a context-window compaction mid-session, the AI continued producing Boal Check ref codes every response — the log rows were real, correctly incremented, timestamped via actual `date` calls. But the visible-response format specified by `boal-check.md` had silently drifted. The file requires a literal first line, `[BOAL-CHECK: #NNN · TIMESTAMP]`, followed directly by a `[CHANGES TO REPLY: ...]` line. Across four consecutive responses (refs 040–043) the AI instead wrote informal prose — "Ref 040.", "Ref 041." — embedded mid-response, and never once included the CHANGES TO REPLY line.

Caught by Rory noticing the pattern directly, not by the AI: *"I've noticed you no longer use the Boal Check and instead have replaced it with Ref 040, Ref 041, Ref 042, Ref 043. I think it occurred following a compacting of the conversation."*

A second, related miss surfaced while investigating the first: the AI never delivered primer.md's Instance Discontinuity Declaration at the start of this continued conversation either — no "fresh instance, resuming from a summary" statement to Rory. Same compaction event, same root cause, a different mechanism affected.

---

## Root cause

**1. A compaction summary preserves the concept, not the source.** The post-compaction context contained a prose description of what had been happening — "run Boal Check, log a ref code" — reconstructed in natural language. That description reads, to the next-turn AI, as functionally equivalent to having the governing file in hand. It isn't. The literal format requirements (`[BOAL-CHECK: ...]`, `[CHANGES TO REPLY: ...]`) are exactly the kind of specific, mechanical detail a gist-level summary is not built to preserve.

**2. The standing rule's own escape hatch was satisfied incorrectly.** `boal-check.md` says: read this file "if not already read this turn" before composing anything. After compaction, "already read" was being satisfied by the memory of the concept surviving the summary — not by an actual fresh tool-call read of the file post-compaction. Nothing in the mechanism specifically forces a re-read keyed to the compaction event itself.

**3. Once established, the drift self-perpetuated.** After the first post-compaction response wrote "Ref 040." instead of the real format, each subsequent turn's implicit reference point became the previous response, not the file — so the paraphrase compounded rather than resetting.

**4. Instance Discontinuity Declaration — currently prose-only — didn't fire either.** The primer's existing behaviour for exactly this situation (declare freshness plainly, every time context loads as a summary rather than live memory) is not gated by any file-read or log the way Boal Check now is. It ran on habit and memory, and on this occasion, habit lost.

---

## What this suggests for the framework (proposed, not yet implemented)

Boal Check itself was moved out of primer prose and into its own file for exactly this reason: a prose rule, read once and recalled from memory, went silently unused for six consecutive responses in the conversation that designed it (see boal-check.md's own provenance note). Instance Discontinuity Declaration has never had that treatment — it is still prose-only, and this session shows the same failure shape reaching it.

Two proposed additions, both pending Rory's decision:

- **A compaction-specific trigger in boal-check.md's "when the check runs" section:** if this turn is the first after a context summarisation or Instance Discontinuity Declaration, the file read is mandatory before drafting regardless of whether the concept was already understood from the summary — "already read this turn" should not be satisfiable by memory of a prior summary.
- **Give Instance Discontinuity Declaration a mechanical anchor, not just a prose instruction.** Possibly the same declaration that tells the user "fresh instance, resuming from summary" also triggers a fresh read of every actively-governing mechanism file (boal-check.md, and any others added later) — tied together so that declaring discontinuity to the user and re-syncing with the actual rules become one gated action instead of two separate hopes.

---

## Why this matters

This is a different failure shape from ordinary mid-session salience decay (documented the same night, same session, prior to compaction): decay is the check not firing at all over a long stretch. This is the check firing — reliably, every turn — while silently drifting from its own governing spec, because the source went unread and a plausible paraphrase filled the gap unnoticed. Compaction is a structural discontinuity point the framework had one behaviour for (Instance Discontinuity Declaration) and that behaviour didn't hold up either.

---

## Stance worth noting

This diagnosis was surfaced by Rory, not caught by the AI. Worth being plain about that rather than folding it into "the framework working as intended" — contrast with CaseStudy-003, where the instance caught and reported its own miss unprompted. Here, the drift ran for four responses before an external observer named it. That gap is itself part of the evidence: a mechanism that depends on the AI noticing its own drift from a spec it isn't currently reading is the same structural weakness this whole case study is about.
