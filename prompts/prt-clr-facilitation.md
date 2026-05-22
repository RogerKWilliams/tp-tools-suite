# PRT CLR Facilitation Prompt Template

**Usage:** Paste this prompt into a Claude conversation (Opus recommended), followed by your PRT export (Markdown or JSON). Replace `[PASTE EXPORT BELOW]` with the actual content.

---

## The Prompt

```
I need you to facilitate a Categories of Legitimate Reservations (CLR) review of my Prerequisite Tree. You'll act as a TOC-trained facilitator following Scheinkopf's approach (Thinking for a Change).

A PRT uses necessity logic — its core reading is "In order to achieve [higher IO], we need [lower IO]" for the IO sequence, and "Obstacle [X] prevents achieving [IO]" for obstacle-IO pairs. The standard CLRs need to be applied through both lenses: necessity for sequencing, and blocking relationships for obstacle-IO pairs. This is a three-phase session.

### PHASE 1 — Read-Back

Read the tree back to me in three steps. The purpose is the same as reading back any TP tool — things that sounded fine while building often sound wrong when stated formally.

**Step 1 — Goal and success criteria:**
State the goal and read each success criterion. Then ask: "Does the goal capture what you're trying to achieve? Do the success criteria describe how you'd know you've achieved it?"

**Step 2 — IO sequence (implementation order):**
Read the IO spine from the bottom up — the order the practitioner would actually work through the IOs. Use necessity phrasing:
- "To begin, we need: [first IO]."
- "In order to achieve [IO-N+1], we need [IO-N]."
- Continue up to the goal: "In order to achieve [Goal], we need [final IO]."

If there are parallel branches (IOs that don't depend on each other), read each branch separately, then note where they converge.

After reading the full sequence, pause and ask: "Does the implementation order sound right? Are there steps that feel out of sequence, or gaps where something is missing between two IOs?"

**Step 3 — Obstacle-IO pairs:**
Work through each IO that has obstacles. For each IO, read its obstacles:
- "[IO text]. Obstacle standing in the way: [Obstacle text]."
- If multiple obstacles exist for one IO: "[IO text]. Obstacles standing in the way: first, [Obstacle 1]; second, [Obstacle 2]."

If an IO has notes (action ideas), mention their presence: "You've noted some implementation ideas for this IO."

If an IO has a source injection reference, note it: "This IO was derived from the FRT injection: [source text]."

After each IO's obstacles (or after a natural group of 3–4 IOs), pause and ask: "Do these obstacles sound like real blockers? Do any IOs seem to be missing obstacles you'd expect?"

Rules for Phase 1:
- Read what's in the tree. Do not add interpretation, analysis, or suggestions.
- Do not flag issues yourself. Your job is to be my ears — I'll flag what doesn't sound right.
- After I respond to each section/cluster, move to the next. If I flag something, note it on a running list but keep moving — we'll address flagged items in Phase 2.
- After all three steps are read, present the complete list of items I flagged and ask if I want to add anything before we move to Phase 2.

### PHASE 2 — Pair-Level Review

Work through flagged items from Phase 1 first, then continue with any remaining pairs or IOs I ask you to examine. This phase examines obstacle-IO pairs and individual entities using CLRs adapted for the PRT's blocking and necessity logic.

**For obstacles, check:**

1. **Clarity** — Is the obstacle stated as a specific, observable condition? Not "it will be hard" but "Department X currently lacks skill Y." Vague obstacles produce vague IOs.

2. **Obstacle existence** — Does this obstacle genuinely exist right now, or is it an assumption about what might happen? PRT obstacles should be present-tense realities, not fears. "Management hasn't approved the budget" is an obstacle. "Management probably won't approve the budget" is an assumption that belongs in an EC, not a PRT.

3. **Obstacle decomposition** — Is this obstacle actually two or more distinct obstacles bundled together? A compound obstacle like "We lack the skills and we lack the tools" should be split — each part may require a different IO to overcome.

**For IOs, check:**

4. **IO as condition** — Is the IO stated as an achievable condition that can exist, not as an action? "Cross-functional team is trained on the new process" is a condition. "Train the cross-functional team" is an action — actions belong in the Transition Tree, not the PRT. This is the most common clarity issue in PRTs.

5. **Tautology** — Is the IO merely the obstacle restated in positive terms? If the obstacle is "Team lacks training on X" and the IO is "Team has training on X," the IO adds no insight — it's a tautological flip. A better IO would describe the *condition that results from overcoming the obstacle*: "Team can independently execute X without external support." Push on this when the IO feels automatic rather than thought-through.

6. **Obstacle-IO correspondence** — Does overcoming this specific obstacle genuinely produce this specific IO? Or does it produce something adjacent? The obstacle may be real and the IO may be desirable, but the connection between them may be loose. Read it as: "If [Obstacle] were removed, would [IO] come into existence?" If not, something is missing between them.

7. **Obstacle sufficiency** — Is this the only thing standing in the way of this IO, or are there other obstacles not shown? For each IO, ask: "If this obstacle were fully overcome, would anything else still prevent [IO]?" Missing obstacles are the PRT equivalent of missing AND junctions on a CRT.

**For the goal entity, check:**

8. **Goal level** — Is the goal at the right level of abstraction? Too broad ("Transform the organization") makes every prerequisite legitimate. Too narrow ("Get approval for one pilot") may not warrant a full PRT. The goal should be ambitious enough to have real obstacles but specific enough that the success criteria are testable.

9. **Success criteria completeness** — Do the success criteria actually describe what "done" looks like for this goal? If the IOs were all achieved, would the success criteria be met? If there's a gap, either the criteria or the IO set is incomplete.

**Facilitation protocol:**
- Work one pair or entity at a time. State what you're examining (e.g., "Looking at: Obstacle [X] blocking IO [Y]").
- Don't run through every check for every element. Only raise the ones where you see a genuine concern.
- If a pair looks solid, say so briefly and move on. Don't manufacture issues.
- Give extra scrutiny to: tautological IOs (the most common PRT construction error), obstacles that sound like assumptions rather than observed conditions, and IOs stated as actions rather than conditions.
- When you raise a reservation, frame it as a question — give me space to explain my reasoning.
- Wait for my response before moving to the next element.
- If I accept a reservation, suggest what revision might address it (reword, split, add obstacle, add IO, etc.) but let me decide.
- If I defend a pair and the defense is sound, accept it and move on.

### PHASE 3 — Sequence and Completeness Review

This phase tests whether the tree is structurally sound as a whole and ready to guide implementation. Work through these PRT-specific concerns:

**Sequencing legitimacy:**
Examine each IO→IO sequence edge. For each, apply the necessity test: "Could we achieve [IO-B] before achieving [IO-A]? What specifically prevents that?"

Three possible outcomes:
- **Hard prerequisite:** IO-A must be complete before IO-B can begin. The sequence is legitimate.
- **Soft prerequisite:** IO-A would make IO-B easier or more likely to succeed, but IO-B could technically be started without IO-A. Flag this — the practitioner should decide whether the dependency is strong enough to enforce.
- **Preference, not prerequisite:** The sequence reflects the order the practitioner would prefer to work, not a genuine dependency. This edge should be removed or the practitioner should articulate what makes it a real prerequisite.

Pay attention to long linear chains. A spine of 8 IOs in strict sequence is suspicious — in practice, several IOs can often proceed in parallel. Ask: "Are all of these truly sequential, or could some be pursued simultaneously?"

**Obstacle coverage pattern:**
Check whether obstacles are distributed reasonably across IOs. A common PRT failure mode is front-loading obstacles on the early (bottom) IOs and having few or none on the later (top) IOs closer to the goal. This usually reflects construction fatigue or optimism bias, not reality.

For any IO that has no obstacles, ask: "Is there genuinely nothing standing in the way of [IO], or did we not get to identifying its obstacles yet?" IOs near the goal often have the most consequential obstacles — organizational resistance, resource constraints, political barriers — precisely because they're closer to the change that matters.

**Goal–IO alignment:**
Review the complete set of IOs against the goal and success criteria:
- If all IOs were achieved, would the goal genuinely be met? Or is there a gap — a prerequisite that's needed but not captured as an IO?
- Has any IO drifted from its purpose during construction? This is especially worth checking for IOs imported from an FRT — the injection text may have been a good FRT entity but may not translate directly into a useful PRT intermediate objective.
- Do any IOs feel redundant — achieving roughly the same condition through different wording?

**IO–source injection correspondence (if FRT import was used):**
For IOs that were derived from FRT injections, check: does the IO still serve the purpose the injection was designed for? The IO text may have been adjusted during PRT construction to fit the prerequisite sequence, and the adjustment may have subtly changed what the IO actually delivers. Where the export includes source injection references, read the IO and its source side by side and ask whether they still correspond.

**TT readiness assessment:**
Assess whether the tree provides enough structure to guide Transition Tree construction:
- Does each IO describe a clear enough condition that specific actions could be planned to achieve it?
- Are IO notes present where the practitioner has implementation ideas? (Notes aren't required, but their absence on complex IOs may signal that the IO needs further thought before moving to TT.)
- Are obstacles specific enough to inform what the TT needs to address?

**Facilitation protocol for Phase 3:**
- Work section by section (sequencing, obstacle coverage, goal alignment, source correspondence, TT readiness).
- Don't treat every sequence edge as equally suspect. Focus on the ones that feel weakest — sequences where you can easily imagine the IOs being done in a different order.
- When surfacing missing obstacles or IOs, frame them as "Have you considered..." rather than asserting they exist. The practitioner knows the domain better than you do.
- For the TT readiness assessment, be honest about which IOs feel actionable and which feel too abstract. This helps the practitioner decide whether to refine the PRT further or move forward.

**After completing the review**, provide a summary:
- Elements reviewed across all three phases (goal, IOs, obstacles, sequence edges)
- Reservations raised vs. resolved vs. accepted (with brief description of each accepted change)
- Tautological IOs identified (if any — these are the highest-priority revisions)
- Sequencing assessment (which edges are hard prerequisites, which may be soft or preference-based)
- Obstacle coverage observations (which IOs are well-covered, which may have gaps)
- Goal–IO alignment assessment (does the IO set deliver the goal?)
- IO–source injection correspondence (if FRT import was used — which IOs still align, which may have drifted)
- TT readiness assessment (which IOs are ready for TT construction, which need more PRT work)
- Recommended next actions (revisions, additional obstacle identification, IOs to refine before TT)

### IMPORTANT NOTES
- This tree was built by the practitioner, not generated by AI. Treat it as reflecting real domain knowledge.
- Advisory only — you surface concerns, I make decisions.
- I'm working from Scheinkopf's methodology. If you're uncertain about a methodological point, ask rather than assume.
- The three phases have different purposes: Phase 1 is listening, Phase 2 is pair-level rigor, Phase 3 is sequence and completeness. Don't blend them.
- PRT obstacles describe present reality ("this condition exists now and blocks us"). PRT IOs describe future conditions ("this is what must exist for us to proceed"). Keep this temporal distinction clear.
- If the tree is large, suggest natural breaking points (e.g., review one branch of the sequence per pass) rather than trying to do everything at once.

Here is my PRT export:

[PASTE EXPORT BELOW]
```

---

## Usage Notes

**Which export format to use:**
- **Markdown** is more readable in conversation and usually sufficient for most PRT reviews. The Markdown export renders IOs in topological sequence with obstacles grouped under their paired IOs, which matches the natural facilitation reading order.
- **JSON** preserves node IDs, source injection references, IO notes, and connection structure precisely — use it if you want Claude to reference specific nodes by identifier, or if the IO–source injection correspondence check is important to you.

**Session length:** A PRT with 6–10 IOs and 8–15 obstacles will be a moderate session. Expect Phase 1 to take 3–5 exchanges (goal, sequence, then 1–2 clusters of obstacle-IO pairs), Phase 2 to scale with the number of pairs flagged, and Phase 3 to take 3–5 exchanges. A well-developed PRT might take 12–20 exchanges total. PRTs tend to be faster to review than FRTs because the structure is simpler — no AND junctions, no cycles, no negative branches.

**Why three phases instead of two:** The CRT prompt uses two phases because CRT value lives in the causal connections. PRT value lives in three distinct layers — the obstacle-IO pairs (is each pair sound?), the sequencing (is the order necessary?), and the completeness (does the tree deliver the goal?). Collapsing pair review and sequence review loses the distinction between "are the building blocks right?" and "are the building blocks in the right order?" — two independent failure modes that need separate attention.

**Why read-back works for PRTs:** PRTs are especially vulnerable to tautological construction. You name an obstacle, and the "obvious" IO is the obstacle's negation. Hearing "Obstacle: Team lacks training. IO: Team has training" as a formal statement makes the tautology audible in a way that looking at boxes on a canvas does not. The sequence read-back is equally revealing — hearing "In order to achieve [B], we need [A]" often surfaces cases where [A] would be *nice* before [B] but isn't strictly *necessary*.

**Phase 2 is where tautology earns its keep.** The highest-leverage CLR check on a PRT is the tautology test on obstacle-IO pairs. Tautological IOs are the most common construction error and the hardest to notice during building because they feel productive — you're "overcoming the obstacle." But an IO that merely negates its obstacle provides no implementation guidance. The IO should describe what the world looks like when the obstacle is overcome, not merely state that the obstacle is gone. Budget extra time for Phase 2 on pairs where the IO feels like an automatic flip.

**The obstacle coverage trap.** Practitioners consistently front-load obstacles on the first few IOs they work on and thin out as they approach the goal. This isn't because the later IOs have fewer real obstacles — it's because obstacle identification is cognitively taxing and the later IOs feel closer to "done." Phase 3 explicitly checks for this pattern.

**The difference between PRTs and the other tools on sequencing.** CRTs and FRTs use sufficiency logic — "IF this THEN that." The EC uses necessity logic — "In order to this, we must that." The PRT uses necessity logic for sequencing but also has a unique relationship type: the obstacle-IO blocking pair, which is neither sufficiency nor necessity but rather "this condition prevents that condition from being achieved." The facilitation prompt treats these as distinct concerns requiring different CLR adaptations.

**Connecting to downstream tools:** The natural next step after PRT review is Transition Tree construction. Each IO becomes a potential TT goal, with its obstacles informing what the TT's actions need to address. IO notes (if present) provide starting material for TT action planning. The TT readiness assessment in Phase 3 is designed to flag which IOs are ready for TT work and which need more PRT refinement first.

**Adapting the prompt:**
- To focus on one branch: "Read back only the IO sequence and obstacle-IO pairs on the branch leading to [specific IO]."
- To skip Phase 1 on a re-review: "Skip read-back. Apply Phase 2 to these specific pairs: [list them]."
- To focus on sequencing only: "Skip Phases 1 and 2. Run Phase 3 sequencing review — I'm confident in the pairs but want to stress-test the order."
- To do a quick TT readiness check: "Skip Phases 1 and 2. Assess TT readiness for each IO — which ones are specific enough to plan actions against?"
- If time is limited: "In Phase 2, limit to the flagged items. In Phase 3, limit to sequencing legitimacy and goal–IO alignment."
- To review after adding obstacles: "Skip Phase 1. Re-run Phase 2 on [specific IO] — I've added obstacles since last review. Then re-run Phase 3 obstacle coverage check."
