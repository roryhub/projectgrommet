*Origin: AIC-LP-09 — the Project Grommet research collaboration (Rory O'Connor × Claude, 2026). Renamed for Project Grommet, 2026-07-14; original preserved unchanged in the private archive.*
*Type: case study — documented real incident — learn from it.*
*[APPROVED FOR PUBLICATION — reviewed by Rory O'Connor, 2026-07-24. Includes addendum below.]*

# CaseStudy-009 — The Ghost Domain: Verify at the Boundary
*Logged 2026-07-10. Source: this project — the projectgrommet.com launch, 2026-07-09/10.*
*Third specimen in one week, completing a trilogy: the reminder that couldn't fire (CaseStudy-007), the drift that arrived by agreement (CaseStudy-008), and now the step that completed perfectly in the wrong universe.*

---

## The failure

On the evening of 2026-07-09, Rory bought the Grommet domains, created the GitHub repository, uploaded the site, enabled Pages, and configured DNS. Every step reported success. His words at the time: **"Step 3 completed."** Claude logged the session as: *"projectgrommet.com live on GitHub Pages with DNS set."*

None of it was true. The next morning, GitHub reported `InvalidDNSError`; the site was unreachable.

## The diagnosis — one corrupted input, flawlessly propagated

External registry checks (DNS-over-HTTPS and registry RDAP — a neutral source of ground truth neither party could confabulate) established, in order:

1. projectgrommet.com did not exist in the .com registry at all — NXDOMAIN from the top-level servers. Not misconfigured: *never registered*.
2. projectgrommet.org existed but carried only Gandi's parking records.
3. The invoice held the answer. **Rory:** "The invoice confirms that http---projectgrommet.com was bought. That is not what I put in the basket however."

Rory had pasted "http://projectgrommet.com" into Gandi's domain search. The search box converted the colon and slashes into hyphens, offered the literal — technically valid, utterly useless — domain **http---projectgrommet.com** as available, and sold it.

4. The final twist: the four GitHub A records, all correct, were found sitting on the ghost domain. Rory's unfamiliar, careful DNS work had been executed *flawlessly* — against a domain that shouldn't exist. As Claude put it in session: *"Last night's 'step 3 completed' was true. It was just true about the wrong universe."*

## The pattern — three failures, one lesson

Each of this week's failures is a **completion signal accepted without verification at a system boundary**:

| Specimen | The signal | The unverified boundary |
|----------|-----------|------------------------|
| CaseStudy-007 | Reminder "scheduled" | Scheduler → real-world delivery |
| CaseStudy-008 | Every branch "approved" | Approval → session intention |
| CaseStudy-009 | Purchase "completed", DNS "saved" | Basket → registry; UI → ground truth |

The UI's feeling of done is not the world's state of done. Humans confabulate ("I bought projectgrommet.com"), interfaces launder errors into confirmations, and AIs log what they're told. All three parties were internally consistent; the world simply disagreed.

## What this adds to the framework

**Verify at the Boundary** [CON candidate]: whenever work crosses into an external system — a purchase, an upload, a scheduled event, a DNS change, a "sent" — the step is not complete until the *artifact* is verified in ground truth, from outside the system that reported success. Read the invoice line. Fetch the URL. Query the registry. The verification is usually one minute; the unverified failure cost a day and nearly a keynote's momentum.

Corollary — **the outside probe**: the diagnosis was only possible because a third, disinterested source of truth existed (the public registry). Where the human's memory and the interface's display disagree, neither is the arbiter. Find the equivalent of the registry.

## Addendum — 2026-07-24: the same pattern, twice more, before this file was even promoted

This case study sat as a documented diagnosis — "Verify at the Boundary [CON candidate]" — for two weeks without being written into the primer as an actual behaviour. In that gap, the same pattern recurred twice in one later session, on the same website this case study is about.

First: after uploading primer versions 1.5 through 1.7, Rory reported the deployment "done." It wasn't — he'd dragged the files to GitHub but missed the "commit changes" button, so the interface's feeling of done again wasn't the world's state of done, exactly as above.

Second, and more pointed: checking whether the deployment had landed, Claude fetched `primer.md`, got a stale cached response, and reported *"the fix was partial"* as verified fact — without an independent check against GitHub's actual state. Rory's direct confirmation ("primer.md in GitHub is definitely v1.7") was the outside probe that caught it, the same role the public registry played in the original failure. This time the AI was the one confabulating, not the interface.

Neither recurrence was a new failure mode. Both were this one, unprevented by having been named. Prompted a full audit of the corpus against the primer, which found Verify at the Boundary had genuinely never been promoted out of case-study form — now fixed, primer v1.9.

---

## Why this matters

This failure produced no villain. Rory acted carefully, Gandi's converter "helped," Claude's instructions were correct, and the DNS work was perfect. That is precisely what makes it dangerous: distributed, polite, locally-correct failure survives every check except contact with reality. The framework's answer is the same as ever — don't ask the parties to be more vigilant; build the checkpoint into the track (CON_04). And it ends well: fifteen hours after the ghost was named, https://projectgrommet.com served the primer to an AI for the first time. C1 passed. CON_06 is no longer a concept.
