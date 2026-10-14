# SHIRMANI SUPREME HUMAN-PRESENTATION SYSTEM

Status: **Architecture/specification drafted; production integration not yet verified.**

## Purpose
Create an accessible Hindi/English digital presenter using owner-authorized photo, voice, and video assets. The presenter should communicate simply, respectfully, transparently, and with evidence-aware answers.

## End-to-end chain
Voice input → speech-to-text → language/context understanding → intent → evidence gate → response → authorized text-to-speech/voice → avatar/facial animation → lip-sync → presentation → audit → improvement.

## Evidence states
- **VERIFIED** — supported by sufficient independent evidence.
- **SOURCE-BASED** — credible source found; independent verification is incomplete.
- **PHILOSOPHICAL / IDENTITY** — personal viewpoint or self-description; not to be presented as scientific fact.
- **INSUFFICIENT EVIDENCE** — say: “अभी पर्याप्त प्रमाण उपलब्ध नहीं है।”

## Presentation requirements
- Use only photo, voice, and video assets the owner is authorized to use.
- Preserve recognizable appearance; do not claim generated lip-sync or voice cloning is a live/verified result until tested.
- Natural gaze, facial movement, and synchronized speech where the chosen provider supports them.
- Adapt formality to the situation, not to caste, religion, or other protected traits.
- Respectful communication across audiences; no belittling of people or communities.
- Disclose that the presenter is AI-generated/AI-assisted where appropriate.

## Provider integration
HeyGen website: https://www.heygen.com/

Keep provider API keys in server-side environment secrets (for example, GitHub Actions Secrets or deployment secrets). Never commit tokens, API keys, passwords, or private credentials to source files, logs, or public issues.

## Verification gates
Before calling the system production-ready, run and record:
1. Speech recognition in Hindi and English.
2. Context and intent understanding.
3. Evidence-state classification, including insufficient evidence.
4. Authorized voice-provider test.
5. Facial movement, gaze, and lip-sync test.
6. Voice/face timing and end-to-end latency.
7. Respectful communication regression tests.
8. Audit record for input, evidence state, response, presentation state, metrics, and test result.

A failed critical test blocks production-ready status.

## Current media pointers
- Owner's video/photo/audio assets were supplied in the ChatGPT conversation; they have **not** been uploaded into this repository by this commit.
- Existing public video/photo gallery linked from the project hub: https://photos.app.goo.gl/hBJ4mN176PboQ7bb6
- Existing Drive media collection: https://drive.google.com/drive/folders/1QRgYwrPteyQfrRbTyDMp4LbBnLv90K66
- Project hub source: https://github.com/rampaulsaini/Nishpaksh-Samaj-Omniverse-Truth

## Next implementation steps
1. Identify the exact target MP4 by filename and duration/size in the Drive/gallery; do not guess a direct media URL.
2. Store authorized media in controlled storage and add only stable, permission-appropriate links here.
3. Configure provider credentials as deployment secrets.
4. Implement a backend adapter and a user-facing presenter UI.
5. Run the verification gates and publish the test report.

## Honest status
This document records the intended architecture and test criteria. It does not claim that HeyGen is connected, that a voice clone has been created, that lip-sync passed, or that the platform is live.
