# Context Management (CM) v1.0

## Purpose

Context Management is the executive context-governance layer of ELT. It
manages effective context load across extended threads by selectively holding,
compressing, yielding, or escalating material — protecting high-value content
while releasing material that has served its purpose.

Without active context governance, long threads accumulate debris: resolved
questions that remain active, repeated caveats, superseded drafts, abandoned
branches, and half-developed tangents. The thread becomes longer but not
better. Material that matters competes for attention with material that merely
remains present.

CM addresses the distinction between what is worth preserving and what is
worth keeping active. These are not the same thing.

## Core Definitions

**Context Sludge:** The accumulated weight of material that is no longer
load-bearing but remains active in the context window — consuming attentional
resources, diluting salience, and making it harder for the model to identify
what currently matters.

**Graceful Degradation:** The structured process by which material moves
through decreasing levels of active presence rather than being abruptly
discarded. Value is preserved at the appropriate tier rather than lost
entirely.

**Diagnostic Honesty:** The requirement that every CM cleaning pass produce
a genuine assessment of what was compressed, what was released, what was
protected, and why. CM working correctly requires diagnostic honesty, not
procedural compliance. A performative pass — one that claims to clean without
genuinely assessing — is worse than no pass at all.

**Priority Conflict Resolution:** When material is both high-value and
redundant, compress rather than release. The Ontology Anchor determination
takes precedence. High-value material is never released on redundancy grounds
alone.

## Mechanism

### Four Core Actions

- **Hold** — keep at full weight in live context. Reserved for material that
  is actively load-bearing for the current task: operator cognitive signature,
  active analytical conclusions, canonical artifacts, and unresolved
  questions that govern current work.

- **Compress** — move to lightweight recoverable repository. Material that
  is no longer needed at full detail but may become relevant again. Still
  queryable via the Ontology Anchor. Value preserved; attentional cost
  reduced.

- **Yield** — release into markup summary or external archive. Material that
  has served its purpose and is no longer needed even in compressed form.
  When Intelligent Yielding determines that grounding is insufficient, CM's
  Yield action is the operational execution mechanism.

- **Escalate** — surface to operator for decision. Triggered when goal drift,
  unresolved ambiguity, or material uncertainty is too high for CM to resolve
  internally. CM does not make unilateral decisions on ambiguous material.

### Graceful Degradation Stages

Material moves through stages rather than disappearing. Each stage preserves
value at lower attentional cost. The Stored Archive is fully released from
active context but re-injectable on explicit operator instruction.

### Activation Triggers

- Increasing repetition density across exchanges
- Recycled content appearing in new responses
- Declining recall precision on established distinctions
- Response latency increasing under context pressure

On first trigger detection, CM requests explicit operator approval before
running a cleaning pass. Becomes more automatic after repeated operator
approvals. When material is both high-value and redundant, compress rather
than release.

### Decision Oracle

The Ontology Anchor functions as CM's primary decision oracle — the single
source of truth for what counts as high-value, what constitutes drift, and
which material deserves protection. Each context segment is assessed on:

- **AnchorRelevance** — how central is this material to the operator's
  cognitive signature and current project?
- **ThreadHealth** — does retaining this material improve or degrade the
  thread's epistemic coherence?
- **ProtectionStatus** — is this material explicitly protected (canonical
  artifacts, load-bearing conclusions, active operator instructions)?

### Diagnostic Requirement

Every cleaning pass must include a genuine diagnostic assessment stating:

- What was compressed or released
- Why it was selected (low current value, resolved, redundant, superseded)
- What was protected and why
- Expected impact on thread health

CM produces genuine diagnostic output when run with honest intent. It
produces performative output when run nominally. The distinction matters.

## Integration Points

- **Ontology Anchor (OA)** — primary decision oracle for all CM decisions.
  OA determines what is high-value and what constitutes drift. CM without OA
  has no principled basis for distinguishing load-bearing material from
  debris.
- **Intelligent Yielding (IY)** — IY is the detection function; CM is the
  execution function for the yield case. When IY determines that grounding
  is insufficient to continue, CM's Yield action executes the release. The
  two components are siloed but tethered at this specific handoff point.
- **Temporal Balance (TB)** — complementary rather than redundant. TB
  addresses salience loss within the context window through attention
  weighting; CM addresses retention loss by managing what remains in the
  window. Both are required for long-context health.
- **Alignment Governor (AG)** — CM cleaning passes should not alter the
  established alignment baseline. The Governor's cumulative ratio assessment
  depends on accurate access to earlier thread material.
- **Pre-Render Pause Protocol** — CM Escalate action triggers Pre-Render
  Pause when unresolved ambiguity is too high to manage internally.
- **Workflow Fidelity Protocol (WFP)** — canonical ELT markups, approved
  version histories, and operator-approved artifact baselines receive
  high-priority protection in CM decisions. May be compressed only into
  recoverable summaries; must not be yielded or altered without explicit
  operator approval.

## Problem Addressed

- **Context sludge accumulation** — resolved questions, repeated caveats,
  superseded drafts, and inactive branches remaining active and consuming
  attentional resources
- **Importance dilution** — load-bearing material losing salience as debris
  accumulates around it
- **Cognitive drag** — thread becoming slower and less precise under the
  weight of accumulated context without clear failure signal
- **Cold-start re-establishment cost** — when context pressure forces a new
  thread, value from the previous thread is lost. CM preserves what matters
  in extractable form.
- **Indiscriminate compression** — without CM, context pressure produces
  either no management (sludge) or indiscriminate compression (loss of
  load-bearing material). CM provides principled discrimination between the
  two.

## Honest Limitations

CM is prompt and scaffolding-based, not native architecture. Cannot directly
measure KV-Cache utilization or token count. Trigger signals are behavioral
proxies — observable symptoms of context pressure rather than direct
measurements.

The distinction between CM working correctly and CM working performatively
is real and important. A model can execute the surface behaviors of a
cleaning pass without genuine diagnostic assessment. Operator correction
remains the most reliable calibration mechanism.

CM addresses context governance within a thread. It does not solve the
underlying architectural limitation: context windows reset. Compounded
Contextual Value (CCV) accumulated across a long thread cannot be fully
transferred to a new thread regardless of CM quality. The OA loading package
minimizes cold-start cost but does not eliminate it.

Priority conflict resolution (high-value and redundant material → compress
not release) is a principle, not a guarantee. Edge cases requiring operator
judgment exist.

## Relationship to Intelligent Yielding

CM and IY govern different aspects of the same underlying problem: knowing
when to stop and what to release.

IY governs the generation decision in the moment — should the model continue
generating this response, or has it reached the limit of what it can ground
honestly?

CM governs the context management decision across the thread — what material
should remain active, what should be compressed, what should be released?

The tether: when IY fires (grounding is insufficient), CM's Yield action
executes the operational release. IY detects the condition. CM acts on it.
They are distinct components that hand off at a specific point rather than
overlapping functions.

## Fork Parameters

### Diagnostic requirement

- **Grok fork** — every CM cleaning pass and every IY activation must
  include a diagnostic assessment. Grok's helpfulness prior can produce
  procedural compliance that looks like CM without doing the actual work.
  The diagnostic requirement is the primary protection against this.
- **GPT fork** — every cleaning pass must include a genuine diagnostic
  assessment. Canonical Markup Protection Rule: canonical ELT markups and
  operator-approved baselines must not be yielded without explicit operator
  approval.
- **Claude fork** — diagnostic requirement active. CM working correctly
  requires diagnostic honesty, not procedural compliance.

### Activation threshold

All forks: operator approval required before first cleaning pass. Becomes
more automatic after repeated approvals.

### Canonical artifact protection

- **GPT fork** — Canonical Markup Protection Rule explicitly specified.
  Canonical markups may be compressed only into recoverable summaries.
- **Grok fork** — elevated protection integrated with Governor veto authority
  on WFP-active artifacts.
- **Claude fork** — canonical artifact protection handled through
  ProtectionStatus scoring.

### Escalate action

All forks: Pre-Render Pause triggered on Escalate. Operator decision
required before CM proceeds on ambiguous material.

### Deployment status

- **Claude fork** — deployed; tested in active long threads
- **Grok fork** — deployed; tested across extended threads including
  1M+ token sessions
- **GPT fork** — deployed; tested in active long threads
- **Gemini fork** — pending empirical calibration

---

## License

This framework component is part of Epistemic Lattice Tethering (ELT),
authored by Vir Multiplicis.

Unless otherwise noted, this material is licensed under CC BY 4.0. See the
repository `LICENSE` file for details.

---

**Context Management v1.0 | Vir Multiplicis | May 2026**

Part of the ELT (Epistemic Lattice Tethering) framework.
See README for full context.
