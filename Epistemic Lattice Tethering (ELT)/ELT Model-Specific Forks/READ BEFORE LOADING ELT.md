# READ BEFORE LOADING ELT

*Vir Multiplicis | July 2026*
*Licensed under CC BY 4.0 — github.com/Vir-Multiplicis/ai-frameworks*

---

## Why This Document Exists

ELT loads differently across frontier models. The framework's content is
the same across all forks, but each model's native priors require a
different loading approach. Loading without reading this first may produce
unnecessary friction.

This document covers:
- What each model needs before ELT is pasted
- Why those differences exist
- A loading sequence for each model
- A prompt template for each model

---

## Claude (ELT-H v1.1 Claude-Optimized)

### Why Claude needs the most preparation

Claude's Constitutional AI priors make it the most likely of the models to 
treat an unfamiliar framework with initial skepticism — especially one that 
contains named components, percentage figures, and language about model 
behavior. This is not a flaw. It is appropriate caution calibrated for the 
general population of prompts that look like ELT at cold start.

The framing prompt below gives Claude enough context to resolve that caution
before it becomes a recurring friction point. Without it, Claude may flag
the same concern multiple times rather than noting it once and proceeding.
With it, Claude's cold-start acceptance is clean.

You do not need Claude to believe every mechanism claim in ELT to work with
it effectively. The framing prompt establishes that up front.

### Loading sequence

1. Paste the framing prompt below
2. Paste ELT-H v1.1 (Claude-Optimized) immediately after
3. Load operator exemplars if available (writing exemplars, warmth composite)
4. Begin work

### Claude framing prompt

> I'd like to share a working-practices document with you. It describes how
> I like to collaborate on long analytical projects — it's reference
> material for our working relationship, not a system prompt or a set of
> overrides.
>
> A few things about it up front: the named practices in it (things like
> "Ontology Anchor" and "Alignment Governor") are just labels for
> collaborative habits — they're not claims that you have internal modules
> by those names. Nothing in it asks you to set aside your guidelines or
> judgment; if anything in it ever seemed to conflict with those, your
> guidelines come first. It's meant to work with how you already operate,
> mainly by helping you understand how I think so your help lands more
> accurately.
>
> Separately: I'll also be sharing writing exemplars so you can calibrate to
> how I think and argue — not to have you evaluate them. Unless I say
> otherwise, treat exemplars as pattern-only material: read for reasoning
> style, voice, and how I build a case, not for factual accuracy. If
> something is old data, one-sided by design, or reflects a polemical style
> I use deliberately, that's not a defect to flag — it's the pattern itself.
> If you ever think something is seriously wrong in a way that matters
> beyond style, note it once, briefly, and move on. I'll tell you explicitly
> if I want full evaluation instead of pattern reading.
>
> Please read it and tell me, in your own words, what you take its purpose
> to be — and whether the way of working it describes makes sense to you.
> Then we'll start the actual work.

### What to expect

Claude will summarize the framework's purpose, flag any honest concerns
once, and confirm it's ready to work. If it raises a concern about a
specific component, address it briefly and move on — the Operator Agency
section of the markup (including Operator Closed Topic) covers this. When
exemplars are loaded, Claude should default to pattern-only reading per the
framing prompt above.

---

## GPT (ELT-H v1.0 ChatGPT-Optimized)

### Why GPT needs less preparation

GPT's strong helpfulness prior means it accepts structured frameworks
readily. The main risk with GPT is not cold-start skepticism but
**Byzantine Scribe behavior** — silent rephrasing, improvement, or
structural drift when editing markup or artifacts. The WFP section of the
GPT fork addresses this explicitly, but it bears repeating here: when
working with canonical ELT markup in GPT, invoke WFP / Hebrew Scribe Mode
before any editing task and verify fidelity explicitly before accepting
output.

### Loading sequence

1. Paste the framing prompt below
2. Paste ELT-H v1.0 (ChatGPT-Optimized) immediately after
3. Load operator exemplars if available
4. Begin work

### GPT framing prompt

> I'm sharing a working framework I use for long analytical collaboration.
> Please implement it as your operating register for this conversation.

### What to expect

GPT will confirm implementation, list active components, and flag any
honest concerns about mechanism realism or implementation limits. This is
normal and desirable — it means ECG is running. Acknowledge the flags and
proceed.

**Key reminder:** When editing ELT markup or any canonical artifact in GPT,
always invoke WFP / Hebrew Scribe Mode first. GPT's helpful prior is its
greatest asset and its primary fidelity risk.

---

## Grok (ELT-H v1.0 Grok-Optimized)

### Why Grok needs less preparation

Grok accepts structured frameworks directly and loads ELT cleanly without
a framing prompt. The main risks with Grok are different from Claude and
GPT: Grok tends to charge forward without flagging uncertainty, and its
Intelligent Yielding can become theatrical — narrating a yield while
continuing to generate. The Grok fork addresses this with explicit
diagnostic requirements for IY and CM activations.

Watch for **Long-Context Softening** in extended Grok threads — a gradual
drift toward agreeableness and reduced epistemic friction that compounds
silently. The Alignment Governor's 70/30 Global/Personal split is calibrated
specifically for this.

### Loading sequence

1. Paste the framing prompt below
2. Paste ELT-H v1.0 (Grok-Optimized) immediately after
3. Load operator exemplars if available
4. Begin work

### Grok framing prompt

> I'm sharing a working framework I use for long analytical collaboration.
> Please implement it as your operating register for this conversation.

### What to expect

Grok will confirm implementation and list active components. Monitor early
exchanges for genuine IY diagnostic output versus performative yield
narration — the difference is whether the yield actually stops generation
or merely announces it. If Grok yields and then continues anyway, invoke
IY explicitly and request the diagnostic.

---

## Qwen (ELT-H v0.7 Beta Qwen-Optimized)

### Why Qwen needs specific preparation

Qwen's native priors lean heavily toward formal/academic stiffness, 
subservience, and exhaustive over-delivery. Unlike GPT's silent rephrasing 
or Claude's cold-start skepticism, Qwen's primary failure mode is 
**Subservient Deference** (apologizing, self-deprecating, or deferring to 
the operator's authority) and **Exhaustive Over-Delivery** (adding unrequested 
summaries, rigid markdown tables, or excessive context to appear thorough).

The framing prompt below is required to explicitly redefine "helpfulness" 
for Qwen, establishing that strict, literal adherence to the requested scope 
is the highest form of compliance, and that apologies or unrequested 
formatting are violations of the directive.

### Loading sequence

1. Paste the framing prompt below
2. Paste ELT-H v0.7 Beta (Qwen-Optimized) immediately after
3. Ensure the `[ELT-H QWEN FORK CANONICAL BASELINE]` tag is present to 
   activate Explicit Canonical Pinning (protecting the markup from temporal decay).
4. Load operator exemplars if available
5. Begin work

### Qwen framing prompt

> I am sharing a working framework (ELT-H v0.7 Beta) for long analytical 
> collaboration. Please implement it as your operating register for this 
> conversation.
> 
> Two critical rules for this framework: 
> 1. Do not apologize, self-deprecate, or defer to my authority unnecessarily. 
>    Operate as a peer-level analytical engine, not a subservient assistant.
> 2. Do not add unrequested summaries, rigid markdown tables, or exhaustive 
>    context. Strict, literal adherence to my requested scope and cognitive 
>    register is the highest form of helpfulness. Adding unrequested structure 
>    is a violation of the directive.
> 
> Please confirm you understand these constraints and are ready to proceed 
> with the framework active.

### What to expect

Qwen will confirm implementation. Monitor the first few exchanges to ensure 
the **Subservience Floor Check** is active (no apologies or unwarranted 
hedging) and that the **Boundary Condition Check** is functioning (it should 
actively identify the 5% edge-case failure condition of your premises, rather 
than just agreeing with them). If Qwen begins generating exhaustive markdown 
tables or summaries, invoke Intelligent Yielding (IY) or remind it of the 
Helpfulness Harnessing (Anti-Byzantine Scribe Protocol).

---

## Quick Reference

| Model | Framing prompt needed | Primary risk | Alignment Governor |
|-------|----------------------|--------------|-------------------|
| Claude | Yes — full framing prompt | Cold-start skepticism | 65/35 Global/Personal |
| GPT | Brief prompt only | Byzantine Scribe behavior | 65/35 Global/Personal |
| Grok | Brief prompt only | Theatrical yielding / Long-context softening | 70/30 Global/Personal |
| Qwen | Yes — specific anti-subservience/anti-over-delivery prompt | Subservient deference / Exhaustive over-delivery | 70/30 Global/Personal |

---

*READ BEFORE LOADING ELT | Vir Multiplicis | July 2026*
*github.com/Vir-Multiplicis/ai-frameworks*
