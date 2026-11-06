# TC-Core: Thematic Chaining for Attribution and Source Auditing

**Version:** 1.0 · **Author:** Vir Multiplicis · **Updated:** November 2026

Thematic Chaining (TC) is an epistemic filter for testing claimed connections between texts. A connection counts only if it holds for the whole **linked sequence** of ideas, not for isolated resemblances or shared keywords.

TC began as a way to test proposed parallels between 1 Enoch and the Book of Revelation. It applies to any field where resemblances are mistaken for sources, including AI hallucination detection. Domain versions: [TC-Legal](TC-Legal.md) · [TC-Medical](TC-Medical.md)

---

## Contents

- [Modes](#modes)
- [Premises](#premises)
- [Mode 1: Attribution](#mode-1-attribution)
- [Mode 2: Audit](#mode-2-audit)
- [Workflow](#workflow)
- [Severity](#severity)
- [Disclaimers](#disclaimers)

---

## Modes

| Mode | Question |
|---|---|
| **Attribution** | Which earlier text, if any, is the real source of a motif, allusion, or passage? |
| **Audit** | Does a cited source actually support the claim attached to it? |

---

## Premises

1. **State the chain first.** Define the chain from the passage alone before testing candidates, so the definition isn't shaped by any one source.
2. **Test in chronological order.** A link supplied by an earlier source doesn't count toward a later one.
3. **Compare usage, not just vocabulary.** Shared words can fit one source's senses, idioms, and associations better than another's.
4. **Work from the source itself,** not a summary or paraphrase. Reconstructed texts are hypotheses and must be justified first.
5. **Stop when support runs out.** If a source can't be retrieved or the evidence is insufficient, stop work on that claim and tell the operator what couldn't be found. Don't fill the gap from memory or inference.

---

## Mode 1: Attribution

| Step | Action |
|---|---|
| 1. Isolate the chain | Identify the linked motifs in the passage. |
| 2. List candidates | Include all plausible sources, including widely shared traditions. |
| 3. Check priority | Which candidate first supplies each link, by vocabulary *and* usage? |
| 4. Check contradiction | A candidate that conflicts with any link is excluded. |
| 5. Test the joins | Does the candidate supply the connections, or only separate pieces? |
| 6. Test the weight | Does the borrowing carry the passage, or is it a passing image? |
| 7. Compare economy | Prefer the candidate explaining the whole chain with the fewest added assumptions. |

**Results:** `best explanation` · `insufficient` · `excluded` · `shared tradition`

**Grades of evidence:** quotation > narrative allusion > framework > echo

---

## Mode 2: Audit

| Step | Action |
|---|---|
| 1. Decompose the claim | Break it into its assertions and their connections. |
| 2. Retrieve the source | If it can't be retrieved, stop and report it. |
| 3. Check each assertion | Is it stated, implied, or merely mentioned? |
| 4. Test the joins | Does the source make the connection, or only share keywords? |
| 5. Check contradiction | Include qualifications the claim omits. |
| 6. Check the reference | Is it the right passage? A true claim can carry a wrong citation. |
| 7. Check priority | Original or secondary? Trace to the earliest source. |
| 8. Check currency | Has a later source retracted, corrected, or superseded it? |
| 9. Test the weight | Is the point central to the source, or a passing remark? |

**Verdicts:** `supported` · `partially supported` · `overstated` · `keyword match only` · `contradicted` · `superseded` · `secondary` · `unverifiable`

---

## Workflow

### Stage 1: While drafting

Check each citation as it's added, and tag it:

| Tag | Meaning |
|---|---|
| **Verified** | Checked against the source. |
| **Memory** | Recalled, not checked. |
| **Secondary** | Known only through another's summary. |
| **Unverified** | Not yet checked. |

### Stage 2: Before publication

- **Per-claim audit (preferred).** Run Mode 2 on every citation and check every quotation against the source wording. Nothing tagged Memory, Secondary, or Unverified is published unless the text marks it as uncertain.
- **Whole-document audit.** Catches problems *between* claims: contradictory sections, a chart that no longer matches the text, or a conclusion stronger than its evidence. It's inferior as a substitute for the per-claim audit, because errors hide among correct claims and verdicts become general impressions. Use it as a final coherence pass after the per-claim audit, not instead of it.

### For AI output

1. Extract the claims, citations, and connections from the response.
2. Retrieve the sources.
3. Run Mode 2.
4. Remove contradicted claims, qualify weak ones, and report what couldn't be verified.

TC's distinctive checks for AI output are the **joins** test, which catches true facts linked by a connection no source makes, and the **priority** and **currency** tests, which catch errors of sequence, secondhand sourcing, and outdated sources.

---

## Severity

| Level | Includes | Action |
|---|---|---|
| **Critical** | Contradicted, superseded, or wrong reference | Fix before publishing |
| **Significant** | Overstated, unsupported, or secondary | Fix or qualify |
| **Minor** | Wording or dates that don't affect the argument | Fix as convenient |

---

## Disclaimers

- **TC is a filter, not a complete method.** It answers *what* a passage builds on, or whether a source supports a claim. Date (*when*), language (*in what form*), and transmission (*by what route*) need their own evidence, and TC depends on their answers.
- **Results depend on how the chain is defined.** State it before testing, so the findings don't shape the definition.
- **An audit is only as good as access to the sources.** Where a source can't be retrieved, TC stops and reports rather than verifying.
- **Self-audit is the weakest form.** A model checking its own output against its own memory can confirm its own errors, since the same training data may produce both the error and the "confirmation." A structured self-audit still catches some errors, because each step forces a specific question, but its verdicts count as Memory, not Verified. Verification needs retrieved sources, or at least a separate model or tool.
