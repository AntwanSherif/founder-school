# 2026-06-23 — Architecture + positioning pivot: technical detour that sharpened the strategy

**Session type:** Technical/strategic detour from the business-fundamentals spine. Produced Lesson 09.

---

## (a) Architecture rethink: edge–cloud funnel + headless core + native sequencing

The session revisited EncoreShot's compute architecture and crystallised three structural decisions:

**Edge–cloud funnel (Tier 0 → Tier 1):** A cheap on-device mechanical cull (too dark, too short, silent, motion-blurred) rejects the obvious garbage before any upload happens. Only survivors go to cloud semantic scoring. This genuinely shrinks the upload and reduces per-session COGS — but the limit is important to name: it *shrinks* the upload, it doesn't eliminate the cloud. The semantic judgment (is this a good shot of Beyoncé?) still needs cloud AI. The funnel is a cost optimization on top of a cloud-dependent architecture, not a path to offline operation.

**Headless core + thin shells:** Platform-agnostic scoring engine with per-surface shells (web now, native later). Business value: one engine maintains the moat across all surfaces without rewriting; persona-expansion (swap prompts → wedding photographer tier) is near-zero marginal cost on top of the same core.

**Native sequencing (deferred, not abandoned):** Native iOS is the right eventual surface for professional concert shooters, but it's a capital spend for a later phase. Web validates the business model first; the headless architecture means iOS is an additive shell, not a rebuild. No date set. Context in `docs/adr/` if/when the decision is formalised.

---

## (b) Persona pivot: target prosumer/superfan, not the casual fan

The most strategically significant shift from this session. Previous implicit target: casual concert fan who shoots occasionally. Problem: **willingness-to-pay is weak for casual consumer editing.**

Evidence from MIDiA Research (2025): approximately 23% of music fans express any willingness to pay for AI editing tools. Of that, freemium-to-paid conversion for casual consumers runs 1–5%. For prosumers and working creatives, conversion exceeds 20%.

This points to a different primary persona: the **prosumer or superfan** — someone who shoots multiple shows a month, cares about posting quality, and has some identity or aspiration tied to the output. They experience the same-night posting window as a real deadline, not a nice-to-have. Their willingness-to-pay is materially higher because the tool solves a real recurring pain, not an occasional novelty.

Practical implication: the free tier and the Founding license (Lesson 03) are still valid as acquisition tools, but the *target* who upgrades and retains is the prosumer, not the casual fan. Onboarding, feature emphasis, and pricing anchors should be calibrated to that persona's workflow, not the one-show-a-year hobbyist.

---

## (c) Niche sharper than "AI culling" — the wedge is concert-specific semantic understanding

The broader AI culling / AI video highlight category is crowded (OpusClip, Descript, Captions, generic highlight-reel tools). These are creator-repurposing tools: take a long video, extract shareable clips, often for creator-economy workflows (YouTube → Shorts, podcast → LinkedIn).

EncoreShot's wedge is different in kind, not just degree: **AI that understands a concert.** That means understanding what makes a shot good of a specific artist in a specific performance context — crowd energy, expression, proximity to the peak moment — not just "where are the interesting-sounding parts." The semantic gap between "find the loud parts" and "find the keeper of Beyoncé at the moment the crowd went insane" is the moat (Lesson 09, Concept 2). Competitors optimising for creator-repurposing are not competitors for this job.

Positioning implication: lead with the concert-specific understanding, not the generic culling speed. The speed and volume are table-stakes; the semantic judgment is the differentiator.

---

## (d) Competitors reframed as opportunity

Session also updated how to read the competitor landscape:

- **Features to steal:** proxy-media-style local preview before upload; stagger UX that shows results appearing as scoring progresses rather than a loading spinner. Both are UX wins that cost little to implement.
- **Pricing intel:** AI media tools in the prosumer segment are pricing $10–20/mo for active users, $50–100 lifetime for early cohorts. EncoreShot's Founding license at $39 sits in a credible band.
- **Acquirers, not just competitors:** the companies building in this space (Adobe, Lightroom's parent, creator-tool platforms) are potential acquirers. An architectural decision that keeps the scoring engine modular and the data model clean is also an acqui-hire preparation decision. This is a long-horizon note, not an immediate action.

---

## Connection to curriculum spine

This session was a **deliberate detour** from the business-fundamentals sequence (Lessons 01–08). It feeds the deferred Advisor-mode readiness assessment (planned for early-to-mid July 2026): the architecture clarity and persona sharpening are prerequisite inputs to a meaningful "ready to charge?" evaluation. Resume context in the Advisor-mode session when that runs.

**Prior record:** [0001-starting-point.md](0001-starting-point.md)
