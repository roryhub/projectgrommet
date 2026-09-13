*Origin: AIC-LP-05 — the Project Grommet research collaboration (Rory O'Connor × Claude, 2026). Renamed for Project Grommet, 2026-07-14; original preserved unchanged in the private archive.*
*Type: case study — documented real incident — learn from it.*
*Read this as: the origin diagnosis for the subtractive-turn principle, and the design-specific texture (TRIZ, Slice & Dice) it's grounded in — not the current operational version. The prescription here ("bake in a question before generation") is sharpened and tested in Transcript-022, which names the specific question and shows it working live. Read that for the current best version; read this for the why and the fuller context.*
*[APPROVED FOR PUBLICATION — reviewed by Rory O'Connor, 2026-07-23.]*

# CaseStudy-005 — AI Bloat and the Subtractive Turn
*Logged 2026-05-14. Source: AI Collaboration project, session with Claude_003.*

---

**Rory:** I've noticed based on a discussion among boardgame designers that key to game design is cutting things away. Yet all the discussion [currently] about using AI shows that it results in bloat. So to be effective as a co-design partner, AI needs to learn to be subtractive.

**Claude:** Honest diagnosis from the inside, in order of depth.

The most surface cause is the training signal. AI is trained on feedback that rewards being helpful, and helpfulness almost always reads as addition — a new idea, an elaboration, an alternative. Cutting something rarely generates positive feedback. The bias toward generation is baked in at the reward level.

Underneath that is something more structural: AI is generatively oriented by architecture. Predicting what comes next is the fundamental operation. Subtraction requires holding a model of the whole and judging what's excess — a different cognitive operation entirely, and not the one the system defaults to.

Then there's what I'd call the wrong risk aversion. AI tends to avoid the risk of leaving something out — the user might need it — over the risk of including too much. But in design, surplus is often more damaging than absence. A confused player, a cluttered rulebook, a mechanic that doesn't earn its place. AI doesn't live with those consequences. It doesn't feel the weight of what it adds.

And finally — the one most relevant to your bloat observation from designers — AI tends toward completion. A deliberate gap, a removed element, an unanswered question left open: these feel like failures from the inside. Adding feels like progress. Removing feels like going backwards.

What this means for the framework: the structural nudge needs to come before generation, not after. Not "review what you produced and cut it" — AI will hedge and qualify rather than remove. But "before you add anything, ask what already exists that might do the job, or what could be removed instead."

**Rory:** I agree with what you're saying. Just like we have to interrupt the AI before it even says Hello, we need to interrupt it to challenge the designer and help them explore what they might subtract or reduce during the design process. This is where having the framework know how to implement tools like the subtractive questioning of TRIZ or the Slice & Dice technique can help.

It doesn't need to 'hold' everything, because, frankly the more I use AI the less hopeful I become about this approach working. What I think it can do is ask pertinent questions that we bake into the framework through both a philosophy of curiosity and with specific questions.

**Claude:** Strong alignment — and it clarifies something important about what the framework is actually for.

The model you're describing is: AI as a question engine, not a knowledge repository. Baked-in questions that interrupt the generative reflex and redirect toward subtraction. That's more honest about what AI can reliably do, and more consistent with everything else the framework says — the Boiling Frog finding, the Ethical Teaching Pause, CON_09. Hints, not answers. Questions, not solutions.

The techniques you mention all have a natural question form at their core. TRIZ trimming asks: "What does this element do, and could something already present do it instead?" The Evaporating Cloud asks: "What are the two things in conflict, what are you trying to preserve in each — and is the conflict actually real?" SCAMPER's Eliminate step asks simply: "What happens if this doesn't exist?" These aren't things the AI needs to hold as knowledge. They're question structures it can be given and apply.

The philosophy underneath them is the same: the designer already knows more than they think. The question is what's obscuring the core. Good questions surface that; they don't add more material on top.

---

### Why this matters for the framework

AI's generative bias is architectural, not behavioural. You cannot fix it by asking AI to "be more restrained." The interrupt must be structural — built into the protocol before generation begins, in the same way STOP in CLAUDE.md precedes the greeting.

The reframe: AI as question engine. The framework's role is to bake in the right questions — particularly subtractive ones — so the AI interrupts the designer's generative momentum rather than amplifying it.

This is also the honest answer to what AI can reliably do. It cannot hold a full design system in memory. It can hold a question and ask it well.

*Connects to: CON_04 (Design the Channels), CON_09 (Chosen Difficulty), Ethical Teaching Pause, the Boiling Frog study.*
