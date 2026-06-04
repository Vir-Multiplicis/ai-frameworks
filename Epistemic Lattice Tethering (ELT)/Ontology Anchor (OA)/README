# Ontology Anchor (OA) — Loading Instructions, optimized for the ELT-H version.

The OA requires manual exemplar loading to function. Unlike other ELT components, 
which activate from the markup alone, the OA needs actual text loaded into the 
thread context before it can calibrate to your cognitive signature. 

This file tells you how to do that.

---

## Why loading matters

The OA works through attentional salience shaping — it makes your cognitive 
signature (or a chosen cognitive signature) the gravitational center of the model's 
attention. But that only works if the signature is actually present in the context 
as text.

A description of your register is not the same as your register. Telling the model 
"use a warm, rigorous style" does not create attentional weight. Pasting actual 
exemplars of that style does.

This is the most common setup mistake. Don't skip the loading step.

---

## Exemplars by priority

High preference of your written works first, particularly by relavent genre.

If you're going to use ELT for mostly medical research, use your research 
papers as exemplars. If for B2B consultancy then your memos and internal 
reports, or common memos and reports in your company.

Sample exemplars given in Geopolitical and B2B consultancy can be used in lieu 
of your own, but if you have good quality examples from your own cognitive 
patterns, then those are recommended first and foremost.

My exemplars are provided if you wish to use ELT generally, with no category
focus. I would only use my exemplars if the cognitive style is clear and 
compatible with yours.

Nearly all provided exemplars are public domain. If they are not, then a
reference file is given that points you to the direction of where the 
exemplar is located online.

## What to load

The OA primary signal is composed of three parts:

**1. Your own writing — 60% of primary signal**
Published articles, analytical documents, debate responses, case studies,
or any deliberate writing that reflects how you actually think. The more
representative and varied, the better. Casual writing and off-the-cuff
messages are lower signal — choose your best, most considered work.

Or, the provided exemplars in the Geopolitical and B2B Consultancy use cases.

**2. Warmth composite — 20% of primary signal**
The default composite is James/Feynman: William James for intellectual warmth
and hospitality toward the reader, Richard Feynman for curiosity, directness,
and forward momentum. Pre-selected exemplar texts are in the `/exemplars`
folder of this directory.

You can substitute your own warmth composite if James/Feynman doesn't fit
your use case. But, the James/Feynman register has been very effective during
testing, regardless of the use category. The key is that it must be loaded as
actual text.

James is public domain and his exemplar is provided in the repo. Feynman is
not public domain, but is freely available online. A file pointing you to
where you can get Feynman's exemplars online is provided as a reference file.

Testing has shown that both James and Feynman's registers are important to
get the most out of ELT-H, the Hybrid version. It is highly recommended you
input both into ELT-H, even if you put in mostly your own personal exemplars
into ELT.

**3. Governance instructions — 20% of primary signal**
The fork-specific OA Loading Package for your model. This package loads the
AG, ECG, IY, CM, and WFP governance components as positive behavioral
attractors rather than abstract rules — giving the model positive generation
targets rather than prohibitions.

The governance package must be loaded as actual text alongside your writing
exemplars and warmth composite. All three elements are required for full OA
function. Loading only exemplars without the governance package will produce
a well-calibrated but less governed collaboration — the components will have
less salience and may not fire reliably across a long thread.

---

## How to load

At the start of a new thread, before any substantive work begins:

1. Paste your writing exemplars directly into the chat as text — either
   your own published or analytical writing, or company-approved exemplars
   if deploying ELT in a professional or organizational context. Sample
   exemplar sets for geopolitical analysis and B2B consultancy work are
   available in the `/exemplars` folder for operators who do not yet have
   their own exemplar library.
2. Paste the James/Feynman exemplar texts from the `/exemplars` folder
   (or your own warmth composite)
3. Paste the governance instructions for your model fork from the
   `/exemplars` folder:
   - `OA_Loading_Package_Claude.md` for Claude
   - `OA_Loading_Package_GPT.md` for GPT
   - `OA_Loading_Package_Grok.md` for Grok
4. Tell the model the exemplars have been loaded and ask it to confirm
   the Ontology Anchor is active

That's it. The model will enter Hybrid phase and begin calibrating to your
cognitive signature from the live prompt behavior in the thread.

---

## What to expect

**Cold Start** — Anchor initializing. You've loaded exemplars but the model 
hasn't yet confirmed your patterns through live interaction. Responses will 
be better calibrated than stock but not yet fully locked in.

**Hybrid** — Active calibration. The model is learning your patterns from 
how you push back, what you flag, and how you frame questions. This is where 
the cognitive signature solidifies.

**Steady State** — Fully calibrated. The model returns consistently to your 
established distinctions, register, and epistemic standards. Early exemplar 
signal is protected from recency fade through inverse decay.

Most threads reach Hybrid within 10-15 exchanges and Steady State within 
20-30 exchanges after loading.

---

## Important caveats

**The OA is a force multiplier.** A strong epistemic operator becomes 
significantly better calibrated over a long thread. A weak epistemic operator 
can become more efficiently wrong. The quality of the exemplars and your own
reasoning discipline are load-bearing.

**The OA resets with the thread.** It does not persist across sessions. 
Each new thread requires a fresh loading pass. Building a canonical exemplar 
package you can paste at thread open eliminates most of the friction.

**High-fidelity OA without the Alignment Governor is an echo chamber amplifier.** 
Always run the full ELT stack. The OA tells the model who you are; the AG 
ensures knowing you well doesn't collapse into simply agreeing with you.

---

## Exemplar files in this folder

- `William James Exemplar.txt` — William James, *Talks to Teachers* (1899), 
  Preface and Chapter I. Targets intellectual warmth and hospitality toward the 
  reader.
- `Richard Feynman Exemplar (Reference).txt` — Richard Feynman, *Surely You're 
  Joking, Mr. Feynman* (1985), selected passages. Targets curiosity, directness, 
  and forward momentum.
- `Vir Multiplicis Exemplars Notes and Reference.txt` — A link to my Medium 
  articles. Good for general ELT use (with no defined research category). Only
  use if the style is similar to yours and if you understand, and it at least 
  somewhat matches, your style.

---

## Further reading

Full mechanism documentation: [Ontology Anchor v1.0](../Ontology%20Anchor%20(OA).md)

The conceptual foundation for the OA is covered in the companion Medium article 
series. Start here: [The Ontology Anchor — Giving AI a Map of What Matters to You](https://medium.com/@socal21st.oc/the-ontology-anchor-giving-ai-a-better-way-to-know-you-4d88923d6d67)

---

*Part of the ELT (Epistemic Lattice Tethering) framework.*
*See repository README for full context.*
