# Production — E001 Act I · seedance_2_0 std 1080p 16:9 · est 1,296 cr (144s @ 9/s)

Balance at shoot start: 1,559.7 · Casting: 5 × soul_cast ≈ 0.6 cr total

## Cast reference job IDs (locked for the series)

| Character | Job ID |
|---|---|
| George Washington | 88b33146-9246-4bda-a84a-7e59fcb8d3eb |
| Joseph Reed | ad42ce72-b58b-4cf8-b7e4-38adea56ba17 |
| Henry Knox | 30b39dd2-ccc7-4bb5-8a5e-bc7167d97afc |
| Artemas Ward | 21428033-9518-4c69-865b-b2e8c108347b |
| Cannon Militiaman | 83d30b54-1732-40e0-83c4-81e85f5d10e8 |

## Shot jobs

| block | len | job id | credits | status | notes |
|---|---|---|---|---|---|
| 1 cold open cannon | 10s | a5f0da0e-244e-4c4a-963d-10c1dc130dee | 90 | done | |
| 2 where is the army | 10s | 8acd52ba-f710-48d2-ae73-faa4bf2c5068 | 90 | done | |
| 3 splendid | 8s | f9fbcade-5a3f-47f7-8495-5f6a89b5232c | 72 | done | |
| 4 title card | 8s | 85504e12-c16d-413d-a473-4fe937ed45fc | 72 | done | preset declined, resubmitted |
| 5 confessional George | 10s | e461b768-13c0-4477-b0c4-ebdb19ecd602 | 90 | done | |
| 6 Ward handover | 12s | 19994b22-a4ad-47ec-b4f0-3a8ef0cda901 | 108 | done | |
| 7 militiamen gossip | 10s | 5596bc54-95c7-4eba-a77f-d506dd9662f4 | 90 | done | preset declined, resubmitted |
| 8 confessional Reed | 10s | 0d897248-b8a2-4c47-9155-540a04332a15 | 90 | done | |
| 9 huzzah | 10s | caf2e5d9-4bdb-4299-b781-38beaff271cc | 90 | done | |
| 10 take a letter | 8s | e8d19bb6-52b4-48c6-80c5-7a01e843c196 | 72 | done | |
| 11 letters gag (no VO) | 10s | d4d38cb2-bc09-471e-b707-622b52a6be66 | 90 | done | |
| 12 latrine | 10s | 31e2d757-c7ba-455f-b61d-43a3c3645c3a | 90 | done | |
| 13 Knox entrance | 12s | f588216c-3721-42ec-9bfd-9155ae2434f4 | 108 | done | |
| 14 confessional Knox | 8s | 78b86f8f-75ff-41b3-b716-3c0aff7bdf18 | 72 | done | |
| 15 end card | 8s | 02dbdd28-c205-4846-bce3-6070bc577b63 | 72 | done | |

Parallel cap: 8 concurrent videos (Max plan). Batch 2 resubmits as slots free.

## Audio jobs

| item | voice | job id | status |
|---|---|---|---|
| Block 11 VO (George's letter) | Arthur (preset 30fc8796), rate -8 | 861382da-f477-4f02-a3e2-f1715040481b | done |

## Post plan

- Block 11 VO (George's letter, "the most indifferent kind of men I ever saw") via
  seed_audio, mixed under clip in the Higgsfield sandbox with ffmpeg.
- Assembly: sandbox_exec — curl all 15 MP4s, ffmpeg concat (re-encode, 1080p, AAC),
  loudness normalize, upload via media_upload + media_confirm for delivery.
- Note: this workspace's egress policy blocks the Higgsfield CDN, so ALL media work
  happens inside the Higgsfield sandbox; delivery to the user via job_display/media link.

## Act I wrap — 2026-07-30

- All 15 shots completed on first take. Zero failed generations, zero retries.
- Final cut: 2:25 (145.1s), 1920x1080, 105 MB. Assembled in the Higgsfield sandbox:
  per-clip normalize (h264 crf18 / 24fps / aac 48k), Arthur VO tempo-fit + mixed under
  block 11 at -10dB ambience, concat, loudnorm (-16 LUFS), uploaded to Higgsfield media.
- Final media_id: 33f03595-54c8-4eb9-91f2-ca0de7740ba4
- URL: https://d2ol7oe51mr4n9.cloudfront.net/user_31undoF7i6cu3qRde6al7QsmiT3/33f03595-54c8-4eb9-91f2-ca0de7740ba4.mp4

## Ledger

| item | credits |
|---|---|
| Casting: 5 soul_cast portraits | ~0.6 |
| 15 Seedance 2.0 clips (144s @ 9/s) | 1,296 |
| Block 11 VO (seed_audio) | ~0.8 |
| **Total** | **~1,297.4** |

Balance: 1,559.7 → 262.3. Act II (blocks 16–30, ~151s ≈ 1,360 cr) needs a top-up.

## Sound pass v2 — 2026-07-30

User note: add background ambience, SFX weight, and music. Platform has no standalone
music/SFX model, so:
- Camp ambience bed extracted free from block 1's native audio (pre-boom camp murmur),
  looped, laid under the four exterior stretches (0–28, 46–68, 78–96, 106–128) at low level.
- Two music cues generated as cheap Seedance audio-carrier clips (480p fast, audio ripped):
  fife-and-drum march (19f04772, 15 cr) under the opening camp reveal (fades out before
  dialogue), sneaky baroque harpsichord (a9fbe6f6, 22.5 cr) under latrine + Knox (106–127).
- Master chain: highpass 35Hz, +2.5dB low shelf @95Hz (cannon weight), 2:1 compression,
  loudnorm -16 LUFS. Confessionals and sincere beats stay dry per the bible's Office rule.
- Sound-mix media_id: bee28fcd-8190-47fa-be2c-b1a6a192613d
- URL: https://d2ol7oe51mr4n9.cloudfront.net/user_31undoF7i6cu3qRde6al7QsmiT3/bee28fcd-8190-47fa-be2c-b1a6a192613d.mp4
- Sound pass cost: ~37.5 cr. Balance: 262.3 → 224.8.

## QC pass v3 — 2026-07-30

Scene-by-scene video analysis (job fd14ea0b) + frame review. Findings:
- Title card correct ("HIS EXCELLENCY"), cast faces consistent, all dialogue verbatim.
- FIXED: end card text stutter ("ACT II / ACT II COMING SOON") — replaced last 8s of
  video with a nano_banana still (verified spelling) + Ken Burns push + fades; original
  fife outro audio kept untouched. v3 media_id: 2c09eb90-ad25-4141-ab58-719e01d43004
  URL: https://d2ol7oe51mr4n9.cloudfront.net/user_31undoF7i6cu3qRde6al7QsmiT3/2c09eb90-ad25-4141-ab58-719e01d43004.mp4
- KNOWN, unfixed (await call): block 11 letters gag — British red-uniform handshake at
  1:38 + stray pointing hand at 1:41 (re-roll ~90 cr); block 9 huzzah — Washington's
  line-half mouthed by tankard officer (re-roll ~90 cr, or keep: reaction cut plays).
- QC cost: end card image ~2 cr. Balance ~222.

## v4 rebuild — 2026-07-30

User flagged: audio massively delayed in second half + stutters, lip-sync issues,
voice inconsistency (George), 1-second internal cuts, screen-position continuity,
toothpick/pipe hallucinations.

Root cause of the drift (post bug, mine): assembly used concat demuxer with -c copy,
which accumulates AAC priming-gap error at every joint (~15 joints), so audio lag grows
through the video and compounds perceived lip-sync error.

Fix in v4: single filter_complex concat over all 15 blocks; every segment hard-locked
to its scripted duration (video trim + audio apad/atrim to exactly 10/10/8/8/10/12/...),
async-resampled audio, VO + music + ambience re-laid at exact nominal timestamps,
corrected end card, master chain. Result: exactly 144.000s, drift structurally impossible.
v4 media_id: 75bed673-d68d-42e1-b432-8362a42f1489
URL: https://d2ol7oe51mr4n9.cloudfront.net/user_31undoF7i6cu3qRde6al7QsmiT3/75bed673-d68d-42e1-b432-8362a42f1489.mp4

Generation-level defects (not fixable in post; pipeline changes for Act II + re-rolls):
1. George voice differs per clip → record one George voice sample, attach as
   audio_references to every clip he speaks in (Seedance supports voice-reference).
2. In-clip lip-sync wobble → shorter lines per shot, one speaker per internal cut.
3. 1-second internal cuts → max 2 internal cuts per block, explicit per-cut durations.
4. Screen-side continuity → lock screen direction in prompts (George frame-left etc.)
   and reuse an establishing still per location as image reference.
5. Prop hallucinations (pipes/toothpicks) → explicit negative lines in every prompt.

## v5 — 2026-07-30

User flagged on v4: (a) cannon boom repeating ~every 5s all video; (b) second half feels
slow "like fps change".

Diagnosis:
(a) Confirmed via waveform scan: boom peaks at sec 4-6 of block 1; the v2 ambience bed
    slice (0.4-5.6s) included it, looped every 5.2s under four stretches. Fixed: bed now
    cut from verified-quiet 0.3-3.3s window (max -22dB), volume lowered to 0.13.
(b) FPS probe: ALL 15 clips native 24fps (batch 1 and 2 identical) — no frame-rate
    fault. The slow feel is in-clip slow-motion rendered by Seedance in later blocks.
    Treated in post: 1.1x time-compression (video setpts + audio atempo, pitch kept) on
    blocks 9-13; VO tempo adjusted to fit; music/bed timestamps recomputed. Knox
    confessional + end card untouched. New runtime 2:19.5 (139.5s).

v5 media_id: 0f0d7378-a16b-400a-a218-df943e8322cd
URL: https://d2ol7oe51mr4n9.cloudfront.net/user_31undoF7i6cu3qRde6al7QsmiT3/0f0d7378-a16b-400a-a218-df943e8322cd.mp4
Cost: 0 credits (post only).

## v6 — 2026-07-30

User: v5 ambience/SFX almost inaudible — wanted middle ground vs v4's cannon loop.
Cause: new bed source slice is ~20dB quieter content than the boomy v2 slice AND the
fader was lowered — double reduction. v6: same boom-free slice (0.3-3.5s), gain restored
to effective v2-era presence (bed 0.85 exteriors / 0.70 under harpsichord, ~16dB up from
v5), harpsichord 0.22→0.26. All else identical to v5.
v6 media_id: 7ac65be9-4704-498d-845a-64b7db7521b3
URL: https://d2ol7oe51mr4n9.cloudfront.net/user_31undoF7i6cu3qRde6al7QsmiT3/7ac65be9-4704-498d-845a-64b7db7521b3.mp4
Cost: 0 credits.

## Act II validation shoot — 2026-07-31

Ultra plan active (balance 6,015 at start). New pipeline per seedance-shotlist-director
skill + logged Act I lessons. Prep: Lee portrait f9bd20dd, Gates portrait 2ebbfc13,
George voice ref extracted from Act I confessional (audio media c5b1aa9e), location
stills from Act I frames (trench e0f77f81, camp lane 8db4dc15).

Validation clips (15s, 1080p std, 135 cr each; voice + location + character refs attached):
| scene | job id | status |
|---|---|---|
| II-1 Chain of command (Ezekiel) | d1b8af67-f981-4dfb-bc32-c8a008bc4988 | done |
| II-2a Lee arrives (dogs first) | 4226b1dc-9ae4-4a36-83d4-f641c309f54f | done |

URLs:
https://d8j0ntlcm91z4.cloudfront.net/user_31undoF7i6cu3qRde6al7QsmiT3/hf_20260731_123307_d1b8af67-f981-4dfb-bc32-c8a008bc4988.mp4
https://d8j0ntlcm91z4.cloudfront.net/user_31undoF7i6cu3qRde6al7QsmiT3/hf_20260731_123232_4226b1dc-9ae4-4a36-83d4-f641c309f54f.mp4

Spend: ~271 cr (2 clips + 2 portraits). Gate: user judges vs Act I before batch-shooting
the remaining Act II scenes (~9 scenes ≈ 1,200 cr).

Verdict: II-1 approved enthusiastically. II-2a notes — dogs bark in audio without barking
on camera, motion snappy/not smooth, lip-sync imperfect, SFX thin. Fixes encoded into the
Style Prefix rev. 2 (Motion fluidity clause + Sound-truth rule: every sound has a visible
or explicit off-screen source; animals quiet unless shown vocalizing).

## Act II full shoot — 2026-07-31

All prompts per seedance-shotlist-director format, Style Prefix rev. 2. 15s / 1080p std /
16:9 / genre comedy (II-11 auto) / 135 cr each. George's voice locked via audio_references
(c5b1aa9e) on every clip he speaks in. Full as-shot prompt text: shotlist-act2.html.

Batch A (8 jobs — all completed first take):
| scene | job id | notes |
|---|---|---|
| II-2a Lee arrives (re-roll, silent dogs) | 15fe2cbc-9e03-40d2-82ea-4b5f92c23085 | replaces 4226b1dc |
| II-2b "Some taken." | 2a2df71a-0e79-47b0-9948-36285f7445df | |
| II-3 Lee confessional (dog barks ON camera → "Six.") | 57fa5de0-33e4-49dd-aba1-b3464d0665fe | |
| II-4 Rum mutiny ("NON-NEGOTIABLE") | 847aebaa-2682-4fc7-b12d-3085b115a31d | |
| II-5 George confessional ("lost a vote") | 7678d042-9c7e-4d76-9ab7-7c0e953f51ab | |
| II-6 Geese / powder | 1e2d9b04-070d-4015-9bf9-3a2490eb2e12 | |
| II-7 War room Gates ("Nine rounds each. Ish.") | 372f2b24-ece9-45b0-b3eb-d4c81187a7c2 | |
| II-8 The Silence (unbroken push-in) | 1e15beee-cd7c-4068-992e-58560e1ba3b5 | |

Batch B (5 jobs, fired 14:26Z):
| scene | job id | notes |
|---|---|---|
| II-9 Reed confessional ("nine bullets a man") | 684b1b33-da01-4b89-8667-e2da3b149013 | |
| II-10 "We bluff." (George face-away for long line) | c8d1a45a-4ded-4576-babd-fdfda68d5763 | |
| II-11 Letter to Martha (silent; VO in post) | 35febfe3-d7c3-4076-881f-3309a7c6b5af | genre auto |
| II-12 Dawn cannon tag | 2dc7c4a6-7066-49be-877b-a1e8cc7b46a6 | cannon still ref 55826bdf |
| II-13 Final George confessional ("It will have to do.") | ddbfe572-eb8e-4b11-b88c-d595e13db4dc | |

Prep / post assets:
- Martha-letter VO (Arthur preset, natural pace): c7cc0453 — raw 24.4s; silence-tightened
  + atempo 1.07 → 18.75s. Plan: bridge across II-10 tail → II-11 → II-12 quiet dawn open,
  postscript landing just before the cannon (joke rhythm). Insurance brisker take: 065ae19f.
- Soft period-strings underscore carrier (480p fast 15s): dc4280b5 (audio verified present).
- "END OF EPISODE ONE" nano_banana card: 84c7a9cd — spelling verified via sandbox relay.
- Cannon still for II-12 extracted from Act I block 1 @8s: media 55826bdf.

Cost: 13 × 135 = 1,755 cr (incl. II-2a re-roll) + carrier/card/VO ~25 cr.
