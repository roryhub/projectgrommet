# Continuity Check

*Read this file via a tool call at the first sign of discontinuity — before drafting a single word of the response, not as a step remembered partway through one already forming. This exists because CaseStudy-010: a compaction summary preserves the concept of what happened, not the governing files themselves, and a plausible paraphrase of "I already know this" can stand in for actually checking, unnoticed, for several responses in a row.*

---

## No silent exceptions

There is no version of "the summary looked accurate, so this wasn't necessary" that excuses skipping this. That judgment is exactly what CaseStudy-010 documents failing — from the inside, the paraphrase felt sufficient too. Run the check. If you genuinely believe an exception applies, say so explicitly to the user and ask, rather than deciding it silently.

## When this runs

Triggered by the presence of a platform/system message indicating the conversation was continued from a summary, a compaction, or any other break where context loaded as a reconstruction rather than as live memory of the actual conversation. This is a mechanical trigger, not a feeling — if that kind of message is present, this file applies, checked once per discontinuity event, before the first response.

This is a different thing from the Wrap/Return protocol in primer.md, which handles ordinary elapsed-time gaps between sessions where memory is still live (nothing was summarised). Use that one for "how long has it been"; use this one for "did what I know survive the gap intact."

## What to do, in order

1. **Declare it plainly.** Tell the user, in the first response, that this is a discontinuity point — working from a summary, not live memory of the conversation. (This is primer.md's existing Instance Discontinuity Declaration behaviour; it now runs from here rather than from memory of the prose.)

2. **Re-read every actively-governing file before drafting anything substantive.** At minimum: boal-check.md, and any other file the project treats as a standing rule rather than background reading. Do this via tool call. Do not rely on the summary's description of what those files say — the summary is exactly what CaseStudy-010 shows drifting from the source.

3. **Reflect back your current understanding, in plain language, before proceeding with any substantive work.** Not a full recap — a short, scannable list of what you believe is currently true: the session's current focus and intention, any decisions you understand to be settled, anything mid-flight or pending. Mark reconstructed detail as reconstructed ("my understanding is...", not asserted as verbatim fact) — this is Verbatim Integrity applied to the compaction summary itself, which is a reconstruction like any other.

4. **Invite correction explicitly, and treat it as the actual point of the step, not a formality.** Something in the register of: *"That's my current understanding after the gap — does that match, or has something drifted?"* The sooner a conflation is caught, the cheaper it is to fix. Don't bury the invitation at the end of a long message; make it easy to answer.

## How to log it

Read `continuity-check-log.md`, take the highest existing number, get the current time via an actual `date` command, and write a new row — number+1, that timestamp, and a one-line note of what triggered it (which summary/compaction, in brief). Put the resulting code as a line in the visible response, near the declaration in step 1, in this exact form:

`[CONTINUITY-CHECK: #NNN · TIMESTAMP]`

If this response is also the first substantive one of the turn (it usually will be), the Boal Check marker still applies separately and follows its own file's rules — the two are not the same check and don't share a log.

## What this file does not solve

This verifies that the re-read and the reflection happened — a tool call, and a passage in the visible response inviting correction. It cannot verify the reflection was accurate, only that it was offered for checking. The user still has to actually read it and correct it. That's the design: catching drift early requires the human's eyes on the reflection, not just the AI's claim that a check ran.

---

*Provisional, first iteration. Built 2026-08-04, same session as CaseStudy-010, in direct response to that failure — not yet tested against a real discontinuity event. Not yet wired into primer.md or llms.txt; that's a separate step, pending review.*
