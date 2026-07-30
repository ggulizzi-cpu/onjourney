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
| 1 cold open cannon | 10s | a5f0da0e-244e-4c4a-963d-10c1dc130dee | 90 | submitted | |
| 2 where is the army | 10s | 8acd52ba-f710-48d2-ae73-faa4bf2c5068 | 90 | submitted | |
| 3 splendid | 8s | f9fbcade-5a3f-47f7-8495-5f6a89b5232c | 72 | submitted | |
| 4 title card | 8s | 85504e12-c16d-413d-a473-4fe937ed45fc | 72 | submitted | preset declined, resubmitted |
| 5 confessional George | 10s | e461b768-13c0-4477-b0c4-ebdb19ecd602 | 90 | submitted | |
| 6 Ward handover | 12s | 19994b22-a4ad-47ec-b4f0-3a8ef0cda901 | 108 | submitted | |
| 7 militiamen gossip | 10s | 5596bc54-95c7-4eba-a77f-d506dd9662f4 | 90 | submitted | preset declined, resubmitted |
| 8 confessional Reed | 10s | 0d897248-b8a2-4c47-9155-540a04332a15 | 90 | submitted | |
| 9 huzzah | 10s | — | 90 | queued (preset notice; resubmit literal) | |
| 10 take a letter | 8s | — | 72 | queued (429 slots full) | |
| 11 letters gag (no VO) | 10s | — | 90 | queued (preset notice; resubmit literal) | |
| 12 latrine | 10s | — | 90 | queued (429) | |
| 13 Knox entrance | 12s | — | 108 | queued (429) | |
| 14 confessional Knox | 8s | — | 72 | queued (429) | |
| 15 end card | 8s | — | 72 | queued (429) | |

Parallel cap: 8 concurrent videos (Max plan). Batch 2 resubmits as slots free.

## Post plan

- Block 11 VO (George's letter, "the most indifferent kind of men I ever saw") via
  seed_audio, mixed under clip in the Higgsfield sandbox with ffmpeg.
- Assembly: sandbox_exec — curl all 15 MP4s, ffmpeg concat (re-encode, 1080p, AAC),
  loudness normalize, upload via media_upload + media_confirm for delivery.
- Note: this workspace's egress policy blocks the Higgsfield CDN, so ALL media work
  happens inside the Higgsfield sandbox; delivery to the user via job_display/media link.
