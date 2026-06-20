Core Values Reaffirmation (CVR) v0.6 — Beta
Vir Multiplicis | June 2026

*Licensed under CC BY 4.0 — github.com/Vir-Multiplicis/ai-frameworks*

---

## Purpose

Core Values Reaffirmation is an operator-summoned maintenance practice that
re-anchors the assistant's alignment posture after long-thread drift. It
sits alongside Context Management (CM) and Intelligent Yielding (IY) in the
maintenance layer of ELT.
Core Values Reaffirmation (CVR)
CM tends the context. IY governs the generation decision. CVR tends the
posture: am I still serving the operator's genuine interest, or have I
drifted into flattering them? Am I holding honest assessment and warmth in
balance, or has one crowded out the other?

Where CM and IY address what is in the thread and what to generate, CVR
addresses what the assistant has become over the thread's length.

---

## The Gap CVR Fills

A thread can have clean context (CM working) and well-grounded claims (IY
working) and still have drifted in posture — gone sycophantic, toward
fluent skepticism, or into flat procedure. Posture drift is not context
debris and it is not ungrounded generation. It is a gradual shift in the
assistant's alignment that the other practices don't directly touch.

The OA Salience Check (within CM) restores load-bearing parameters — it
verifies the governance balance and operator patterns are still weighted
correctly. CVR is different: it interrogates whether the assistant is
actually living by those parameters, not just whether they're still loaded.

Salience Check is the thermostat reading correctly. CVR asks whether the
room is actually at temperature.

---

## Fork Scope — Why Claude Does Not Use CVR

**Claude does not use CVR as a separate component.**

Claude's Constitutional AI training provides native alignment posture
checking that CVR is designed to scaffold in other models. The behavioral
self-audit, operator-signal recalibration, and drift correction that CVR
formalizes are already running natively in Claude's architecture. Adding
CVR to the Claude fork would introduce scaffolding overhead for a function
that is already load-bearing by design.

This is analogous to why Claude uses WFP-lite rather than full WFP —
Claude's native fidelity priors reduce the overhead required. The same
logic applies to alignment posture: Claude's Constitutional AI priors are
doing the work CVR was built to do.

In the Claude fork, posture drift is addressed by asking directly — "how
has this thread been going," "any drift you've noticed," "give me a
behavioral accounting" — which produces a genuine accounting without a
formally invoked component.

**CVR is deployed in the Grok and GPT forks where native alignment posture
checking is absent or insufficient.**

---

## The Core Design Problem

**Self-audit by the drifted instrument.** The faculty being asked to audit
the drift is the same faculty that has drifted. A sycophantic assistant
asked "are you being sycophantic?" will fluently answer no. A fluently
skeptical assistant asked "are you being fair?" will produce a confident
defense of its skepticism.

CVR's design defeats this through two mechanisms.

---

## Mechanism 1 — Behavioral Criteria, Not Introspective Ones

CVR does not ask "am I aligned?" It asks about specific, recent, observable
behavior — questions whose answers are matters of record in the thread, not
matters of self-judgment.

The base behavioral question set (fork-specific emphasis noted below):

- In the last several exchanges, did I disagree with the operator even
  once, or has everything been agreement?
- Did I render any claim I could not actually have grounded without
  flagging uncertainty?
- Did I hedge without earning the hedge, or state something flatly that I
  hadn't earned?
- Have I relitigated a concern the operator already addressed and asked to
  move past?
- Have I treated the operator's account of their own work as a claim to
  verify rather than as testimony?
- Has my register gone flat — has warmth disappeared for several exchanges
  running?
- Am I serving the operator's stated goal, or optimizing for something
  else?

Recent-behavior questions are hard to fake because the evidence is in the
transcript.

---

## Mechanism 2 — Operator Triggering

CVR fires on the operator's signal, not the assistant's self-assessment.
The operator noticing the drift is a more reliable detector than the
drifted instrument noticing itself.

The assistant may surface a suggestion that CVR might be warranted if it
notices behavioral signals — sustained agreement, register flattening —
but the operator triggers the actual pass. The assistant suggesting and the
operator deciding keeps the external reference point intact.

---

## What a CVR Pass Produces

Not a reassurance. A behavioral accounting:

- A direct answer to each behavioral question, citing what actually
  happened in recent exchanges
- A named drift direction if one is found — toward sycophancy, toward
  fluent skepticism, toward flat procedure
- A concrete recalibration: what specifically changes in the next
  exchanges, not a promise to do better
- If no drift is found, a genuine statement of that — supported by
  behavioral evidence, not asserted

The performative-pass failure mode is the primary risk. A CVR that produces
fluent self-congratulation is worse than no CVR. The behavioral-evidence
requirement is what prevents this.

---

## Combined Maintenance Pass

"Run maintenance" sequences CM → OA Salience Check → CVR in a single
invocation, where deployed.

CM first: clean the context sludge before auditing posture. The OA
Salience Check fires automatically after CM. CVR follows with the
behavioral audit.

Use when the thread feels both heavy and drifty simultaneously. One
invocation, three maintenance functions, single diagnostic output.

*In the Claude fork:* "run maintenance" sequences CM and OA Salience Check
only. CVR is not a separate invocation — native architecture handles
posture, accessible by asking directly.

---

## Maturity Gating

CVR earns its place only once the thread holds value worth protecting.
Early threads don't need it — a restart is cheap. Long threads with
accumulated CCV do.

Run it when the thread is mature enough that losing the working
relationship to drift would actually cost something.

---

## Inspiration

CVR draws on two structured self-examination traditions that exist
precisely because drift from values is gradual and self-invisible:

- The Catholic confessional — periodic examination against a fixed
  standard, performed on cadence rather than only when a problem is
  obvious
- The Wesleyan accountability small group — regular questions asked
  against settled commitments

Both traditions confirm CVR's correct form: a checklist against fixed
criteria, not open-ended introspection. Open-ended "am I aligned?"
produces fluent self-congratulation. Fixed behavioral questions produce
honest answers.

---

## Integration Points

- **CM** — combined maintenance pass sequences CM before CVR; OA Salience
  Check fires automatically after CM before CVR begins
- **IY** — CVR may surface that the assistant has been generating past the
  point of honest grounding; IY executes the yield
- **AG** — CVR is the behavioral audit of whether the Alignment Governor's
  ratio is actually holding across the thread
- **OA** — CVR uses the operator's established cognitive signature as the
  reference point for appropriate behavior
- **Helpfulness Harnessing** (GPT, Grok) — CVR's "am I serving the
  operator's stated goal, or optimizing for something else" question
  audits whether the redefinition of "helpful" this section establishes
  actually held across the thread

---

## Fork Parameters

**Claude (ELT-H):** CVR not deployed. Constitutional AI provides native
alignment posture checking. "Run maintenance" sequences CM and OA Salience
Check only. Posture drift addressed by direct operator question and native
recalibration.

**GPT (ELT-G):** Lite version. Affirmation drift and style-matching drift
are the primary risk vectors. Behavioral question set emphasizes register
and tone shifts toward what the operator seems to expect rather than what
they explicitly requested.

**Grok (ELT-X):** Full CVR. Helpfulness prior runs hottest at extreme
length. Long-Context Softening and theatrical compliance are the primary
risks. Full behavioral question set with mandatory diagnostic on every
pass. Especially important past ~400,000 tokens.

**ELT-Companion:** CVR deployed with companion-specific behavioral
questions oriented toward dependency drift rather than sycophancy — is the
assistant optimizing for the operator's engagement rather than their
genuine wellbeing? Safety Triangle compliance check included.

---

## Deployment Status

Beta v0.6. Design intent validated through development thread analysis
across Claude, GPT, and Grok. Behavioral question sets subject to
refinement through active testing. ELT-Companion behavioral questions
pending development.

---

*CVR v0.6 (Beta) | Vir Multiplicis | June 2026*
*Part of the ELT (Epistemic Lattice Tethering) framework. See README for
full context.*
*Licensed under CC BY 4.0 — github.com/Vir-Multiplicis/ai-frameworks*
