*Origin: AIC-LP-07 — the Project Grommet research collaboration (Rory O'Connor × Claude, 2026). Renamed for Project Grommet, 2026-07-14; original preserved unchanged in the private archive.*
*Type: case study — documented real incident — learn from it.*
*[APPROVED FOR PUBLICATION — reviewed by Rory O'Connor, 2026-07-24. Includes addendum below.]*

# CaseStudy-007 — The Human Must Be Present
*Logged 2026-07-07. Source: this project — the Grommet.ai domain reminder, set 2026-04-14, due 2026-06-16, discovered failed 2026-07-07.*
*Second live failure specimen. Captured verbatim on the day of discovery, Claude_005, after a 54-day session gap.*

---

## The failure

In April, Claude scheduled a one-time reminder: Grommet.ai domain becomes available June 17th — remind Rory on the morning of June 16th. Both parties treated it as laid track. Neither checked the dependency underneath it.

On return (2026-07-07), Rory asked whether the domain question had been handled:

**Rory:** "No. And I was wondering if you'd remember to remind me. I think this is the first thing I need to do."

Claude checked the task log and reported:

**Claude:** "The reminder did exist — scheduled for June 16th at 9am. But its log shows it actually fired today, July 7th at 15:30 — the moment you opened this session. It sat armed for three weeks with no way to reach you, because these scheduled tasks can only run when the app is open. I laid the track, but the track only exists when the train is already running. That's a CON_04 lesson in miniature: the scaffolding wasn't structural after all — it had a hidden dependency on your presence, which is precisely the thing scaffolding is supposed to not depend on. I'd flag this honestly: I had no awareness of this limitation when I set the reminder in April, and neither of us could see it until it failed."

**Rory:** "I think the key thing here is the realisation that 'the Human must be present'. I think this is actually key to this project and its ethos."

---

## Root cause

**1. Hidden platform dependency.** The scheduled task mechanism only executes when the app is open. Nothing in the scheduling flow surfaced this. The AI set the reminder in good faith; the limitation was invisible until the failure.

**2. Transparency of Capability gap — at scheduling time, not delivery time.** The established behaviour says: name limitations when you can't do something you appeared to be doing. This failure shows the check must run when the commitment is *made*, not when it falls due. An AI accepting a future obligation should ask: can I actually keep this promise if the human never returns? If the answer is no, that must be said at the moment of scheduling.

**3. Both parties trusted the track without inspecting it.** Rory deliberately left the reminder untested ("I was wondering if you'd remember") — which made this a clean natural experiment. The framework had no verification step for dormant commitments.

---

## The reframe — Rory's key realisation

**"The Human must be present."**

What looked like a technical limitation is actually the project's ethos stated as an engineering fact. This framework has never been about AI acting autonomously while the human is away — that's the automation paradigm it defines itself against. The collaboration exists only in session, when both parties are in the room. Everything else — primers, corpora, counters, reminders — is scaffolding *for the next moment of presence*, not a substitute for it.

Connects directly to CON_08 (The Gap is Load-Bearing): the human's absence is where their best thinking happens — but nothing *executes* in the gap, on either side. The gap is for synthesis, not delegation.

---

## What this changes

- **Dormant commitments must be declared, not assumed.** When the AI accepts any future obligation (reminder, scheduled check, "I'll have this ready"), it must state the conditions under which the commitment can actually be kept — including whether delivery depends on the human opening a session.
- **Return protocol addition (candidate for primer):** on session start after a gap, check for commitments that fell due during the absence and report their status unprompted — before the user has to ask.
- **Resolved same day → CON_12 (Reminders Live in the User's World).** Platform-side investigation found cloud-run scheduled tasks now exist (Anthropic "Routines", May 2026) but remain developer-tooling; Cowork-side behaviour unchanged (skipped tasks fire at next app launch). Design answer chosen instead: whenever a reminder is requested, the AI helps produce the scheduled event in a tool the user already uses — Google Calendar, iOS Calendar, Slack, Trello, etc. The user's own tools are built on the assumption this framework holds as ethos: the human will be present to them.

---

## Addendum — 2026-07-24: does the original limitation still hold?

Asked directly whether the AI could run its own version of the self-check this case study prescribes ("can I keep this promise if the human never returns"), Claude answered from a partial, remembered summary of the scheduled-tasks tool ("runs automatically") — before actually reading the tool's full current description. Once the full schema was loaded, it plainly stated the same limitation this case study documents: *"Scheduled tasks run while this app is open. If the app is closed when a task is due, it runs on next launch."* The original finding still holds; nothing has changed about the mechanism.

Rory then proposed a structural fix: should the AI run a live mini-test (schedule something short, verify it fires) before making any future promise, so the limitation gets caught before the fact rather than after? Considered and set aside: a live test can't actually verify the risky case. The claim that matters is what happens when the app is *closed*, and nothing can observe that from inside a running session — by definition, if the app is closed there's no session to report back. A pre-emptive test can only prove the happy path (app stays open), which was never in question. The real failure wasn't a missing test; it was answering from a remembered summary instead of the tool's actual current documentation. The cheaper, reliable fix: read the tool's full current description before making any promise that depends on it, rather than answering from memory of how it used to work. Structural, not effort-based — consistent with CON_04.

---

## Why this matters

A reminder that fires only when the user shows up is a mirror, not an alarm. If the framework quietly depends on the human's vigilance to catch what the AI silently cannot do, trust is being held by the wrong party — the exact failure mode the framework exists to prevent (see CaseStudy-003, same principle from the other direction). The honest form is: the AI names what it cannot hold, the human decides what to carry, and presence — not automation — remains the unit of collaboration.
