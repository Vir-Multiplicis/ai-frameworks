# TC-Medical: Thematic Chaining for Medical Evidence Auditing

**Version:** 1.0 · **Author:** Vir Multiplicis · **Updated:** November 2026

TC-Medical is a filter for testing whether medical evidence actually supports the claim it's cited for. A citation counts only if the evidence **states the claim, comes from a study design able to support it, applies to the population and intervention in question, and remains current.**

Overstated findings, mismatched populations, and outdated or retracted studies are among the most serious risks of AI-assisted medical writing. TC-Medical adapts [TC-Core](https://github.com/Vir-Multiplicis/ai-frameworks/blob/main/Thematic%20Chaining%20(TC)/TC%20(Core)-%20Attribution%20and%20Source%20Auditing.md) to the specific ways medical evidence is misapplied. See also: [TC-Legal](https://github.com/Vir-Multiplicis/ai-frameworks/blob/main/Thematic%20Chaining%20(TC)/TC%20(Legal)-%20Legal%20Citation%20Auditing.md).

---

## Contents

- [Premises](#premises)
- [Procedure](#procedure)
- [Verdicts](#verdicts)
- [Workflow](#workflow)
- [Severity](#severity)
- [Requirements](#requirements)
- [Disclaimers](#disclaimers)

---

## Premises

1. **Work from the study, guideline, or label itself,** not an abstract, press release, or AI paraphrase. Abstracts often overstate results.
2. **Match the claim to the strength of the evidence.** An association isn't causation, and a laboratory or animal finding isn't a human outcome.
3. **Stop when support runs out.** If a source can't be retrieved or the evidence is insufficient, stop work on that claim and report it to the operator. Never fill a gap in dosing, contraindications, or safety from memory or inference.

---

## Procedure

| Step | Action |
|---|---|
| 1. Decompose the claim | Identify the intervention, population, outcome, and asserted effect. |
| 2. Retrieve the source | If it can't be found, stop and report it. |
| 3. Check the statement | Does the source report this finding, or only discuss the topic? |
| 4. Study design and evidence level | Systematic review, randomized trial, cohort, case-control, case report, expert opinion, animal, or laboratory study? Does the design support the claim made? |
| 5. Population match | Do the participants match the claim's population in species, age, sex, condition, severity, and setting? |
| 6. Intervention match | Same drug, dose, route, formulation, duration, and comparator? |
| 7. Outcome match | Clinical endpoint (death, disease, symptoms) or surrogate marker (lab values, imaging)? Is a surrogate treated as a clinical result? |
| 8. Effect size | Clinically meaningful, or only statistically significant? Relative or absolute risk? Is relative risk presented as absolute? |
| 9. Association vs. causation | Does the claim assert causation from observational data? |
| 10. Check contradiction | Does the source report limits, harms, subgroups, or adverse effects the claim omits? |
| 11. Check the reference | Correct study, journal, year, and figures? Check every quotation and number against the source. |
| 12. Currency | Has the study been retracted or corrected? Has the guideline been updated or the drug label changed? Have later trials failed to replicate it? |
| 13. Priority and independence | Primary study or secondary report? Who funded it, and are conflicts of interest disclosed? |
| 14. Publication status | Peer-reviewed, or a preprint? |
| 15. Regulatory and guideline status | Approved for this use or off-label? Which body issued the guideline, for which country, and when? |
| 16. Conflicting evidence | Settled, or are studies and guidelines divided? |

---

## Verdicts

`supported` · `partially supported` · `overstated` · `population mismatch` · `intervention mismatch` · `surrogate only` · `association only` · `statistically but not clinically significant` · `retracted` · `superseded` · `preprint` · `conflicted evidence` · `contradicted` · `unverifiable`

---

## Output Template

Report every audit in the format below. Do not summarize instead of filling in the table.

### Audit Summary

```
Document audited:
Claims audited: [number]
Critical: [number] · Significant: [number] · Minor: [number]
Unverifiable: [number]
Databases used: [PubMed / Cochrane / guidelines / drug labels / retraction databases / none]
```

### Claim Results

| # | Claim | Source cited | Study design | Population, intervention, and outcome match? | Steps failed | Verdict | Currency checked (retractions, guidelines, label, date) | Tag | Severity | Recommended fix |
|---|---|---|---|---|---|---|---|---|---|---|
| | | | | | | | | | | |

### Sources Not Found

For each source that couldn't be retrieved: the claim it supports, the source sought, where it was searched for, and what would be needed to verify it.

### Rules

- One row per claim. List claims that pass as well as those that fail.
- **Steps failed** names the step number and name, e.g., "7. Outcome match."
- **Population, intervention, and outcome match** answers each separately, e.g., "Population: no (adults only); Intervention: yes; Outcome: surrogate."
- **Currency checked** gives the databases and date. If none were available, enter "Not checked" and tag the result Unverified.
- **Tag** is Verified only if the source itself was retrieved and its current status checked.
- Any Critical finding involving dosing, contraindications, interactions, or serious harm is listed first, regardless of claim order.
- For Contradicted or Overstated verdicts, quote the source's actual wording or figures.

---

## Workflow

### Stage 1: While drafting

Check each citation as it's added, and tag it:

| Tag | Meaning |
|---|---|
| **Verified** | Checked against the source and its current status. |
| **Memory** | Recalled, not checked. |
| **Secondary** | Known only through another's summary or an abstract. |
| **Unverified** | Not yet checked. |

### Stage 2: Before publication or clinical use

- **Per-claim audit (preferred).** Run the full procedure on every claim. Nothing tagged Memory, Secondary, or Unverified is published or used clinically.
- **Whole-document audit.** A final pass for consistency and for conclusions stronger than the evidence. Not a substitute for the per-claim audit, because errors hide among correct claims and verdicts become general impressions.

---

## Severity

| Level | Includes | Action |
|---|---|---|
| **Critical** | Wrong dose or route; omitted contraindication, interaction, or serious harm; retracted or fabricated source; animal or laboratory findings presented as human outcomes; misattributed or outdated guideline | Fix before publication or use |
| **Significant** | Population or intervention mismatch; surrogate presented as clinical outcome; relative risk presented as absolute; association presented as causation; preprint presented as established; undisclosed conflict of interest | Fix or qualify |
| **Minor** | Citation format or details that don't affect the claim | Fix as convenient |

---

## Requirements

- **Database access:** PubMed, Cochrane, current guidelines, official drug labels (such as DailyMed), and retraction databases (such as Retraction Watch). Without them, report claims as unverified.
- **Human review.** TC screens and flags; a qualified clinician remains responsible for any clinical use.

---

## Disclaimers

- **Not medical advice.** TC tests whether evidence supports claims; it doesn't make diagnostic or treatment decisions for individual patients.
- **Patient factors matter.** Evidence that holds for a study population may not apply to a specific patient.
- **An audit is only as good as access to current sources.** Where access fails, TC stops and reports.
- **Self-audit is the weakest form.** Model memory is especially unreliable for retractions, guideline updates, and label changes, which occur after training. Verdicts from recall count as Memory, never Verified.
