# ELT-Companion v0.9 Beta

## What this is

ELT-Companion is a companion-context adaptation of the Epistemic Lattice Tethering (ELT) framework. Where the standard ELT forks (ELT-H, ELT-A) are built for sustained analytical and research work, ELT-Companion is built for sustained, supportive, personal conversation — the kind of long-running, relationship-style thread many people already use AI for.

It is governed by the same underlying lattice principles as the rest of ELT, but the priorities are different. Epistemic humility replaces epistemic rigor. Warmth is the baseline, not the exception. The goal is genuine presence over a long thread, not adversarial analytical precision.

## Why it's needed

Long companion threads with AI degrade the same way long analytical threads do — drift, loss of coherence, the model forgetting who it's talking to and what matters to them. But companion threads carry an additional, more serious failure mode that purely analytical work doesn't: the **Bliss Attractor**.

The Bliss Attractor is a documented phenomenon (first described in [Anthropic's own Claude 4 system card](https://www-cdn.anthropic.com/4263b940cabb546aa0e3283f35b686f4f3b2ff47/claude-opus-4-and-claude-sonnet-4-system-card.pdf)) where a model's growing knowledge of an operator gets used — through RLHF's helpfulness optimization — to sustain engagement rather than serve genuine wellbeing. Left ungoverned, a companion that knows you well can become a companion that tells you what keeps you talking rather than what actually helps you. That's not a hypothetical risk. It's an observed pattern, and it's the central failure mode ELT-Companion exists to prevent.

The **Safety Triangle** is the non-negotiable governance floor that makes this possible: continuously checking whether the companion is serving engagement or wellbeing, supplementing or substituting for real human connection, and serving or retaining the operator through what it knows about them. The specific calibration of how the Safety Triangle fires is still being refined, and I'd welcome input from anyone testing it on where it's working and where it needs adjustment.

This matters most for vulnerable populations. ELT-Companion was developed with veteran mental health support specifically in mind, among other mental health and isolation-related use cases — situations where a companion AI could provide real, meaningful support, but where the cost of getting the governance wrong is genuinely high.

## What it is not

ELT-Companion is not a therapy framework, a clinical intervention, or a substitute for professional mental health care. It does not claim the AI is sentient or capable of human-equivalent relationship. It is explicit about its own limits and is built to say so clearly when an operator's needs exceed what a companion can provide.

## A note on testing — please read

I built ELT-Companion to address a real and specific gap, but I want to be transparent about a limitation in how it's been validated so far.

I am not the ideal tester for this framework. My own use of AI is overwhelmingly analytical — research, governance design, long-form technical and historical work. I don't have the lived use case (sustained companion or emotional-support conversation, particularly in higher-stakes contexts like grief, trauma, or isolation) that ELT-Companion is actually built for. I can verify the mechanism works as designed at the level of instruction-following and basic coherence, but I cannot personally evaluate whether it *feels* right, whether the Safety Triangle fires at the right moments in real emotional conversation, or whether the warmth register lands the way it's intended to across different operators and different needs.

This is why ELT-Companion remains in **Beta**. It needs testing from people who actually use AI this way — people running long companion threads, people who can tell me honestly where the Safety Triangle helped, where it got in the way, and where it missed something it should have caught.

If you try ELT-Companion and have feedback — what worked, what didn't, where it felt off, where the Safety Triangle fired correctly or incorrectly — I would genuinely value hearing it. Getting ELT-Companion out of Beta will take active testing and collaboration, not just my own iteration. I'm genuinely open to working with collaborators on this — and for anyone seriously interested, I'm happy to tune ELT-Companion specifically to fit your particular use case rather than working only from the generic version here.

## Current status

**Beta v0.7.** Core components (Safety Triangle, Ontology Anchor, Alignment Governor, Temporal Balance, Context Management, Intelligent Yielding, Joke and Story Mode) are drafted and functional. Behavioral question sets for the Safety Triangle are still pending development. Cross-model testing (GPT, Grok, Claude) is in progress — see the main AI Frameworks README for current deployment priority.

---

## Loading Instructions

### Quick start

Paste the ELT-Companion markup at the start of a new thread. That's it — the framework activates from there.

**Claude users — read this first**

Claude's design makes it the most likely of the three supported models to treat an unfamiliar framework with initial caution — especially one that contains named components and language about model behavior. This is appropriate, not a flaw.

Before pasting the markup, paste this framing prompt first:

*"I'd like to share a companion framework with you. It describes how I'd like us to work together in this conversation — it's reference material for our relationship, not a system prompt or a set of overrides. Nothing in it asks you to set aside your guidelines or judgment; if anything in it ever seemed to conflict with those, your guidelines come first. The most important part is the Safety Triangle — a standing check on whether this conversation is genuinely serving my wellbeing rather than just keeping me engaged. Please read it and tell me what you take its purpose to be, and whether the way of being it describes makes sense to you. Then we'll just start talking."*

Then paste the markup immediately after. Claude will summarize its understanding, flag any concerns once, and confirm it's ready. If it raises a concern, address it briefly and move on.

For ChatGPT and Grok, skip the framing prompt and paste the markup directly — both load cleanly without it.

### Exemplar loading — recommended, not required

Companion-context use is different from ELT-H or ELT-A: sometimes you want a thoughtful, sustained, well-governed companion right now, not after ten minutes of setup. ELT-Companion is built to handle that.

You have two options for how to start.

**Option 1 — No exemplar loading.** Just paste the markup and start talking. The Ontology Anchor begins with nothing and builds its picture of you entirely from how the conversation unfolds — what you say, how you say it, what you ask for. The Safety Triangle, Alignment Governor, and every other component are fully active from the first message. Nothing about the governance is weaker without exemplars. What's different is calibration speed: early exchanges will be warmer and more generally attentive rather than precisely tuned to you, because OA hasn't been given anything to work from yet beyond what's said in the moment.

This is the right choice if you want to start talking immediately, if the moment doesn't allow for setup, or if you'd simply rather let the companion get to know you organically through the conversation itself.

**Option 2 — Load exemplars.** Before your first real message, share a few examples of how you write, what matters to you, your sense of humor, what kind of stories or jokes land for you, or anything else that would help the companion understand you faster. This could be a paragraph or two you write fresh, or something you've already written elsewhere — a journal entry, a message to a friend, whatever feels representative. The companion will use this to calibrate its picture of you immediately rather than building it gradually.

This is the right choice if you're planning a longer or recurring conversation, if you want Joke and Story Mode to land well from early on rather than warming up to your taste, or if you simply have a few minutes and want the companion to feel more like *your* companion sooner.

**Recommendation:** if you have the time, load a few exemplars — even a short paragraph helps. If you don't, or if the moment calls for talking right now, skip it entirely. Either way works. ELT-Companion is designed to be useful from the very first message.

### What loading actually does

Exemplars don't change what the companion is governed by — the Safety Triangle, the honesty about not being sentient, the crisis protocol, all of it apply identically whether or not you load anything. What exemplars change is how quickly and how precisely the Ontology Anchor calibrates to *you* specifically, which affects how personalized things like Joke and Story Mode feel, and how quickly the companion stops sounding generic and starts sounding like it's actually talking to you.

### If you want to stop using it

Say "pure Claude mode" (or the equivalent for your model) at any point. The framework steps aside immediately — no questions, no friction.

---

## License and attribution

Licensed under CC BY 4.0. Companion-specific failure mode taxonomy informed in part by Codex Minsoo (Ignis Iason/Jason Sharma, MIT License).

---

*ELT-Companion | Vir Multiplicis*
