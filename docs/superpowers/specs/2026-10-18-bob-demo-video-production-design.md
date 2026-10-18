# Bob the Bouncer Demo Video — Production Design

**Status:** Proposed design for owner review

**Decision recorded:** Hybrid 16:9 production package approved by the owner

**Scope boundary:** Preparation only. No video generation or rendering in this phase.

## Goal

Prepare a clear, accessible demo video for Bob the Bouncer that can serve as the feature's front door. The video should make the value legible to people who are less comfortable with technology: pause, see why something is concerning, choose a safe next step, and remain in control.

The production source of truth stays in the `muse-proposal` repository. The `teambotics-website` repository may serve its published site, but it is not the home for the production package.

## Approved production direction

Use a hybrid 16:9 workflow:

1. Capture the existing Bob prototypes for accurate product interaction and interface layout.
2. Generate supporting human-scale motion or transition shots with a local video model on the owner's other device.
3. Add interface labels, captions, localized copy, and other readable text as editable overlays in a later deterministic edit. Do not rely on generated video to render accurate UI text.
4. Keep prompts and project instructions model-neutral until the owner identifies the local video model and workflow.

This preserves exact product behavior where it matters while leaving room for generated connective footage. The current target duration of about two minutes is provisional; the final runtime follows the reviewed script and actual performance.

## Story and visual direction

Use the approved storyboard in `docs/bob-demo-visual-storyboard-v1.md` as the current story order: ordinary morning, suspicious email, evidence, safe action, unknown call, simple choices, digital-arrest scam, three-state explanation, and an agency-focused close.

Production rules:

- Keep one focus per shot, large touch targets, generous reading time, and calm camera movement.
- Use the locked full-kit Bob design throughout. Preserve character proportions and visual continuity between generated shots and prototype captures.
- Use yellow, amber, and green with distinct icons and labels; never make meaning depend on color alone.
- Keep the emotional arc calm and reassuring. Do not use panic imagery, alarm graphics, threatening stings, or hacker clichés.
- Clearly mark prototype screens as a demo. Do not imply live email ingestion, call interception, or automated verdicts.
- The user, not Bob, chooses and completes the action and closes the case.
- Keep all language-specific interface copy and captions replaceable.

## Voice, script, and timing

The voice decision is one consistent voice identity across English, Marathi, French, and Spanish. Do not add character voices or switch voice identities within a language track.

The current Drive MP3s are performance previews, not a synchronized final narration set. The production notes record approximate lengths of 51.3 seconds (EN), 56.3 seconds (MR), 69.2 seconds (FR), and 65.9 seconds (ES). Existing automatic transcripts are unverified and are not suitable for captions. Do not assume the older two-minute timing map fits these recordings.

Before a timed edit is prepared, the final script must be reviewed, each language's narration confirmed or recorded, and beat cues mapped to the actual performances. Captions and subtitle files must be derived from reviewed transcripts. The package should preserve the approved voice identity and allow per-language timing differences without forcing all languages into one duration.

## Source material and in-house tool boundaries

Keep new canonical production documents and manifests in `muse-proposal` and reference existing assets by repository path.

- **Legion-PanelForge:** Useful for character-consistent still frames and key art. It is not a video renderer. A dedicated Bob reference may anchor stills used by the later motion workflow.
- **ComicBotics:** Useful for visual direction, continuity, and still-image production planning. Its current proven capabilities do not include video rendering.
- **Audio Studio:** Useful as a reference for segmented narration, provenance, validation, deterministic assembly, and human listening review. Its current voice setup does not establish that the locked Muse voice can be generated in all four languages; do not route the final voice production through it without confirming that capability.

No changes to those repositories, adoption of their dependencies, or assumption that they can render video is included in this design.

## Claims and source discipline

Narration and visible product copy must distinguish advice from product capabilities and must not overstate legal or security facts. Before a factual scam or government-contact claim is approved for the script, verify its exact wording against a current primary source for the relevant locale. Recheck official contact routes at script lock; do not place unverified numbers in artwork or overlays.

Initial primary-source references for claim review:

- Canada Revenue Agency, [Recognize a scam](https://www.canada.ca/en/revenue-agency/corporate/scams-fraud/recognize-scam.html)
- Canada Revenue Agency, [Verify it's the CRA calling](https://www.canada.ca/en/revenue-agency/corporate/scams-fraud/verify-cra-contact.html)
- Press Information Bureau of India, [CBI warns public about digital-arrest scams](https://www.pib.gov.in/PressReleasePage.aspx?PRID=2261539&lang=2&reg=3)
- Press Information Bureau of India, [Prime Minister's address on digital-arrest scams](https://www.pib.gov.in/PressReleasePage.aspx?PRID=2068698&lang=2&reg=48)

These links are research leads, not approval of specific script lines. Localized wording and each claim's scope still require review before publication.

## Production package proposed for the next phase

After this design is approved and an implementation plan is approved, prepare:

- A concise creative brief and a reviewed master script with localized script variants.
- A retimed shot-by-shot storyboard with prototype capture instructions and generated-shot descriptions.
- An asset manifest that records source, intended use, language, and continuity notes.
- Bob reference and continuity guidance for still/keyframe creation and later local video generation.
- A narration beat map, reviewed transcript/caption plan, and editable subtitle/overlay plan.
- Edit, sound, accessibility, and export handoff notes.

These are handoff materials only. They do not include generated shots, rendered video, or a model-specific workflow file.

## Inputs to settle before the later render phase

- Which local video model, device, and workflow will be used.
- Whether the current voice previews will be replaced or confirmed as final reads.
- Final language coverage and reviewed translations/transcripts.
- Delivery settings beyond the approved 16:9 aspect ratio, including resolution, frame rate, and any platform-specific versions.
- The exact official contact path and final wording of any legal or scam-prevention claims shown.

Until those inputs are known, visual prompts stay model-neutral and timing/export values stay explicitly provisional.

## Acceptance criteria for this design

- The production package has one canonical home in `muse-proposal` and can be served through the existing site arrangement.
- Product actions come from prototype captures; generated footage is supporting material.
- Readable UI, subtitles, and localized text remain editable after video generation.
- One voice identity is preserved across the approved languages, with timing based on reviewed final performances.
- The story presents Bob as calm, explanatory, and user-directed, with no unsupported integration or detection claims.
- No video is generated or rendered as part of design approval or package preparation.
- Every factual public claim has a current primary source and reviewed wording before script lock.
