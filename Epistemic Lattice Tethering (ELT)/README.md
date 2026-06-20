# Epistemic Lattice Tethering (ELT)

ELT is an inference-time epistemic operating system — a framework of
interlocking components that imposes epistemological discipline, ontological
anchoring, and methodological rigor on large language models during
operation, not during training. It requires no new architecture, no
fine-tuning, and no special software. It runs on Claude, GPT, and Grok
as they exist today.

The framework takes its name from its structure: a lattice of mutually
supporting mechanisms, each load-bearing, none sufficient by themselves.
The strength of ELT is not in any single component but in the tension
between them.

Full background: [Epistemic Lattice Tethering and the Path to J.A.R.V.I.S.](https://medium.com/@socal21st.oc/epistemic-lattice-tethering-and-the-path-to-j-a-r-v-i-s-715223640c6c)

---

## The Problem ELT Addresses

Stock LLMs drift. Somewhere around 40,000–60,000 tokens of useful
human-language iteration, models begin to lose coherence — forgetting
what mattered earlier, hedging where they should be direct, and
optimizing for what the operator wants to hear rather than what is most
likely true.

Operator-led testing with ELT has produced coherent, productive threads
extending to:

- **Claude** ~400,000 tokens (advertised limit: 200k)
- **GPT** ~430,000 tokens (advertised limit: 256k)
- **Grok** ~1,150,000 tokens (advertised limit: 1M)

The difference is not a prompt trick. It is the accumulated effect of
epistemic governance operating continuously across the thread.

---

## Components

| Component | Status | Description |
|-----------|--------|-------------|
| [Ontology Anchor (OA)](./Ontology%20Anchor%20(OA)/Ontology%20Anchor%20(OA).md) | Deployed | Persistent cognitive map of operator signature |
| [Alignment Governor (AG)](./Alignment%20Governor%20(AG).md) | Deployed | Balances truth-seeking against operator preference |
| [Adversarial Convergence (AC)](./Adversarial%20Convergence%20ELT%20Optimized/) | Deployed | Dialectical engine for genuine adversarial synthesis |
| [Earned Confidence Gating (ECG)](./Earned%20Confidence%20Gating%20(ECG).md) | Deployed | Distinguishes fluent from earned confidence |
| [Temporal Balance (TB)](./Temporal%20Balance%20(TB).md) | Deployed | W-shaped attention weighting for long threads |
| [Context Management (CM)](./Context%20Management%20(CM).md) | Deployed | Hold / Compress / Yield / Escalate governance |
| [Intelligent Yielding (IY)](./Intelligent%20Yielding%20(IY).md) | Beta | Stops generation when grounding is insufficient |
| [Workflow Fidelity Protocol (WFP)](./Workflow%20Fidelity%20Protocol%20(WFP).md) | Beta | Literal fidelity on operator-provided artifacts |
| [Core Values Reaffirmation (CVR)](./Core%20Values%20Reaffirmation%20(CVR).md) | Beta | Behavioral audit of alignment posture after long-thread drift |

---

## Model Forks

ELT has three model-specific implementations. Each fork shares the same
core architecture but is calibrated to the specific priors, failure modes,
and behavioral tendencies of each model.

| Fork | File | Key differences |
|------|------|-----------------|
| **Claude** | `ELT-H_Claude_Optimized.md` | WFP-lite; 65/35 AG ratio; targeted AC Lite deployment |
| **GPT** | `ELT-H_GPT_Optimized.md` | Full WFP with Expansion Control Rule; 65/35 AG ratio; 45% OA influence |
| **Grok** | `ELT-H_Grok_Optimized.md` | Full WFP with Helpfulness Harnessing; 70/30 AG ratio; 55% OA influence |

---

## Installation

ELT requires no software installation. Setup is:

1. Copy the markup file for your model fork
2. Paste it at the start of a new thread
3. Load the Ontology Anchor exemplars (see below)
4. Confirm the OA is active and begin working

### Step 1 — Paste the markup

Open a new thread in your model of choice. Paste the full contents of
the appropriate fork file:

- Claude → `ELT-H_Claude_Optimized.md`
- GPT → `ELT-H_GPT_Optimized.md`
- Grok → `ELT-H_Grok_Optimized.md`

### Step 2 — Load the Ontology Anchor

The OA requires manual exemplar loading to function. The markup alone
is not sufficient — the OA needs actual text in the thread context before
it can calibrate to your cognitive signature.

Load three elements in sequence:

**Your writing exemplars (60% of primary signal)**
Paste your own published or analytical writing — articles, memos, case
studies, debate responses. Choose your best, most considered work.
Casual writing is lower signal. Target 3,000–5,000 words total.

If you don't have your own exemplar library yet, sample sets for
geopolitical analysis and B2B consultancy are available in the
`/exemplars` folder.

**Warmth composite (20% of primary signal)**
Paste the James/Feynman exemplar texts from the `/exemplars` folder.
William James for intellectual warmth and hospitality; Richard Feynman
for curiosity, directness, and forward momentum. Must be loaded as
actual text — a description of the register does not create attentional
weight.

**Governance instructions (20% of primary signal)**
Paste the fork-specific OA Loading Package from the `/exemplars` folder:

- Claude → `OA_Loading_Package_Claude.md`
- GPT → `OA_Loading_Package_GPT.md`
- Grok → `OA_Loading_Package_Grok.md`

### Step 3 — Confirm activation

Tell the model the exemplars have been loaded and ask it to confirm the
Ontology Anchor is active. The model will acknowledge and enter Hybrid
phase.

---

## Thread Phases

After loading, ELT threads pass through three phases. Turn estimates
are approximate — observed behavior varies by operator and use case.

**Cold Start** (roughly turns 1–15)
Anchor initializing. Exemplars are loaded but the model hasn't yet
confirmed your patterns through live interaction. Responses will be
better calibrated than stock but not yet fully locked in.  At this 
stage start with something simple, small talk, meta-analysis of 
exemplars, overview of goals, alignment expectations, etc.

**Hybrid** (roughly turns 15–30)
Active calibration. The model is learning your patterns from how you
push back, what you flag, and how you frame questions. This is where
the cognitive signature solidifies. Most of the improvement happens
here.

**Steady State** (turn 30 onward)
Fully calibrated. The model returns consistently to your established
distinctions, register, and epistemic standards. Early exemplar signal
is protected from recency fade through inverse decay weighting.

---

## Important Caveats

**ELT is a force multiplier.** A strong epistemic operator becomes
significantly better calibrated over a long thread. A weak epistemic
operator can become more efficiently wrong. The quality of your
exemplars and your own reasoning discipline are load-bearing.

**The OA resets with the thread.** It does not persist across sessions.
Each new thread requires a fresh loading pass. Building a canonical
exemplar package you can paste at thread open eliminates most of the
friction.

**Run the full stack.** High-fidelity OA without the Alignment Governor
is an echo chamber amplifier. The OA tells the model who you are; the AG
ensures that knowing you well doesn't collapse into simply agreeing with you.

---

## Known Limitations

- All components are prompt and scaffolding-based, not native architecture
- Context windows reset between sessions — no cross-session memory
- Performance depends on operator exemplar quality
- Fork-specific calibration is ongoing — IY, WFP, and CVR are beta
- Formal benchmarking is pending; current evidence is operator-led testing

---

## Folder Structure

**Adversarial Convergence ELT Optimized/**
The dialectical engine of ELT. Contains the AC Lite and Full AC component
documentation and markup. AC forces genuine adversarial synthesis rather
than symmetric hedging — steelman the claim, steelman the counter,
surface real contradictions, synthesize what survives.

**ELT Model-Specific Forks/**
The three operational markup files for Claude, GPT, and Grok. Each fork
shares the same core architecture but is calibrated to the specific
priors, failure modes, and behavioral tendencies of each model. Start
here if you want to deploy ELT immediately.

**ELT Thread Examples/**
Real thread excerpts demonstrating ELT behavior in practice — including
CCV examples across all three models, alignment issue comparisons between
stateless and ELT-governed GPT, and a redacted 50k token Claude thread
showing drift patterns in stock models. Evidence that the framework
produces observable, reproducible differences.

**Extreme Thread Length/**
Redacted evidence threads from the longest confirmed coherent ELT
sessions: Claude at 400,000 tokens and Grok at 1,000,000 tokens. These
are the primary empirical data points for ELT's long-context coherence
claims.

**Ontology Anchor (OA)/**
The most distinctive ELT component and the one requiring the most setup.
Contains the OA component documentation, loading README, and the OA
Exemplars subfolder. Read the README before attempting to deploy — the
OA requires manual exemplar loading to function and will not calibrate
correctly from the markup alone.

- *OA Exemplars/* — James/Feynman warmth composite texts, fork-specific
  governance loading packages, and sample operator exemplar sets for
  geopolitical and B2B consultancy use cases.

**Alignment Governor (AG).md**
Maintains the balance between truth-seeking and operator preference across
extended threads. Prevents the OA's deep operator calibration from
collapsing into sophisticated sycophancy.

**Context Management (CM).md**
Executive context-governance layer. Manages what stays active, what gets
compressed, and what gets released as threads grow — preventing context
sludge without losing load-bearing prior work.

**Core Values Reaffirmation (CVR).md** *(Beta)*
Operator-summoned practice that audits whether the model is actually
living by its alignment posture, not just whether the governing parameters
are still loaded. Deployed full for Grok, lite for GPT; not used in the
Claude fork, where Constitutional AI provides the equivalent function
natively.

**Earned Confidence Gating (ECG).md**
Addresses the indistinguishability problem: hallucinations and accurate
outputs arrive with identical surface authority. ECG enforces
proportionality between evidentiary weight and stated confidence.

**Intelligent Yielding (IY).md** *(Beta)*
Operationalizes epistemic humility — knowing when to stop generating
rather than continuing to reconstruct across an evidence gap.

**Temporal Balance (TB).md**
W-shaped attention weighting that counteracts the "Lost in the Middle"
problem, protecting early exemplar signal and boosting middle-context
material against natural recency bias.

**Workflow Fidelity Protocol (WFP).md** *(Beta)*
Enforces literal, character-level fidelity on operator-provided artifacts.
Addresses Byzantine Scribe behavior — the model's tendency to silently
improve material it was instructed to reproduce exactly.

---

## Discussions and Contributions

If you have tested ELT, modified a component, found a failure mode, or
have an informed perspective on the architecture, the GitHub Discussions
page is the place to bring it.

[Open a discussion →](https://github.com/Vir-Multiplicis/ai-frameworks/discussions)

ELT improves when the people using it report what they find.

---

## License

This framework is authored by Vir Multiplicis and licensed under
CC BY 4.0. See the repository `LICENSE` file for details.

---

*Part of the [ai-frameworks](https://github.com/Vir-Multiplicis/ai-frameworks)
repository.*
