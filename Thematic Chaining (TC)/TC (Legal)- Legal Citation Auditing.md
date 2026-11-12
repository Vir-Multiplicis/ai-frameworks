# TC (Legal): Thematic Chaining for Legal Citation Auditing

**Version:** 1.1 · **Author:** Vir Multiplicis · **Updated:** November 2026
**License:** [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) · See the repository `LICENSE` file for details.

TC-Legal is a filter for testing whether legal authority actually supports the proposition it's cited for. A citation counts only if the authority **states the proposition, applies to the facts at issue, binds or persuades the relevant court, and remains good law.**

Misapplied, overextended, and fabricated case citations are among the most serious risks of AI-assisted legal work. TC-Legal adapts [TC-Core](https://github.com/Vir-Multiplicis/ai-frameworks/blob/main/Thematic%20Chaining%20%28TC%29/TC%20%28Core%29-%20Attribution%20and%20Source%20Auditing.md) to the specific ways legal citations go wrong. See also: [TC-Medical](https://github.com/Vir-Multiplicis/ai-frameworks/blob/main/Thematic%20Chaining%20%28TC%29/TC%20%28Medical%29-%20Medical%20Evidence%20Auditing.md)

---

## Contents

- [Premises](#premises)
- [Procedure](#procedure)
- [Verdicts](#verdicts)
- [Output Template](#output-template)
- [Workflow](#workflow)
- [Severity](#severity)
- [Requirements](#requirements)
- [Disclaimers](#disclaimers)

---

## Premises

1. **Work from the authority itself:** the opinion, statute, or regulation, not a summary, headnote, or AI paraphrase.
2. **Separate the holding from dicta,** and the majority from concurrences and dissents.
3. **Stop when support runs out.** If an authority can't be located or verified, stop work on that citation and report it to the operator. Don't rely on model memory for legal currency.
4. **Retrieve every citation.** Memory is never sufficient for a holding, statute, or regulation. A result is **Verified** only if the audit cites the authority's location and the citator check. For foreign-language authorities, name the translation used.

---

## Procedure

| Step | Action |
|---|---|
| 1. Decompose the proposition | Break it into its legal assertions. |
| 2. Retrieve the authority | If it can't be found, stop and report it. A citation that can't be located may be fabricated. |
| 3. Check the statement | Does the authority state the proposition, or only discuss the topic? |
| 4. Check which opinion | Majority, concurrence, dissent, or plurality? Identify which reasoning controls. |
| 5. Holding vs. dicta | Is the proposition necessary to the decision? |
| 6. Application to the facts | Does the reasoning extend to these facts, or does the claim stretch it? |
| 7. Check contradiction | Does the authority contain limits or qualifications the claim omits? |
| 8. Check the citation | Correct case, reporter, page, and pin cite? Check every quotation against the opinion's wording. |
| 9. Currency | Has the case been overruled, limited, distinguished, or questioned? Has the statute or regulation been amended or repealed? Use a citator (KeyCite, Shepard's). |
| 10. Authority | Binding or persuasive in the relevant jurisdiction and court? |
| 11. Publication status | Published and citable as precedent in this court? |
| 12. Procedural posture and standard of review | At what stage, and under what standard, was it decided? |
| 13. Conflicting authority | Settled law, or a split? Presenting one side of a split as settled is overstatement. |

---

## Verdicts

`supported` · `partially supported` · `overstated` · `overextended` · `dicta` · `minority or dissenting view` · `overruled` · `limited` · `not binding` · `unpublished` · `split authority` · `contradicted` · `unverifiable`

---

## Output Template

Report every audit in the format below. Do not summarize instead of filling in the table.

### Audit Summary

```
Document audited:
Jurisdiction and court:
Citations audited: [number]
Critical: [number] · Significant: [number] · Minor: [number]
Unverifiable: [number]
Citator used: [KeyCite / Shepard's / none]
```

### Citation Results

| # | Proposition | Authority cited | Steps failed | Verdict | Currency checked (citator and date) | Binding? | Tag | Severity | Recommended fix |
|---|---|---|---|---|---|---|---|---|---|
| | | | | | | | | | |

### Authorities Not Found

For each authority that couldn't be located: the proposition it supports, the citation as given, where it was searched for, and whether it may be fabricated.

### Rules

- One row per citation. List citations that pass as well as those that fail.
- **Steps failed** names the step number and name, e.g., "6. Application to the facts."
- **Currency checked** gives the citator and date. If no citator was available, enter "Not checked" and tag the result Unverified.
- **Tag** is Verified only if the authority itself was retrieved, its currency checked with a citator, and the audit states where it was checked; otherwise use Memory or Unverified.
- For Contradicted, Overstated, or Overextended verdicts, quote the authority's actual language.

---

## Workflow

### Stage 1: While drafting

Check each citation as it's added, and tag it:

| Tag | Meaning |
|---|---|
| **Verified** | Checked against the authority and a citator. |
| **Memory** | Recalled, not checked. |
| **Secondary** | Known only through another's summary or headnote. |
| **Unverified** | Not yet checked. |

### Stage 2: Before filing

- **Per-citation audit (preferred).** Run the full procedure on every citation. Nothing tagged Memory, Secondary, or Unverified is filed.
- **Whole-document audit.** A final pass for consistency between arguments and for conclusions that outrun the cited authority. Not a substitute for the per-citation audit, because errors hide among correct citations and verdicts become general impressions.

---

## Severity

| Level | Includes | Action |
|---|---|---|
| **Critical** | Fabricated or unlocatable case; contradicted or overruled holding; wrong citation; dissent or concurrence presented as the holding | Fix before filing |
| **Significant** | Overextended holding; dicta presented as holding; non-binding authority presented as binding; unacknowledged split | Fix or qualify |
| **Minor** | Citation format; pin cites that don't affect the proposition | Fix as convenient |

---

## Requirements

- **Citator access** for currency and authority checks. Without it, report citations as unverified.
- **Human review.** TC screens and flags; a licensed attorney remains responsible for every citation filed with a court.

---

## Disclaimers

- **Not legal advice.** TC tests whether citations support propositions; it doesn't determine legal strategy or outcomes.
- **Jurisdiction matters.** Rules on precedent, publication, and citation vary by court and jurisdiction.
- **An audit is only as good as access to the authorities and citators.** Where access fails, TC stops and reports.
- **Self-audit is the weakest form.** Model memory is especially unreliable for legal currency, which changes after training. Verdicts from recall count as Memory, never Verified.
