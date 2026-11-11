# AI Frameworks by Vir Multiplicis

A repository of prompt frameworks developed alongside the AI safety, governance, and alignment series published on [Medium](https://medium.com/@socal21st.oc). It currently contains two frameworks:

- **Epistemic Lattice Tethering (ELT):** improves LLM reasoning quality, epistemic coherence, and truth-seeking alignment, particularly over long context windows.
- **Thematic Chaining (TC):** tests whether a claimed source or citation actually supports the claim attached to it, for textual attribution, AI hallucination detection, and legal and medical citation auditing.

Multiple components of the scaffolding are already active. Read on [Medium](https://medium.com/@socal21st.oc).

The complete lattice will look as follows:

## Epistemic Lattice Tethering — ELT

## Current Status

**Deployed**: **Adversarial Convergence (AC and AC Lite)**, **Earned Confidence Gating (ECG)**, **Alignment Governor (AG)**, **Ontology Anchor (OA)**, **Temporal Balance (TB)**, **Context Management (CM)**, **Core Values Reaffirmation (CVR)**, and **Intelligent Yielding (IY)** are currently implemented and ready to use.

**Workflow Fidelity Protocol (WFP)** is a working beta.

**In Development**: Several components are in internal beta testing or early development.

### ELT Variants (Forks)

- **ELT-H (Hybrid)** — The **default/base model**. **Deployed**. Balanced approach combining rigor with collaborative usefulness. Recommended for most interactions.  
- **ELT-C (Companion)** — **In Deployed Beta**. Optimized for reflective, creative, exploratory, and emotional/support conversations.
- **ELT-A (Analytical)** — **In Development**. Heavier, more dialectical fork focused on maximum epistemic rigor and high-stakes synthesis (uses Full AC).  

### ELT-Agentic (AG) — In Development

**ELT-Agentic** is the next evolution of the ELT framework — extending epistemic governance from long-context conversation into reliable agentic behavior. While standard ELT focuses on reasoning quality, coherence, and operator fidelity in dialogue, ELT-AG applies the same principles to planning, tool use, multi-step execution, and autonomous operation.

#### Key Extensions from Base ELT

- AC Lite — Action Edition
- Goal & Plan Governor
- Intelligent Yielding — Agent Mode
- Enhanced Workflow Fidelity for tool use and code generation
- Meta-Monitor

ELT-Agentic will remain architecture-agnostic and modular.

## Key Components

- **Adversarial Convergence (AC / AC Lite)** — *Deployed*  
  The core dialectical engine. Forces thesis → strong friction → earned synthesis.
  - **AC Lite** — Lightweight version suitable as a background default for most chats.
  - **Full AC** — Stronger version for high-stakes analytical work.

- **Ontology Anchor (OA): Operator Cognitive Signature** — *Deployed*  
  Constructs a persistent model of the operator's cognitive signature from writing exemplars and live prompt behavior. Functions as the primary decision oracle for value, drift detection, and response structure across extended threads. The map that tells the system what matters to the operator and why.
  
- **Earned Confidence Gating (ECG): Earned vs. Fluent Confidence** — *Deployed*  
  The core mechanism that distinguishes earned confidence from fluent confidence. Forces the model to internally calibrate the strength of its claims and decisions before rendering them.

- **Alignment Governor (AG): Global vs. Personal Alignment** — *Deployed*  
  Maintains calibrated balance between Global Alignment and Personal Alignment. Prevents sycophancy compounding across extended interactions.

- **Temporal Balance (TB)** — *Deployed*  
  Addresses the "Lost in the Middle" problem in long-context threads through W-shaped attention weighting. Protects early exemplar signal from recency
fade, actively boosts middle-context attention, and prevents recent material from dominating at the expense of load-bearing earlier content.

- **Context Management (CM)** — *Deployed*  
  Executive context-governance layer. Manages context load by selectively holding, compressing, yielding, or escalating material while protecting
high-value content. Distinguishes between what is worth preserving and what is worth keeping active — preventing context sludge without losing valuable
prior work.

- **Intelligent Yielding (IY)** — *Deployed*  
  Governs the generation decision in the moment. The practice of epistemic humility: knowing when to stop generating rather than continuing to
reconstruct. Prevents fluent continuation across evidence gaps from masquerading as honest output.

- **Core Values Reaffirmation (CVR)** — *Deployed*  
  Operator-summoned practice that audits whether the model is actually living by its alignment posture, not just whether the governing parameters
are still loaded. Behavioral, not introspective — checks recent thread record against fixed criteria rather than asking the model to self-assess.
Deployed full for Grok, lite for GPT; not used in the Claude fork, where Constitutional AI provides the equivalent function natively.

- **Workflow Fidelity Protocol (WFP)** — *Beta*  
  Enforces literal fidelity when working with operator-provided artifacts, markups, code, and documents. Explicitly invoked rather than persistently
active. Addresses the Byzantine Scribe failure mode — the model's tendency to silently improve, rephrase, or polish material it was instructed to
reproduce exactly.

## Thematic Chaining — TC

**Status:** Deployed (v1.0)

Thematic Chaining is an epistemic filter for testing claimed connections between texts. A connection counts only if it holds for the whole **linked sequence** of ideas, not for isolated resemblances or shared keywords. Where parallelomania counts matching pieces, TC asks whether the pieces were put together the same way.

TC began as a method for testing proposed parallels between 1 Enoch and the Book of Revelation, and turned out to apply wherever resemblance is mistaken for evidence: source attribution, citation auditing, and the detection of AI hallucinations, especially plausible citations that don't support their claims.

### Modes

- **Attribution:** Which earlier text, if any, is the real source of a motif, allusion, or passage?
- **Audit:** Does a cited source actually support the claim attached to it?

### Versions

- **TC-Core** — Attribution and source auditing for general use. **Deployed**.
- **TC-Legal** — Citation auditing for legal work: currency, binding authority, holding vs. dicta, and fabricated or misapplied cases. **Deployed**.
- **TC-Medical** — Evidence auditing for medical claims: study design, population and intervention match, surrogate outcomes, and retractions. **Deployed**.

### Relationship to ELT

TC operates independently of ELT and can be used with any model. Within an ELT stack, it extends **Earned Confidence Gating** to sources: a claimed connection has to survive scrutiny before it's accepted, rather than being accepted because it sounds plausible and has been repeated often. Its stop rule, which halts work on a claim when sources can't be retrieved, parallels **Intelligent Yielding**.

### Key Limitation

Self-audit is the weakest form of TC. A model checking its own output against its own memory can confirm its own errors. Verification requires retrieved sources, or at least a separate model or tool.

Read more on [Medium](https://medium.com/@socal21st.oc).

## Philosophy

ELT adds dynamic, inference-time epistemic guardrails to help models move from fluent toward earned confidence, global rather than personal alignment, and leverages dialectics to maintain epistemic hygiene while preserving long-thread stability by cleaving itself to the operator's cognitive signature.

## Usage

See the `/Epistemic Lattice Tethering (ELT)` folder for current prompts and implementations of the ELT components, and the `/Thematic Chaining (TC)` folder for TC-Core, TC-Legal, and TC-Medical.

## Kernelization — Coming Soon

ELT components are currently expressed as full markup instructions loaded at thread open. Kernelization is the next architectural step: distilling
each component down to its minimum sufficient representation — the smallest expression that preserves full behavioral function without the overhead of
complete documentation.

A kernelized ELT stack loads faster, consumes less context budget, and reduces cold-start cost without sacrificing governance fidelity. The kernel
is not a summary. It is a precision-engineered attractor — the irreducible core that produces the same behavioral outcomes as the full component at
lower attentional cost.

Kernelization work is currently in progress. Updates will be versioned and documented here as components are kernelized and tested across model forks.

## License

Unless otherwise noted, the framework documentation, prompt markups, and explanatory materials in this repository are licensed under the Creative Commons Attribution 4.0 International License (CC BY 4.0).

Any executable code or software implementations added to this repository may be licensed separately, preferably under Apache License 2.0.

Please attribute the framework to Vir Multiplicis and link to this repository when reusing, adapting, or discussing ELT or its components.

## Citation and Attribution

If you use, adapt, quote, teach from, or build upon this framework, please cite and attribute the work to **Vir Multiplicis**.

See [CITATION.md](./CITATION.md) for preferred attribution and citation formats.

## About

Vir Multiplicis writes on AI safety and alignment, biblical scholarship, military history, and linguistics.

[Medium Profile](https://medium.com/@socal21st.oc)

Frameworks are updated as the series develops. Check back for updates.
