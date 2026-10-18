# Bob the Bouncer — Demo Package (for David)

**Status:** Final. Voice locked, character locked, architecture locked.
**Date:** 2026-10-17

---

## 1. PROJECT BRIEF

### What Bob is for
Bob the Bouncer is a calm, human-centered anti-scam agent. The premise: scams can't be stopped at the platform level. A social network is a wide net by design — the scammer needs one success in a million, the platform has to catch all million. So instead of policing the net, Bob stands next to the person at the endpoint — the last place the scam reaches.

Bob has two jobs. **On duty:** when something happens, he's there — calm, showing his work, getting the right institutions involved. **Off duty:** he teaches. Short, plain-spoken inoculation — the tells, the patterns, the one sentence that kills each scam — before the call ever comes. A user who's seen the playbook is a harder target; education is the cheapest defense there is, and it's the same no-shame voice either way. Each job gets its own video and its own character: full-kit Bob on duty; a distinct teacher character off duty.

### Who it should help
Bob is age-agnostic — scams don't check ID, and neither does he. But he's designed from the boomer outward: if it works for someone under stress, phone to their ear, zero patience for jargon, it works for everyone. That's the design center, not the boundary. Starting with two pilot markets: Canada and India. Built for anyone who's been scammed and lost their confidence — the money is rarely the real wound.

### The core promise
When something happens, Bob helps you figure out what happened, shows his work, and gets the right institutions involved. No shame, ever. The strongest guy in the room is the calmest one.

### What's working vs. simulated in the prototypes
**Working (real):** the interaction grammar — every scenario runs the same 6-step language (calm → signal → Bob mode → evidence → safe path → all-clear). The traffic-light state system (yellow = uncertain, amber = threat, green = resolved). The playbook content: every kill-shot, helpline, and safe path is verified against primary sources (CRA/RCMP/canada.ca; 1930/cybercrime.gov.in). The agent→human handoff logic: the agent builds the case, the human closes it — "we're done" is the receipt.

**Simulated (mocked):** everything is a clickable prototype. No real email ingestion, no live call interception — `CallScreeningService` is the verified real API path, not yet integrated. The "verdicts" are scripted, not detected. The avatar morph is CSS, not live agent state. The voiceover is TTS, not a live voice.

### The story the demo must land
Two things, in order: (1) The scam can't be stopped at the platform — so Bob stands next to the person. (2) One Bob, every language — the same voice, the same calm, in every market. The language menu on the video IS the second point, demonstrated, not claimed.

### Open decisions / facts to verify
- Pilot market for the ask: Canada vs. India first? (Nikhil's call — not needed for the video.)
- Phishing screenshot: Nikhil sends directly (site section, separate from video).
- Integrity-side pitch (Boardy's two-pitch directive: design-lead vs. integrity-lead versions) — follow-up work, not in this video.
- LOCKED — Voice: Affirming Hearth (`avocado_v2:vdc_29090`).
- LOCKED — Character: full-kit Bob (SECURITY cap, shades, BOB THE BOUNCER tee). Concept art already with David; he refines/finalizes.

---

## 2. VIDEO SCRIPT (~2:00, beat-timed)

Narration is **Bob speaking, first person**. Calm, warm, unhurried — ~130 wpm with breathing room. Each language version (EN, MR, FR, ES) is adapted to hit the **same timecodes** — translate the beats, not just the words.

| Time | On screen | Bob (VO) |
|------|-----------|----------|
| 0:00–0:12 | Cold open. Phone at rest (calm inbox). The Shakepay phish lands. Avatar morphs — amber glow. Bob is on duty. | "This is a real phishing email. It landed this morning. Watch what happens." |
| 0:12–0:30 | The three tells appear, one by one. Then: "Why are you Bob right now?" — Bob answers with the evidence. | "I don't just warn you. I show my work. Wrong sender. Generic greeting. Shady link. Ask me why — I'll always answer with evidence, never authority." |
| 0:30–0:40 | All-clear. Green. "We're done." Glow fades. | "And when it's over, it's over. We're done." |
| 0:40–0:55 | A call comes in. Unknown number — yellow. Bob pops over the call screen. | "Unknown number. I'm already here. Put me on speaker, so I can stay with you." |
| 0:55–1:15 | Quick-tap buttons (no typing). "They're threatening me" → amber verdict. | "Three taps. No typing — typing under stress is too much to ask. And hear this: the real CRA never threatens arrest. Ever. Hang up. Hanging up is always safe." |
| 1:15–1:20 | Safe path: the real CRA number, one tap away. Green. | "The real number. One tap away." |
| 1:20–1:40 | India. The fake CBI video call — uniform, fake warrant, the cage. Then the kill-shot, full frame. | "In India, the scam wears a uniform. So hear this in plain words: there is no such thing as digital arrest in Indian law. Real police never arrest anyone over a video call." |
| 1:40–1:50 | The system, as simple cards: yellow / amber / green. Agent→human flow. | "Yellow means I'm watching. Amber means I found something. Green means we're done. I build the case — you close it." |
| 1:50–2:00 | Full-kit Bob, full frame. Tagline card. Language menu visible. | "I'm Bob the Bouncer. I stand at the last place the scam reaches — right next to you. Don't narrow the river. Filter at the tap." |

---

## 3. SHOT LIST (revised)

| # | Shot | Source |
|---|------|--------|
| 1 | Cold open: phish lands, Bob morphs, amber | Screen-record prototype 1 (fixed file), steps 1–3 |
| 2 | Three tells + "why are you Bob right now?" | Prototype 1, steps 4–5 |
| 3 | All-clear: green, "we're done" | Prototype 1, step 6 |
| 4 | The call: yellow at ring → "put me on speaker" | Screen-record prototype 2, steps 1–2 |
| 5 | Quick-tap → amber verdict → real CRA number | Prototype 2, steps 3–5 |
| 6 | Digital arrest: the one sentence, full frame | Prototype 3 — the kill-shot card |
| 7 | The system: traffic-light cards + agent→human flow | Simple title cards (David to design) |
| 8 | Close: full-kit Bob + tagline + language menu | Final Bob character art (David) |

**Source files (all with David):**
- Prototype 1 (email, timer-race fixed): `~/workspace/your_files/bob-mode-prototype.html`
- Prototype 2 (CRA call): `~/workspace/your_files/bob-mode-prototype-2-call.html`
- Prototype 3 (digital arrest): `~/workspace/your_files/bob-mode-prototype-3-india.html`
- Full-kit Bob concept: `~/workspace/bob-prototype/assets/media-generation-bob-security-full-kit-0-ab3b346e-08dd-4878-80dd-7fd55a857233.webp`

---

## 4. PRODUCTION ARCHITECTURE — ONE VIDEO, N AUDIOS

Render **one** video master. Produce **one audio track per language** (EN, MR, FR, ES to start), synced to the same timecodes. The viewer picks a language from a menu; the audio swaps underneath. Adding a language = adding an audio track, never re-rendering video.

**Two hard constraints for David:**
1. **Beat-timed script.** Translations don't run the same length — each language VO is performed/mixed to the timecodes above, not just translated. Same visual cues land at the same timestamps in every language.
2. **Language-agnostic video master.** No burned-in text anywhere. All on-screen text as overlay/subtitle layers per language — otherwise French audio plays over English captions and the illusion breaks.

**VO production:** Muse renders each language track in the locked Bob voice once the script text is final; David cuts it under the master.

## 5. VO DIRECTION

- **One voice, every language:** Affirming Hearth (`avocado_v2:vdc_29090`) — deep, resonant, warm. Manly but warm, never threatening. Calm authority; the power is that he never raises his voice.
- **Languages:** English, Marathi, French, Spanish (in that order).
- **Delivery:** unhurried, plain-spoken, no drama. Bob de-escalates — including in his read.
- **Multilingual bar:** the same character must be recognizable in every language. If a language take sounds like a different person, it's a bad take.
