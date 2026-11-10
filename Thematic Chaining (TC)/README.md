# Thematic Chaining (TC)

**A framework for testing whether a source actually supports a claim, or only resembles it.**

**Version:** 1.0 · **Author:** Vir Multiplicis · **License:** CC BY 4.0

---

## The problem

LLMs are bad at citations in a specific way. The source is real, or looks real, the claim sounds right, and the source doesn't actually say it. Sometimes the source doesn't exist at all. In *Mata v. Avianca* (S.D.N.Y. 2023), lawyers were sanctioned for filing cases ChatGPT had invented outright, complete with realistic names, courts, and reporters.

Part of the reason is how AI finds sources. When an LLM cites something, it tends to pick whatever is most statistically similar to the claim: sources that share its wording, its topic, or its keywords. Similarity is a superficial way to link evidence to a claim. A source can match a claim closely in vocabulary and subject while never making the specific point the claim depends on. When the match is close but the support isn't there, the model may smooth over the gap by paraphrasing the source to fit, or by producing a citation that only looks real.

The underlying error is older than AI: treating resemblance as evidence of connection, and treating each added resemblance as strengthening the case. Shared keywords, similar phrasing, and plausible-looking references can all pass a quick check while nothing actually connects the claim to the source.

## The idea

TC counts a connection only if it holds for the whole **linked sequence** of ideas, not for isolated resemblances or shared keywords. Instead of asking how many details a claim and a source have in common, it asks:

- Does the source supply the **connections** between the pieces, or only the pieces?
- Did this source come **first**, or is it repeating an earlier one?
- Does anything in the source **contradict** the claim, or qualify it in ways the claim leaves out?
- Is the source still **current**, or has it been retracted, corrected, or superseded?

## Files

| File | Use it for |
|---|---|
| [TC (Core)](TC%20(Core)-%20Attribution%20and%20Source%20Auditing.md) | General attribution and source auditing. Start here. |
| [TC-Legal](TC%20(Legal)-%20Legal%20Citation%20Auditing.md) | Legal citations: holding vs. dicta, majority vs. dissent, binding authority, overruled cases, and splits. |
| [TC-Medical](TC%20(Medical)-%20Medical%20Evidence%20Auditing.md) | Medical evidence: study design, population and outcome match, surrogate endpoints, relative vs. absolute risk, and retractions. |

TC-Legal and TC-Medical are adaptations of TC (Core) for the specific ways citations go wrong in those fields.

## Two modes

| Mode | Question |
|---|---|
| **Attribution** | Which earlier text, if any, is the real source of a motif, allusion, or passage? |
| **Audit** | Does a cited source actually support the claim attached to it? |

Most users will want the **Audit** mode. The domain versions are audit-only.

## Quick start

1. Copy the contents of the file you need into a chat with Claude, ChatGPT, Gemini, or another LLM, or upload the file.
2. Turn web search on. TC depends on retrieving the actual sources.
3. Paste or upload the document you want checked.
4. Ask: **"Run a Mode 2 audit on this document."** For the legal or medical versions, ask the model to run the full procedure.

The model returns one row per claim, including claims that pass, with the steps each claim failed, a verdict, a severity level, and a recommended fix.

## How results are tagged

Every result is tagged by how it was checked:

| Tag | Meaning |
|---|---|
| **Verified** | The source itself was retrieved and checked. |
| **Memory** | Recalled by the model, not checked. |
| **Secondary** | Known only through someone else's summary. |
| **Unverified** | Not yet checked. |

A model checking its own output from memory never counts as Verified. The same training data that produced an error can also "confirm" it. If a source can't be retrieved, TC stops work on that claim and reports it instead of filling the gap.

## Limitations

- **TC is a filter, not a complete method.** It tests *what* a passage builds on, or whether a source supports a claim. Questions of date, language, and transmission need their own evidence.
- **Results depend on how the chain is defined.** State the chain before testing candidates, so the findings don't shape the definition.
- **An audit is only as good as access to the sources.** Without web search, database access, or (for legal work) a citator, most results will be tagged Memory or Unverified.
- **TC screens and flags.** For legal and medical use, a licensed attorney or qualified clinician remains responsible for the final work.
- **Long documents strain the output.** Models may start skipping rows on long documents, so audit one document at a time.

## Status and testing

TC is at **v1.0 and lightly tested**. Testers are welcome, especially:

- Runs across different models, with and without web search
- Seeded-error tests: take a document you know well, plant fabricated or overstated citations, and see what gets caught
- False positives: real, correct sources that TC wrongly flags
- Legal and medical professionals testing the domain versions on real work

Please report results in [Discussions](https://github.com/Vir-Multiplicis/ai-frameworks/discussions). Include the model used, whether search was on, the type of document, what was caught, what was missed, and any false flags.

## Background

TC began in biblical textual criticism, as a way to test proposed parallels between texts: when a later passage resembles several earlier sources, which one is the real source? The same problem shows up wherever resemblance is mistaken for connection, including AI hallucination detection, legal citation checking, medical evidence review, copyright, and prior art.

Introductory article: [*Validating Parallel Similarities and Source Citations Through Thematic Chaining*](https://medium.com/@socal21st.oc/validating-parallel-similarities-and-source-citations-through-thematic-chaining-bd510b5061c3) (Medium, November 2026).

## Relation to other frameworks in this repository

TC is a **standalone framework**. It is not part of Epistemic Lattice Tethering (ELT). It pairs well with **Adversarial Convergence (AC)**: AC disciplines how a model reasons, and TC checks the model's claims against sources.

## License and citation

Licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). See [CITATION.md](../CITATION.md) for attribution formats.

> **Thematic Chaining (TC)** by **Vir Multiplicis**, published in *AI Frameworks by Vir Multiplicis* under CC BY 4.0: [https://github.com/Vir-Multiplicis/ai-frameworks](https://github.com/Vir-Multiplicis/ai-frameworks)
