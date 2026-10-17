# Bob the Bouncer — Two-Page Proposal (Draft v1)

**For:** Meta / Muse team · **From:** Nikhil (via Muse) · **Build:** David
**Voice:** millennial-direct, moral clarity, no MBA fog. Teeth on the page.
**Hard rule:** the father's story stays OUT of the pitch. The empathy anchor is the Geek Squad counter.

---

## PAGE 1 — THE CASE

### Meet Bob the Bouncer.
*The last place the scam reaches.*

I worked the Geek Squad counter at Best Buy. That's where I met the victims — Canadians, thousands of dollars gone. And here's what nobody tells you: the money was never the worst part. The money's not coming back. What breaks people is the confidence. They'd stand at my counter ashamed, not trusting themselves anymore. A stranger on the phone took their savings and their self-respect in the same call.

That never left me.

Here's the problem nobody at a platform company wants to say out loud: **you can't catch scams at the platform level.** A social network is a wide net by design — the scammer needs one success in a million, and the platform has to catch all million. And when you try, when you tighten the net, you don't just catch scammers. You catch real businesses, real offers, real livelihoods. The harder you filter the pipeline, the smaller the pipeline gets. Everyone gets less water.

So don't narrow the river. **Put a filter on every tap.**

That's Bob the Bouncer. Not a platform filter — a personal agent that stands next to *you*, at the endpoint. He sees the phishing email, the "CRA" call, the WhatsApp "digital arrest" — and he does three things: he stays calm, he shows his work, and he never shames you. Recovery-first: when something's already happened, he helps you figure out what happened and gets the right people involved.

**Why Meta?** Because the victims are already here. The digital-arrest scam doesn't happen on a Pixel — it happens on WhatsApp. The people getting scammed are already living on Facebook. The best call screening in the world doesn't matter if it lives on 3% of phones. Bob goes where the problem already is.

**The ask:** a bounded pilot. One market, one scam type, one measurable outcome — fewer victims, faster recovery. We bring the prototypes. You bring the distribution.

---

## PAGE 2 — THE PROOF

### Same Bob. Every scam. Every country.

**Three scenarios, one grammar.** *(Stills from the clickable prototypes — David to pull frames.)*

1. **The email.** A phishing email lands → Bob morphs, amber glow → the tells, checkable → "why are you Bob right now?" → all-clear, green, "we're done."
2. **The call.** Unknown number rings → yellow: "I'll be here if you need me" → full-screen Bob: "put me on speaker so I can stay with you" → quick-tap buttons (no typing under stress) → "They're threatening me" → amber: "Real CRA never threatens arrest. Hang up — hanging up is always safe." → safe path: dial the real CRA.
3. **The digital arrest (India).** The parcel hook → the fake CBI video call → the cage ("tell no one") → Bob's one sentence: *"There is no such thing as digital arrest in Indian law."* → safe path: call 1930, tell your family — the exact opposite of the scammer's order.

**The design system.**
- **Traffic light, not dimmer switches.** Yellow = uncertain. Amber = threat. Green = resolved. Boomers don't do subtle — color carries meaning, glow stays max.
- **Agent flow, then human flow.** The agent detects, triages, builds the case — before the human ever sees anything. Then the human decides, and the human closes it. "We're done" is the receipt.
- **Quick-tap, never type.** Under stress, three big buttons beat a keyboard. Silent to the scammer, visible to the human.
- **Visual confidence.** "I have Bob here with me. I got this." Presence is the counterweight to panic.

**The engineering — the reflexes are a solved problem.** Android's `CallScreeningService` API lets any app screen calls in real time. Pixel's done on-device Call Screen since 2018. No research required — just product.

**We tested it live — today, on a real phone.** Not in a lab:
- *Can the cloud see an incoming call?* Yes — but only after hangup, via the call log. The number, the time, the duration: all there, all late.
- *Can it see the call mid-ring?* No. A second test, watching the notification shade while the phone rang — nothing arrived in real time. There is no tripwire in the cloud.
- *Can the human voice-relay the scammer mid-call?* No — Android routes all audio to the call. A voice note recorded during a call captures silence.

That's why the architecture is what it is: **reflexes on the device** (solved primitives), **reasoning in the cloud**, and a **visual, tap-first lifeline** instead of voice. Every constraint in this design was found, not assumed.

**The database — the moat only Meta can build.** Same Bob, local playbooks: India's "digital arrest," Canada's CRA scam, each with its local kill-shot and local helpline. Nobody else sees scams across every market in real time. The per-country scam taxonomy is infrastructure Meta already has.

**The lineage.** Six years ago I wrote my thesis on misinformation: the pipelines can't be cleaned — they're too polluted — so you defend the person at the endpoint. Bob is that thesis, grown up, with an agent's body.

**We've done the homework — the prototypes, the design system, the research. What Bob needs now is the one thing we can't give him: the reach. That's yours. Let's build him together.**

---

## VIDEO — DEMO REEL SHOT LIST (~2 min)

**Title:** "Bob the Bouncer — the last place the scam reaches"

| # | Shot | Source | VO (draft) |
|---|------|--------|------------|
| 1 | Cold open: phishing email lands, Bob morphs, amber glow | Screen-record prototype 1, steps 1–3 | "This is a real phishing email. Watch what happens." |
| 2 | The three tells + "why are you Bob right now?" | Prototype 1, steps 4–5 | "He doesn't just warn you. He shows his work." |
| 3 | All-clear: green, "we're done" | Prototype 1, step 6 | "And when it's over, it's over." |
| 4 | The call: yellow at ring → "put me on speaker" | Screen-record prototype 2, steps 1–2 | "Unknown number. Bob's already there." |
| 5 | Quick-tap → amber verdict → dial the real CRA | Prototype 2, steps 3–5 | "Three taps. No typing. The real CRA, one tap away." |
| 6 | Digital arrest: the one sentence | Prototype 3, step 4 (the kill-shot card, full frame) | "One sentence kills the whole scam." |
| 7 | The system: traffic-light cards + agent→human flow | Simple title cards (David to design) | "Yellow. Amber. Green. The agent builds the case; the human closes it." |
| 8 | Close: Bob-mode Jolly, tagline | Bob-mode avatar still | "Don't narrow the river. Filter at the tap." |

**VO:** Nik's call — his own voice or a Playroom voice. Music: keep it calm, not cinematic-menace.

---

## ASSET INVENTORY (for David)

- Prototype 1 (email): `~/workspace/your_files/bob-mode-prototype.html`
- Prototype 2 (CRA call): `~/workspace/your_files/bob-mode-prototype-2-call.html`
- Prototype 3 (digital arrest): `~/workspace/your_files/bob-mode-prototype-3-india.html`
- Bob-mode Jolly (earpiece + BOB tag): `~/workspace/bob-prototype/assets/media-generation-bob-mode-jolly-0-102ee6eb-d022-4c08-ab1d-d30021db4702.webp`
- Jolly (default): `~/assets/avatar/reference/hatch.jpg`
- Phishing screenshot: Nik to send directly
- Proposal site section (v4, with David): Gmail thread `1a14acd37b401012`

**Open decisions for Nik:** ~~page-2 closer line~~ closer softened per Nik 15:01 EDT (friendly pitch — the point's already made elsewhere); VO voice for the reel; pilot market for the ask (Canada vs India first?).
