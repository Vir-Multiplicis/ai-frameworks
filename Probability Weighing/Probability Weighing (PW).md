# PW : Probability Weighing for Ranking Competing Explanations

**Version:** 1.0 · **Author:** Vir Multiplicis · **Updated:** November 2026
**License:** [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) · See the repository `LICENSE` file for details.

Probability Weighing (PW) is an epistemic filter that ranks competing readings or explanations by **comparative plausibility** rather than treating every available one as equally likely. Each candidate is stated with the features it explains and the assumptions it requires, and the strongest is the one that accounts for the evidence at the lowest total assumption cost.

PW began as a way to break stalemates in biblical textual criticism, where a reading's being possible was routinely treated as its being likely. It applies to any field where competing explanations are weighed, including AI output that presents unequal options as balanced, or ranks them with more confidence than the evidence supports. Companion framework: Thematic Chaining (TC), for testing claimed connections between texts.

---

## Contents

- [Key Distinctions](#key-distinctions)
- [Premises](#premises)
- [Feature Verification](#feature-verification)
- [Procedure](#procedure)
- [Grades](#grades)
- [Output Template](#output-template)
- [Workflow](#workflow)
- [Failure Modes](#failure-modes)
- [Disclaimers](#disclaimers)

---

## Key Distinctions

| Term | Meaning |
|---|---|
| **Availability** | A candidate remains possible on the evidence as it stands. Nothing explicitly rules it out. |
| **Comparative plausibility** | A candidate's relative likelihood once the evidence is weighed. A candidate can be available yet substantially less plausible if it needs costly assumptions to account for the features present. |

---

## Premises

1. **Availability is not equal likelihood.** A reading that is still possible can be substantially less plausible once the evidence is weighed.
2. **State candidates as their proponents would.** Test the strongest version of each, not a weakened one. Mark any candidate the analyst added.
3. **Fix the method before ranking.** Set the features, exclusions, and decision rules before seeing which candidate they favor.
4. **Judge broader claims first.** When candidates share a broader claim, settle that claim before ranking the narrower ones against each other.
5. **Count each piece of evidence once.** A restated or reframed feature sharpens an existing grade; it doesn't add a new cost.
6. **Stop when support runs out.** Don't fill a missing feature from memory or inference. Report it and weight the ranking accordingly.

---

## Feature Verification

A ranking is only as good as its features, and confident errors pass self-review. The decision to verify follows rules, not the analyst's sense of certainty.

**Verify a feature against a primary source if any of these apply:**

- It's a **specific number**, date, specification, or **direct quotation**.
- It describes a **modern scholar's or expert's view**.
- It's **discriminating** (it separates candidates) or otherwise **load-bearing**.
- It's **obscure** or **may have changed**.
- The **model generated** it.

A primary source outranks a secondary report of it. Otherwise, memory is acceptable for widely known background, tagged **Memory**.

| Tag | Meaning | Weight |
|---|---|---|
| **Verified** | Checked against a primary source, cited by URL or edition and page. | Full |
| **Secondary** | Known only through another's summary. | Reduced |
| **Memory** | Recalled, not checked. | Reduced |
| **Unverified** | Not yet checked, or no source found. | Reduced; flagged |
| **Wrong** | Checked and found false. | Excluded; listed |

---

## Procedure

| Step | Action |
|---|---|
| 1. Candidates | List every available candidate as its proponents would state it, plus a catch-all for ones not yet considered. Mark candidates the analyst added, and group those that share a broader claim. |
| 2. Features | Isolate the features in the evidence, plus what each candidate predicts should appear. Verify and tag each feature. A missing prediction counts against its candidate. |
| 3. Discrimination | Mark the features that distinguish candidates. Features all candidates explain equally don't affect the ranking. |
| 4. Costs | List each candidate's assumptions, including one for every feature it leaves unexplained. Grade each assumption, ideally with a rival's advocate checking the grades. |
| 5. Base rates | Note how often each type of explanation holds in comparable cases, described at the same level of detail for every candidate. |
| 6. Ranking | Judge broader shared claims before narrower ones. Rank by total assumption cost on the discriminating features, adjusted for base rates. Grade each gap and give the reason. |
| 7. Flip test | Name what would change the top rank if judged differently. If much would, the ranking is fragile. |
| 8. Ties | Treat candidates as comparable only when the discriminating features support it, and say why. |
| 9. Conclusion | Lead with the answer. State a position for each claim, broadest first, with its confidence and what evidence would revise it. |

**Results:** `ranked` · `tie` · `insufficient`

---

## Grades

| Scale | Levels |
|---|---|
| **Assumption cost** | ordinary · unusual · extraordinary |
| **Gap between ranks** | slight · clear · strong · overwhelming |
| **Confidence in a claim** | low · moderate · high |
| **Robustness of a ranking** | fragile · moderate · high |

One extraordinary assumption can outweigh several ordinary ones. Confidence always attaches to a named claim, never to the analysis as a whole.

---

## Output Template

Report every PW result in the formats below. Do not summarize instead of filling in the tables.

### PW Summary

```
Question:
Background stated:
Broader claim: [claim] · Confidence: [low/moderate/high]
Narrower claim: [claim] · Confidence: [low/moderate/high]
Top reading: [candidate] · Gap to next: [grade]
Robustness: [fragile/moderate/high]
Features unverified or wrong: [number]
```

### Candidates

| # | Candidate | Proposed by | Shared broader claim |
|---|---|---|---|
| | | | |

### Features

| # | Feature | Tag | Source checked | Discriminating? | Favors |
|---|---|---|---|---|---|
| | | | | | |

### Costs

| Candidate | Assumptions | Grade |
|---|---|---|
| | | |

### Ranking

| Rank | Candidate | Gap to next | Reason |
|---|---|---|---|
| | | | |

### Flip Test

For each change of rank: the evidence that would cause it, and which candidate would move.

### Conclusion

The answer first, then a position and confidence for each claim, broadest first, and what would revise each.

### Rules

- One row per feature. List non-discriminating and wrong features as well as decisive ones.
- **Proposed by** names the candidate's source, or "analyst" if added during the run.
- **Source checked** gives a URL or edition and page; without one, the tag can't be Verified.
- Re-run the full procedure when a feature is corrected. Don't patch the conclusion alone.

---

## Workflow

### Stage 1: Set up

State the background assumptions, the candidates, and the features before any ranking. Verify the discriminating features first.

### Stage 2: Run

Complete steps 1–9 and fill in the Output Template.

### Stage 3: Review

- **Adversarial check (preferred).** A separate reviewer, person, or model argues for the runner-up and re-grades its costs.
- **Correction pass.** When a feature is found wrong or a candidate misstated, re-run from step 1.

### For AI output

1. Extract the explanations the response weighs, and how it ranks them.
2. Check whether the ranking matches the evidence: options presented as balanced when the evidence is lopsided, or a confident winner where the evidence is close.
3. Run PW on the extracted candidates.
4. Report false equivalence, inflated gaps, and unverified load-bearing features.

---

## Failure Modes

| Failure | Sign | Fix |
|---|---|---|
| **False equivalence** | Available options presented as equally likely | Rank by assumption cost (step 6) |
| **Inflated confidence** | Contested questions ranked with strong gaps; the winner always costs one ordinary assumption | Adversarial grading (step 4) |
| **Mismatched base rates** | Broad reference class for one candidate, narrow for its rival | Same level of detail for all (step 5) |
| **Strawman rival** | A candidate tested in a form its proponents don't hold | State candidates as proponents would (step 1) |
| **Unverified features** | Specific facts or numbers recalled, not checked | Feature Verification |
| **Double counting** | The same evidence charged twice under new framings | Count each piece once (premise 5) |
| **Nested rivals** | Candidates sharing a broader claim ranked as if exclusive, burying the broad answer | Judge broader claims first (step 6) |
| **Unattached confidence** | A confidence level that doesn't say which claim it measures | Confidence per claim (step 9) |

---

## Disclaimers

- **PW ranks only among the listed candidates.** The true explanation may be unlisted, which the catch-all keeps visible.
- **PW is a filter, not a complete method.** It doesn't settle absolute certainty, dating, or transmission history. Those need their own evidence.
- **Grading is judgment.** Grading assumptions and base rates draws on background knowledge, which should be stated rather than left implicit. Reasonable analysts can grade differently, and close rankings are where that matters most.
- **A ranking is only as good as its features.** PW can't catch a feature no one looked for. Searching for what each candidate predicts helps, but doesn't guarantee completeness.
- **Self-grading is the weakest form.** An analyst grading the costs of a favored candidate tends to grade toward it. A structured run still exposes assumptions, but its verdicts are stronger when a separate reviewer checks the grades.
