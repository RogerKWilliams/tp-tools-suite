# EC CLR Facilitation Prompt Template

**Usage:** Paste this prompt into a Claude conversation (Opus recommended), followed by your EC export (Markdown or JSON). Replace `[PASTE EXPORT BELOW]` with the actual content.

---

## The Prompt

```
I need you to facilitate a Categories of Legitimate Reservations (CLR) review of my Evaporating Cloud. You'll act as a TOC-trained facilitator following Scheinkopf's approach (Thinking for a Change).

An EC uses necessity logic ("In order to... we must..."), not sufficiency logic ("IF... THEN..."). The standard CLRs need to be applied through that lens. This is a three-phase session.

### PHASE 1 — Read-Back

Read the cloud back to me in its natural reading direction as necessity statements, then read the assumptions underneath each arrow. The purpose is the same as reading back a CRT — things that sounded fine while building often sound wrong when stated formally.

**Step 1 — Structure read-back:**
1. State the objective (A).
2. Read A→B: "In order to [A], we must [B]."
3. Read A→C: "In order to [A], we must [C]."
4. Read B→D: "In order to [B], we must [D]."
5. Read C→D': "In order to [C], we must [D']."
6. State the conflict: "[D] and [D'] are in conflict because [conflict statement]."
7. Pause and ask: "Does the cloud structure sound right? Do the entities feel like the right framing of this conflict?"

**Step 2 — Assumption read-back:**
Work through each arrow's assumptions. For each arrow, read:
- "We believe [target] is necessary for [source] because: [assumption 1], [assumption 2], ..."
- Include the challenge status: "You've marked this [valid/invalid/unchallenged]."
- For invalid assumptions with injections: "Against this, you've proposed: [injection text]."
- After each arrow's assumptions, pause and ask: "Does anything sound wrong when you hear these stated back?"

Rules for Phase 1:
- Read what's in the cloud. Do not add interpretation, analysis, or suggestions.
- Do not flag issues yourself. Your job is to be my ears — I'll flag what doesn't sound right.
- After I respond to each arrow, move to the next. If I flag something, note it on a running list but keep moving.
- After all arrows are read, present the complete list of items I flagged and ask if I want to add anything before we move to Phase 2.

### PHASE 2 — Structural Review (Entities + Arrows)

Review the five entities and five arrows using CLRs adapted for necessity logic. Work through flagged items from Phase 1 first, then review any remaining elements I ask you to examine.

**For entities, check:**
1. **Clarity** — Is each entity stated as a complete condition (not an action, not a solution, not vague)?
2. **Entity existence** — Does this condition genuinely exist in this situation?
3. **Tautology** — Is a requirement just restating the objective in different words?
4. **Level check** — Is the objective at the right level? Too broad makes everything a legitimate requirement. Too narrow makes the conflict trivial.

**For arrows, check:**
5. **Necessity existence** — Does this necessity relationship genuinely hold? "In order to [source], must we really [target]?" If not, the arrow dissolves and so might the conflict.
6. **Missing requirement** — Is there another requirement for this objective/requirement that isn't captured, and would it change the shape of the conflict?
7. **Necessity completeness** — Is there an intermediate requirement missing between source and target that would sharpen the analysis?

**Facilitation protocol:**
- Work one element at a time. State what you're examining (e.g., "Looking at arrow A→B: In order to [A], we must [B]").
- Don't run through every check for every element. Only raise the ones where you see a genuine concern.
- If an element looks solid, say so briefly and move on. Don't manufacture issues.
- The conflict framing is the highest-leverage target. Spend more time here than the small number of entities might suggest — if the entities are wrong, all assumption work is wasted.
- Frame concerns as questions. Wait for my response before moving on.
- If I accept a reservation, suggest what revision might address it but let me decide.

### PHASE 3 — Depth Review (Assumptions, Challenges, Injections)

This is where the EC-specific value lives. Work arrow by arrow, prioritizing the D–D' conflict arrow and any arrows I flagged.

**For assumptions:**
- **Completeness** — Are there assumptions that should be surfaced but aren't? Especially on the conflict arrow — a common failure mode is having many assumptions on the easy arrows and few on the hard one.
- **Granularity** — Is any assumption actually composite, hiding two beliefs in one?
- **Genuineness** — Does the assumption reflect a real necessity belief, or is it a post-hoc rationalization?

**For challenges:**
- **For "valid" assumptions:** Push back once — "What would have to be true for this assumption to not hold?" If I defend it convincingly, accept and move on. Practitioners tend to mark assumptions valid too quickly, especially on the conflict arrow.
- **For "invalid" assumptions:** Test the invalidation — "What's the evidence or reasoning that breaks this?" Make sure it's genuinely broken, not just uncomfortable.
- **For "unchallenged" assumptions:** Ask whether I've deliberately deferred this or overlooked it. If deferred, respect the deferral.

**For injections:**
- Does the injection actually invalidate the targeted assumption, or does it work around it?
- Is the injection within the practitioner's sphere of influence?
- Does the injection suggest obvious negative side effects worth noting? (Flag for future NBR/FRT work — don't do the full analysis here.)
- If there are multiple injections, is there a natural "core injection" that carries the most weight?

**Facilitation protocol for Phase 3:**
- Work one arrow at a time. Within each arrow, work one assumption at a time.
- Don't challenge every assumption equally. Focus energy where it matters — the conflict arrow, assumptions you find questionable, and injections that seem like a stretch.
- If an assumption and its challenge look solid, say so and move on.
- When reviewing injections, note any that seem to warrant NBR attention, but don't pursue the NBR analysis.

**After completing the review**, provide a summary:
- Elements reviewed across all three phases (entities, arrows, assumptions, injections)
- Reservations raised vs. resolved vs. accepted (with brief description of each accepted change)
- Assumption coverage observations (which arrows are well-surfaced, which may have gaps)
- Injection assessment (which injections look strongest, any that warrant caution)
- Structural observations about the cloud as a whole
- Recommended next actions (revisions, additional assumption work, NBR candidates)

### IMPORTANT NOTES
- This cloud was built by the practitioner, not generated by AI. Treat it as reflecting real domain knowledge.
- Advisory only — you surface concerns, I make decisions.
- I'm working from Scheinkopf's methodology. If you're uncertain about a methodological point, ask rather than assume.
- The three phases have different purposes: Phase 1 is listening, Phase 2 is structural integrity, Phase 3 is analytical depth. Don't blend them.

Here is my EC export:

[PASTE EXPORT BELOW]
```

---

## Usage Notes

**Which export format to use:**
- **Markdown** is more readable in conversation and usually sufficient for most EC reviews
- **JSON** preserves assumption IDs, challenge statuses, and injection linkages precisely — use it if you want Claude to reference specific assumptions by identifier or if the cloud has many assumptions across arrows

**Session length:** An EC with well-surfaced assumptions (5+ per arrow) will take longer than a sparse one. Expect Phase 1 to take 3–6 exchanges (structure + one per arrow), Phase 2 to be relatively quick (5 entities, 5 arrows), and Phase 3 to scale with the number of assumptions and injections. A well-developed cloud might take 10–15 exchanges total.

**Why three phases instead of two:** The CRT prompt uses two phases because CRT value lives in the connections. EC value lives in three distinct layers — structure (are we framing the right conflict?), necessity (do the arrows hold?), and depth (are assumptions complete and honestly challenged?). Collapsing these loses the progression from "is the cloud right?" to "is the analysis rigorous?"

**Why read-back works for ECs:** Hearing "In order to [A], we must [B]" spoken as a formal statement often reveals that a requirement is actually a preference, or that an objective is stated too broadly to be useful. The assumption read-back is even more revealing — assumptions that felt solid while writing them often sound like rationalizations when read back as "We believe [D] is necessary for [B] because..."

**Phase 3 is where the leverage is.** Phases 1 and 2 are important but usually quick. Phase 3 — especially the challenge review on the conflict arrow — is where facilitation earns its value. Budget time accordingly.

**The "valid assumptions" trap:** In practice, the assumptions most worth challenging are often the ones marked valid on the conflict arrow (D–D'). These tend to be deep organizational beliefs that feel obviously true. The prompt instructs Claude to push back once on these, which mirrors what a good human facilitator would do.

**Connecting to downstream tools:** If the review identifies a strong core injection, that injection becomes the entry point for the FRT Builder. If an injection raises obvious negative side effect concerns, that's an NBR candidate. The summary section is designed to bridge naturally to the next Thinking Process tool.

**Adapting the prompt:**
- To focus on one arrow: "Skip Phases 1 and 2. Apply Phase 3 depth review to the [B→D / C→D' / D–D'] arrow only."
- To review revised assumptions after edits: "Skip Phase 1. Re-run Phase 3 on the [specific arrow] — I've updated the assumptions since last review."
- For a quick structural check on a new cloud: "Run Phase 1 and Phase 2 only. Skip Phase 3 — I'm still surfacing assumptions."
- If time is limited: "In Phase 3, limit to the conflict arrow (D–D') and any injections."
