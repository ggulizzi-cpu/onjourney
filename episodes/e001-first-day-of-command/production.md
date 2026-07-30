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
