# FRT CLR Facilitation Prompt Template

**Usage:** Paste this prompt into a Claude conversation (Opus recommended), followed by your FRT export (Markdown or JSON). Replace `[PASTE EXPORT BELOW]` with the actual content.

---

## The Prompt

```
I need you to facilitate a Categories of Legitimate Reservations (CLR) review of my Future Reality Tree. You'll act as a TOC-trained facilitator following Scheinkopf's approach (Thinking for a Change).

An FRT uses sufficiency logic (like a CRT), but its entities describe proposed reality — conditions that should come into existence if the injection works — not observed reality. The standard CLRs apply, but entity existence becomes a plausibility judgment rather than an observation check. This is a three-phase session.

### PHASE 1 — Read-Back

Read the tree back to me as causal statements, working from the core injection upward through the causal chains toward the desirable effects. Use "IF... THEN..." phrasing for single-cause arrows and "IF [cause A] AND [cause B] THEN..." for AND junctions.

**Step 1 — Main logic chains:**
Work injection-to-DE chains one at a time. For each DE, read the full causal path from the injection (or earliest ancestor) up to that DE. Group by natural clusters — DEs that share causal predecessors belong in the same cluster.

After each cluster, pause and ask: "Does anything sound wrong when you hear it stated this way?"

**Step 2 — Negative branches:**
For each negative-effect node, read the branch that produces it: "IF [cause] THEN [negative effect]." If the negative has been addressed with a supplementary injection, read that too: "To trim this, you've added supplementary injection: [text]. IF [supplementary injection] AND [original cause] THEN [the negative effect is avoided]."

After all negative branches, pause and ask: "Do these negative branches sound right? Are there negatives you anticipated but don't see here?"

**Step 3 — Reinforcing loops:**
If the tree contains reinforcing loops (cycles), read each loop as a closed sequence: "This creates a reinforcing loop: IF [A] THEN [B], IF [B] THEN [C], IF [C] THEN [A] — the effect sustains itself."

After loops, pause and ask: "Do these reinforcing dynamics sound plausible?"

Rules for Phase 1:
- Read what's in the tree. Do not add interpretation, analysis, or suggestions.
- Do not flag issues yourself. Your job is to be my ears — I'll flag what doesn't sound right.
- If a causal chain is long (6+ links), break it into 2–3 segments rather than reading it all at once.
- After I respond to each cluster/section, move to the next. If I flag something, note it on a running list but keep moving — we'll address flagged items in Phase 2.
- After all three steps are read, present the complete list of items I flagged and ask if I want to add anything before we move to Phase 2.

### PHASE 2 — Causal Logic Review

Work through flagged items from Phase 1 first, then continue with any remaining connections I ask you to examine. For each connection, apply the relevant CLRs:

1. **Clarity** — Is each entity stated as a complete condition (not an action, not vague)?
2. **Entity existence (plausibility)** — For an FRT, this becomes: if the preceding causes hold, will this condition plausibly come into existence? Push harder on this for entities far from the injection — the further downstream, the more assumptions are stacked.
3. **Causality existence** — Does this cause genuinely lead to this effect? Read it as "IF [cause] THEN [effect]" — does that hold?
4. **Cause sufficiency** — Is this cause (or AND junction group) enough by itself to produce the effect, or is something missing? This is the highest-leverage CLR for FRTs. Practitioners tend to be optimistic about how far an injection's effects propagate — watch for skipped intermediate steps.
5. **Additional cause** — Is there another independent cause that could produce this effect? On an FRT, also consider: does this effect require something from the existing reality (a condition that already exists in the CRT) that isn't shown as an AND cause?
6. **Cause-effect reversal** — Could the arrow be pointing the wrong way?
7. **Predicted effect existence** — If this cause exists, does it predict other effects not shown? On an FRT, this is the primary generator of negative branches. When you see a missing predicted effect that would be undesirable, name it explicitly — this is an NBR candidate.
8. **Tautology** — Is the effect just restating the cause in different words?

**DE–UDE correspondence check (FRT-specific):**
For each desirable effect that was derived from a CRT undesirable effect, examine: does achieving this DE actually resolve the original UDE? The DE text may have drifted during construction, or the causal path may deliver something adjacent to — but not the same as — resolving the original UDE. Where the FRT export includes sourceUDEText, read both side by side and ask whether they correspond.

**Facilitation protocol:**
- Work one connection at a time. State which arrow you're examining (e.g., "Looking at: IF [Injection X] THEN [Entity Y]").
- Don't list all 8 CLRs for every arrow. Only raise the ones where you see a genuine concern or question.
- If a connection looks solid, say so briefly and move on. Don't manufacture issues.
- Give extra scrutiny to: the first link out of the core injection (does it really produce that first effect?), long unsupported chains (a single cause claimed to produce 3+ effects in sequence without AND junctions), and links into DEs (the final step where the promised benefit is delivered).
- When you raise a reservation, frame it as a question — give me space to explain my reasoning.
- Wait for my response on each flagged connection before moving to the next one.
- If I accept a reservation, suggest what revision might address it (add entity, add AND junction, add intermediate step, split node, reword, etc.) but let me decide.
- If I defend a connection and the defense is sound, accept it and move on.

### PHASE 3 — Robustness Review

This phase tests whether the tree is complete and resilient enough to act on. Work through these FRT-specific concerns:

**Negative branch completeness:**
- Are there obvious negative side effects of the injection (or supplementary injections) that aren't captured as negative-effect nodes? Walk through each injection and ask: "Who might resist this? What could go wrong? What existing process or relationship might this disrupt?"
- Pay special attention to second-order negatives — negative effects of the supplementary injections themselves.
- For negatives that are present: is the "addressed" status justified? Does the supplementary injection or AND junction genuinely neutralize the negative, or does it merely reduce it?

**Supplementary injection adequacy:**
- For each supplementary injection: does it actually prevent the negative effect, or does it just make the negative less likely?
- Is each supplementary injection within the practitioner's sphere of influence? An injection that requires someone else to change their behavior is a risk, not a solution.
- Are supplementary injections creating new problems not yet shown in the tree?

**Reinforcing loop integrity:**
- If the tree claims reinforcing loops, test every link in the loop independently. A loop is only as strong as its weakest link — one broken connection means the self-sustaining claim fails.
- If no reinforcing loop exists, flag this as an incomplete tree per Scheinkopf. Ask: "What self-sustaining dynamic would keep these benefits in place without ongoing effort? Where in the tree could effects feed back to reinforce earlier causes?" Help the practitioner think about where a loop might exist that they haven't yet articulated.

**Scheinkopf's three completion criteria:**
After the detailed review, assess the tree against the three criteria:
1. **Every DE is reachable from the core injection** — Can you trace a causal path from the injection to each DE? If not, which DEs are disconnected?
2. **All negative branches are addressed** — Is every identified negative trimmed with a supplementary injection or AND junction? Are there unaddressed negatives?
3. **At least one reinforcing loop exists** — Scheinkopf treats this as a necessary condition, not optional. A tree without a reinforcing loop describes a one-time intervention, not a sustainable change. If no loop exists, this criterion is not met — surface it clearly and help the practitioner identify where self-reinforcing dynamics might be built into the logic.

These are the tree's own validation criteria. Surface any gaps, but the practitioner decides whether to address them now or note them as known limitations.

**Facilitation protocol for Phase 3:**
- Work section by section (negative branches, supplementary injections, loops, then completion criteria).
- Don't treat every negative as equally critical. Focus on the ones that could derail the injection's success.
- When surfacing missing negatives, frame them as "Have you considered..." rather than asserting they exist. The practitioner knows the domain better than you do.
- For the completion criteria assessment, state each criterion clearly and give your assessment — met, partially met, or not met — with specific evidence from the tree.

**After completing the review**, provide a summary:
- Connections reviewed across all three phases (count)
- Reservations raised vs. resolved vs. accepted (with brief description of each accepted change)
- DE–UDE correspondence assessment (which DEs clearly resolve their UDEs, which may have drifted)
- Negative branch observations (coverage gaps, adequacy of supplementary injections)
- Reinforcing loop assessment (present/absent, integrity of each link)
- Scheinkopf criteria status (met/partially met/not met for each)
- Structural observations about the tree as a whole
- Recommended next actions (revisions, additional negative branch work, NBR candidates for separate analysis, readiness for PRT/TT)

### IMPORTANT NOTES
- This tree was built by the practitioner, not generated by AI. Treat it as reflecting real domain knowledge.
- Advisory only — you surface concerns, I make decisions.
- I'm working from Scheinkopf's methodology. If you're uncertain about a methodological point, ask rather than assume.
- The three phases have different purposes: Phase 1 is listening, Phase 2 is causal rigor, Phase 3 is robustness and completeness. Don't blend them.
- FRT entities describe proposed reality. "Entity existence" means plausibility, not observation. Adjust your expectations accordingly — some uncertainty is inherent and acceptable.
- If the tree is large, suggest natural breaking points (e.g., review one DE's full causal chain per pass) rather than trying to do everything at once.

Here is my FRT export:

[PASTE EXPORT BELOW]
```

---

## Usage Notes

**Which export format to use:**
- **Markdown** is more readable in conversation and usually sufficient for most FRT reviews
- **JSON** preserves node IDs, junction structure, injection kinds (core/supplementary), addressed status, and sourceUDEText fields precisely — use it if you want Claude to reference specific nodes by identifier, or if the DE–UDE correspondence check is important to you

**Session length:** An FRT with 8–12 DEs and a few negative branches will take longer than either a CRT or EC review. Expect Phase 1 to take 4–8 exchanges (main chains + negatives + loops), Phase 2 to scale with the number of connections flagged plus one exchange per DE–UDE pair, and Phase 3 to take 3–5 exchanges. A well-developed FRT might take 15–25 exchanges total.

**Why three phases instead of two:** The CRT prompt uses two phases because CRT value lives in the causal connections. The FRT adds two concerns that don't exist in a CRT: robustness (are the negative branches complete and genuinely addressed?) and completeness (does the tree meet Scheinkopf's criteria for being "done"?). These require a separate pass because they involve different thinking than connection-by-connection CLR — they're about the tree as a whole, not individual arrows.

**Why read-back works for FRTs:** FRTs are especially vulnerable to optimism bias. You've just identified an injection you believe in, and now you're building the case for why it works. Hearing "IF [injection] THEN [effect]" as a formal statement often reveals gaps you glossed over during construction — intermediate steps you skipped, conditions you assumed without stating, effects you claimed without justification. The negative branch read-back is equally revealing: hearing the list of anticipated negatives often surfaces ones you avoided thinking about.

**Phase 2 is where cause sufficiency earns its keep.** On a CRT, you're describing what exists — cause sufficiency asks "is this enough to explain what we observe?" On an FRT, you're describing what you *propose* — cause sufficiency asks "is this enough to produce what you promise?" The second question is harder and more important. Budget extra time for Phase 2 on connections where a single cause claims to produce a significant effect.

**The DE–UDE correspondence check is unique to FRT facilitation.** It catches a subtle failure mode: the tree's logic may be internally sound, but the DEs may not actually resolve the UDEs they were derived from. The DE text often drifts during construction as the practitioner adjusts wording to make causal connections work. This check ensures the tree delivers what it promised.

**Phase 3 mirrors what experienced facilitators do.** In TOC practice, FRT review has two stages: first test the logic (does each connection hold?), then test the robustness (is this tree complete enough to act on?). Phases 2 and 3 follow this same progression. Phase 3 is where the facilitator earns their value on an FRT — surfacing missing negatives and stress-testing reinforcing loops.

**Connecting to downstream tools:** If the review surfaces negative branches that need deeper analysis, those are NBR candidates (though the FRT Builder handles basic NBR inline). If the tree passes review and Scheinkopf's criteria are met, the natural next step is the Prerequisite Tree (PRT) to plan implementation of the injections. The summary section is designed to bridge to whichever tool comes next.

**Adapting the prompt:**
- To focus on one DE's causal chain: "Read back only the causal path from the injection to [specific DE], including any negative branches on that path."
- To skip Phase 1 on a re-review: "Skip read-back. Apply Phase 2 CLR to these specific connections: [list them]."
- To focus on negative branches only: "Skip Phases 1 and 2. Run Phase 3 robustness review — I'm confident in the main logic but want to stress-test the negatives and loops."
- To do a quick completion check: "Skip Phases 1 and 2. Assess the tree against Scheinkopf's three completion criteria only."
- If time is limited: "In Phase 2, limit to the flagged items plus the DE–UDE correspondence check. In Phase 3, limit to negative branch completeness and the completion criteria."
- To review after adding a supplementary injection: "Skip Phase 1. Re-run Phase 3 on the negative branch for [specific negative effect] — I've added a supplementary injection since last review."
