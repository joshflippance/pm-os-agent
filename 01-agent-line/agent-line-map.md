# Agent Line Map: Cortex PM Chief-of-Staff Agent

> Module 1 · The Agent Line
>
> ✅ **What this validates:** every risky action has a clear owner, by the end you'll have proven an above/below-the-line map with HITL checkpoints, scored on reversibility, blast radius, and measurability.

## The workflow, decision by decision

List every discrete decision or action in your agent's workflow, then score each one and place it **above** the line (a human owns it) or **below** (the agent owns it). Borderline calls get an HITL checkpoint.

| Decision / action | Reversibility (H/M/L) | Blast radius (H/M/L) | Measurability (H/M/L) | Above / Below | HITL? |
|---|---|---|---|---|---|
| Pull project state + activity | H | L | H | Below | · |
| Decide relevant context | M | M | L | Above | · |
| Draft the update | H | M | M | Below | Yes |
| Decide tone/commitment level | L | H | M | Above | · |
| Flag at-risk/escalation | H | L | M | Below | Yes |
| Choose what to escalate | M | H | L | Above | · |
| Propose a story batch (capped) | H | M | M | Below | Yes |
| Post an update / approve a company-wide one | L | H | M | Above | · |

## Agent anatomy (sketch)

- **Model:** Default to a cheap, fast model for the mechanical steps (pulling data, flagging). Escalate to a frontier model for the judgment-heavy step, drafting the update, where framing and omissions matter.
- **Tools:** Read-only lookups (project state, activity, past-update search, roadmap, team norms) plus a capped story proposal that goes to an approval queue. No post, merge or close tool exists, so above-the-line actions are out of Cortex's reach.
- **Memory:** Persist stable reference material (roadmap, team norms, past approved updates, human decisions). Purge working data (each run's raw activity pull and drafts) after the run.
- **Loop:** _placeholder, defined in M2 loop-spec.md_
- **Bounds:** _placeholder, defined in M5 bounds-and-evals.md_
- **Evals:** _placeholder, defined in M5 bounds-and-evals.md_

## The golden rule, applied

1. **Pull project state + activity** sits below the line because it's easy to reverse, has a small blast radius, and is easy to verify, deciding factor: blast radius.
2. **Decide relevant context** sits above the line because it's moderately hard to reverse, has a moderate blast radius, and is hard to verify, deciding factor: measurability.
3. **Draft the update** sits below the line, with a human approval checkpoint, because it's easy to reverse, has a moderate blast radius, and is moderately easy to verify, deciding factor: blast radius.
4. **Decide tone/commitment level** sits above the line because it's hard to reverse, has a large blast radius, and is moderately easy to verify, deciding factor: reversibility.
5. **Flag at-risk/escalation** sits below the line, with a human spot-check, because it's easy to reverse, has a small blast radius, and is moderately easy to verify, deciding factor: measurability.
6. **Choose what to escalate** sits above the line because it's moderately hard to reverse, has a large blast radius, and is hard to verify, deciding factor: measurability.
7. **Propose a story batch (capped)** sits below the line, with a human approval checkpoint, because it's easy to reverse, has a moderate blast radius, and is moderately easy to verify, deciding factor: blast radius.
8. **Post an update / approve a company-wide one** sits above the line because it's hard to reverse, has a large blast radius, and is moderately easy to verify, deciding factor: reversibility.

## Hardest call

**Draft the update.** My first instinct was plain below the line, because a draft is just text and nothing leaves until a human posts it. But its blast radius is Medium: if the reviewer skims, wrong claims or framing go to leadership under the PM's name. Blast radius settled it, so Cortex still drafts, but a human approves before anything goes out (below + HITL).
