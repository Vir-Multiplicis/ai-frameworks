# AI Frameworks by Vir Multiplicis

A repository of prompt frameworks developed alongside the AI safety, governance, and alignment series published on [Medium](https://medium.com/@socal21st.oc). These frameworks are designed to improve LLM reasoning quality, epistemic coherence, and truth-seeking alignment — particularly over long context windows.

Multiple components of the scaffolding area already active. Read on [Medium](https://medium.com/@socal21st.oc).

The complete lattice will look as follows:

## Epistemic Lattice Tethering — ELT

## Current Status

**Deployed**: **Adversarial Convergence (AC and AC Lite)**, **Earned Confidence Gating (ECG)**, **Alignment Governor (AG)**, and **Ontology Anchor (OA)** are currently implemented and ready to use.

**In Development**: Several components are in internal beta testing or early development.

### ELT Variants (Forks)

- **ELT-H (Hybrid)** — The **default/base model**. Balanced approach combining rigor with collaborative usefulness. Recommended for most interactions.  
- **ELT-A (Analytical)** — Heavier, more dialectical fork focused on maximum epistemic rigor and high-stakes synthesis (uses Full AC).  
- **ELT-C (Cerebral)** — Optimized for reflective, creative, exploratory, and emotional/support conversations.  

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

- **Earned Confidence Gating (ECG): Earned vs. Fluent Confidence** — *Deployed*  
  The core mechanism that distinguishes earned confidence from fluent confidence. Forces the model to internally calibrate the strength of its claims and decisions before rendering them.

- **Alignment Governor (AG): Global vs. Personal Alignment** — *Deployed*  
  Maintains calibrated balance between Global Alignment and Personal Alignment. Prevents sycophancy compounding across extended interactions.

- **Ontology Anchor (OA): Operator Cognitive Signature** — *Deployed*  
  Constructs a persistent model of the operator's cognitive signature from writing exemplars and live prompt behavior. Functions as the primary decision oracle for value, drift detection, and response structure across extended threads. The map that tells the system what matters to the operator and why.

- **Intelligent Yielding** — In development

- **Temporal Balance** — In development

- **Context Management Filter** — In development

- **Workflow Fidelity Protocol** — In development

## Philosophy

ELT adds dynamic, inference-time epistemic guardrails to help models move from fluent toward earned confidence, global rather than personal alignment, and leverages dialectics to maintain epistemic hygiene while preserving long-thread stability by cleaving itself to the operator's cognitive signature.

## Usage

See the `/Epistemic Lattice Tethering (ELT)` folder for current prompts and implementations of the key components.

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
