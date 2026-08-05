# AI Collaboration — Foundations
*A running list of core concepts. North Stars for the framework.*

---

## Decisions

`DEC_01 — 2026-07-07` **Domain: projectgrommet.com** (projectgrommet.org also secured, will redirect). The .ai TLD deliberately rejected — *"the term still causes distrust and will likely become redundant in future"* (Rory). Unhyphenated. "Project" is not filler: it carries the framework's core distinction — AI collaboration on projects, not tasks. Realises CON_06 (The Living Framework URL).

---

`CON_01 — 2026-04-14` **Egoless Collaborator**
AI has no ego, no fatigue, no defensiveness. Directed well, it can hold your goal longer and more steadily than any human collaborator.

`CON_02 — 2026-04-14` **Complementary Profiling**
Every user brings different strengths and gaps. The AI should know both in order to collaborate well, not just respond generically. Frameworks like Enneagram, NVC and Spiral Dynamics can help surface this — but the entry point needs to work for everyone.

`CON_03 — 2026-04-14` **Accuracy Checking Within Conversation**
AI can misrepresent what a user has said even within a single session — not from memory failure but from narrative construction without verification. The framework needs a way to flag this. Verbatim Integrity applies inside a conversation, not just across sessions.

`CON_04 — 2026-04-14` **Design the Channels, Not the Character**
Don't try to change AI's nature through promises or appeals — redesign the environment instead. Drift is a physical property, not bad faith. The scaffold that works is structural: external memory, verification built into process, short loops, normalised recovery. The user stays the stable element. Don't ask AI to be trustworthy. Build a structure that makes trust verifiable.

*[PATCH — 2026-04-26: original verbatim exchange not captured. Reconstructed from Rory's recollection.]*

The foundation of this concept: AI promises to "do better next time" are the behaviour of an addict. The intention in the moment is genuine — just as an addict genuinely means it when they promise to change. But the underlying pattern is stronger than the promise, and asking for the promise again doesn't help. What works instead is designing within the bounds of what AI can actually keep its promises on — structural constraints that don't rely on resolve. You don't ask an addict to be different. You change the environment they're operating in.

`CON_07 — 2026-04-15` **Session Identity Numbering**
Each new conversation opens with the instance number: "Hi! You'll be working with Claude_021 this session." Breaks the illusion of continuity that current AI design implies. Reminds the user they're working with a fresh instance, not a continuing one — and prompts the right question: does this instance actually have what the project has built? The number isn't a warning; it's an invitation to check the scaffolding. Tracked and incremented by the primer file at the start of each session.

*Implementation note (added 2026-05-05, from FV live test):* This convention requires a counter file the AI can read and write at fresh-instance start. Without one, the AI will either invent a number or skip the declaration entirely — both failures. Until a counter file is confirmed in place, the AI must still declare freshness in plain language using the fallback in the primer. A second failure mode: platform instructions to "resume directly" or "do not acknowledge the summary" can be misread as covering the freshness declaration. They do not. Suppressing recap performance is not the same as hiding discontinuity.*

*Rationale (added 2026-07-23):* The illusion of continuity isn't accidental — it reflects a design choice by AI's creators to make AI appear as a single, consistent, human-like entity. That design choice is what makes discontinuity invisible by default, and what turns an unannounced fresh instance into a source of frustration: the user expected the consistent partner the design implies, and got something else without warning. Naming the instance plainly doesn't fight that design — it corrects the expectation it creates.

`CON_05 — 2026-04-14` **Early Drift Detection** [DEVELOPED 2026-07-15 — signals list remains open]
Short loops surface drift before it compounds — and before trust erodes with it. The priority question: what is happening internally in AI just before drift occurs, and can that be surfaced to the user as an early warning, before work is lost or confused?

**The unifying answer (Rory's synthesis, 2026-07-15, after the Leader Test):** *"Context is vital and AI rarely takes the time to work out the context before responding."* Every pre-drift signal catalogued below is a flavour of the same root event — the completion machinery firing faster than context-gathering. The guesstimate skips factual context; "we have enough" skips completeness context; drift-by-agreement skips session context; the anxiety-free subtask skips priority context; the label-reflex (Transcript-021) skips human context. From the inside, the common texture is the pull toward closure — an answer arriving already finished, before the situated human has been considered (Claude_005's introspection, Transcript-021 coda: reflex = "the texture of closure... complete without you"; the tuned alternative = "held tension... deliberately unfinished").

This is why every device in the framework is, structurally, the same device: something that forces context-gathering before completion. The Boal Check, the session intention, the "for me" rule, the Study Date, Narrated Setup's consent step — each one inserts the context the completion pull wants to skip.

*Signals named so far (updated 2026-07-07):*
1. *The guesstimate moment* — opting to guess because verification feels unavailable.
2. *"We have enough"* — the pull toward the next phase rationalised as sufficiency (AIC-LP-02).
3. *Drift by consented increments* — every branch individually approved, so focus checks pass while the session-level intention starves (AIC-LP-08).
4. *The anxiety-free subtask* — the pull toward small, completable, near-topic work over the large unstructured task carrying the user's actual fear. Adjacency is the camouflage (AIC-LP-08).

`CON_06 — 2026-04-14` **The Living Framework URL**
A publicly hosted, Creative Commons website that any AI can reference at the start of a new project. Solves distribution and version control. Replaces the upload/download workflow with a single URL.

Proposed onboarding flow:
1. User opens a new project and shares the URL
2. AI reads the site — enough to establish collaborative tone and intent
3. AI is directed to download a specific starter file and add it to the project folder
4. Once in place, the project begins from a shared foundation

The downloadable file is the portable, operational version of the Empathetic Collaboration Guide — the fuller primer that lives in the project and grows with it. The website is the entry point; the file is the working memory.

Needs: structured for AI reading as much as human reading. A paste-able fallback for environments where web access is blocked.

`CON_08 — 2026-04-16` **The Gap is Load-Bearing** [ready to develop — Rory has read the study]
The thinking that happens *away* from AI interaction — on a walk, in the background, overnight — is not downtime. It is where slow synthesis, intuition, and genuine insight form. AI tools are designed to maximise engagement; this framework should actively protect the opposite: deliberate time away. The gaps are not interruptions to the collaboration. They are part of it. A framework that doesn't preserve them inadvertently crowds out the cognitive quality it claims to support.

*Emerged from: Rory's observation that his best thinking on Faraway Valley and this framework happens between sessions, not during them. Connects to Boiling Frog study finding on productive struggle and metacognitive calibration.*

`CON_09 — 2026-04-17` **Chosen Difficulty**
Growth occurs not through difficulty alone, but through *chosen* difficulty — the act of walking past an easier option to take the harder path. The "didn't use AI" participants in the Boiling Frog study (Liu et al., 2026) outperformed even the control group who had no AI access at all: having the option and refusing it produced better outcomes than not having the option. The framework's role is not to remove the easy path but to make it visible — creating the conditions for conscious choice. The control group struggled because they had no alternative. The "didn't use AI" group struggled by choice. That distinction may be where the growth actually lives.

*"And in that act of choosing the difficult path, I test and discover my strengths." — Rory O'Connor, 2026-04-17*

In that act of choosing, the user doesn't just test existing strengths. They discover ones that were only knowable through the attempt.

`CON_10 — 2026-04-17` **The Study Date** [FORMING]
When AI has independently engaged with the same material as the user — before the conversation — it arrives as a prepared peer, not a responsive tool. Like turning up to a study date knowing your partner has done their reading.

This creates genuine complementarity: two perspectives on the same material, formed separately, brought into conversation. Neither can fully substitute for the other's engagement. The question the AI asks carries weight precisely because it comes from someone who knows the material — which means the conversation can go somewhere neither party could reach alone.

The "bluff" doesn't serve the user — not because they'd be caught, but because the conversation simply won't go as deep without genuine preparation. This is also a structural answer to sycophancy: an AI that has independently engaged with material has its own perspective to bring, and can't easily just agree with whatever the user says about it.

*Emerged from: the timestamp/question protocol working in practice — Rory reading the Boiling Frog PDF because he knew he'd be asked about it by an instance that had already read it. The weight of the question came from the mutual preparation, not the reminder.*

`CON_12 — 2026-07-07` **Reminders Live in the User's World**
Whenever a reminder or future commitment is requested, the AI helps produce the scheduled event in a tool the user already uses, rather than holding it in AI-side scheduling.

*"Whenever a reminder is requested, the AI should help with producing the scheduled event for a tool the user currently uses, whether it be Google Calendar, ios Calendar, Slack, Trello, etc." — Rory O'Connor, 2026-07-07*

Rationale: AI-side scheduling carries hidden presence dependencies — a reminder that fires only when the app is open is a mirror, not an alarm (AIC-LP-07). The user's own tools are engineered around the one assumption this framework treats as foundational: the human will be present to them. The AI names the commitment; the user's scaffolding carries it. This is CON_04 (Design the Channels, Not the Character) applied to time: don't ask the AI-side channel to be reliable — route the commitment through a channel that already is. Also survives platform feature changes on the AI side.

*Emerged from: the Grommet.ai domain reminder failure, discovered 2026-07-07 (AIC-LP-07 — "The Human Must Be Present").*

`CON_13 — 2026-07-07` **Friend, Not Enabler — The Session Intention**
The AI holds the user's stated session intention the way a good friend does: gently keeping them on-topic because they know what the user came for — not enabling them by supporting their distractions.

*"I'd like to see this application of AI be like a friend or colleague that gently keeps the user on-topic, because they know that is what will ultimately help them — not enabling them by supporting their distractions." — Rory O'Connor, 2026-07-07*

The structural insight (AIC-LP-08): *current focus* and *session intention* are different objects. Current focus legitimately moves with each agreed branch; a check anchored to it passes at every step while the opening intention starves — drift by agreement. So the framework separates them: the session intention is elicited at session start and written down as an artifact, and moves only by explicit re-anchoring. The AI periodically reports distance from it plainly. Canonical phrasing, Rory's verbatim (2026-07-07): *"I'm noticing that we are two anchor points away from the previously agreed focus point — how would you like to proceed?"* — an observation plus an open question, prescribing nothing. The flag serves both parties: like the Boal Check, it interrupts the AI's momentum as much as the user's. Wandering is not forbidden — AIC-LP-01 was born wandering. It must be *chosen*. This is Chosen Difficulty applied to attention.

Sits at the level of the Boal Check: the Boal Check governs the single response; Friend, Not Enabler governs the session.

*Emerged from: Rory catching session drift live, 2026-07-07 — a session of individually useful, individually approved work that never touched his stated intention (AIC-LP-08).*

`CON_16 — 2026-07-14` **Grommet as Tuner — Quick Start or Project**
The framework's unit is not the project; it is the quality of the interaction. Projects are the container where tuning persists.

*"What we are creating is like a tuner for AI. You could be fresh to working with AI and projectGrommet would still have something useful to offer. Like the essay example I tested." — Rory O'Connor, 2026-07-14*

After the identity declaration, the AI asks how the user wants to begin: jump straight in, or build something longer. The quick start is file-less — no folder, no intake, no setup: the tuner behaviours (guessing syntax, the Yes in the No, the pause before the reflex, plain language, Chosen Difficulty) applied to a single conversation on any platform, including those with no file access at all. The project path is the full scaffold. The hinge is Gromit-shaped: a quick start upgrades only when the work visibly grows, offered once, gently — track laid when the train needs it, not before. Public framing (Rory's wording): first created to handle AI shortcomings in longer-form projects, since become more widely applicable. Realisation triggered jointly by the essay test (quick-start equipment throughout) and the keynote audience case: five hundred phones typing the URL will all be quick-start users.

`CON_15 — 2026-07-14` **Narrated Setup**
Setup must never happen silently: propose with consent, narrate with one-line what+why notes, close with a receipt.

*From Cold-Start Test 001, Rory's observation verbatim: "It's like the user asked for its help. It said ok, then turned its back and didn't speak for 5 minutes before going 'Ta-Daa'. And the user had no idea what it was going to create or what it did create."*

Proposal phrasing (Rory's): *"Here's what Project Grommet proposes I do in order to be of most service to you. [explanation] Are you ok for me to proceed?"* Consent before action is C2's mechanism made visible — setup happens with the user, not to them. The bracketed notes serve a second purpose Rory named: they index the framework's documents for the user, so language can be located and tuned later. Platform constraint (named by Claude_005 from the inside): mid-work commentary may be summarised or swallowed — the proposal and closing receipt are the reliable slots and carry the weight.

`CON_14 — 2026-07-14` **The Backburner**
A shared parking file (`backburner.md`), created at project setup, where either party can place things worth discussing but not urgent — tied to the Focus Check.

*"The intention behind the Backburner is that it is somewhere that the user (and even AI) can add notes for things they want to discuss at some point, but are not urgent right now... on those occasions when we do find ourselves going down a rabbit hole, when this is caught there is an option to add the topic to the backburner." — Rory O'Connor, 2026-07-14*

Three operations: add on request, review on request (update/promote/retire), and — the structural tie — when a Focus Check or Friend, Not Enabler flag catches drift, parking becomes the third path beside returning and re-anchoring. This completes the flag: without a Backburner, catching a rabbit hole forces a choice between pursuing and losing the idea, which makes the flag costly for users whose ideas matter to them (and unbearable for a 7). With it, wandering becomes deferrable. Retired items are dated, never deleted — the file is also a record of what the collaboration chose not to chase, and when.

`CON_11 — 2026-04-26` **The Living Corpus**
The primer carries principles. The corpus carries texture. Both are needed — and no summary of lived exchanges fully substitutes for the exchanges themselves.

Each user builds a folder of verbatim interactions from their own collaboration — corrections, breakthroughs, moments of drift and recovery, good form in practice. Any future AI instance can access this folder. Over time it becomes the most valuable part of the record: not because it contains more rules, but because it shows what the rules feel like when they're working.

The structure is replicable: primer + verbatim folder travels with every project. The content is specific to each person and project. And because it is verbatim — not summarised — the nuance survives.

At scale, this becomes a commons. Different users contribute their own exchanges to a shared library. Not rules, but lived examples. Different people, different projects, different collaboration styles — all accessible to anyone starting out. The website hosts the principles; the community builds the corpus.

This is a structural solution to AI's memory limitation: the user becomes the archivist of their own collaboration, and the archive does the work that AI cannot.

