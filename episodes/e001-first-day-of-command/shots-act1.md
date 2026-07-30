# E001 Act I — Shot list & Seedance prompts

**Scope:** blocks 1–14 of the script + Act-break end card = 15 generations, ~144s.
**Spec:** `seedance_2_0` · std · 1080p · 16:9 · native audio ON · genre: comedy.
**Character references:** locked cast portraits attached as `image_references` per shot.
**Voice direction (baked into every dialogue prompt):** dry, deadpan, naturalistic
documentary sitcom delivery — never announcer-like, never theatrical.

Global style header used in every prompt:

> Ultra-realistic cinematic mockumentary, 1775 American Revolutionary War, Cambridge
> Massachusetts. Documentary handheld camera language, 35mm film texture, natural
> light, authentic colonial costumes and props only — no modern objects. Comedic
> deadpan tone like The Office.

| # | Len | Cast refs | Beat |
|---|-----|-----------|------|
| 1 | 10s | Militiaman | Cold open: camp reveal, cannon self-fires |
| 2 | 10s | George, Reed | "Where is the army?" |
| 3 | 8s | George | "Splendid." snap-zoom |
| 4 | 8s | — | TITLE CARD: HIS EXCELLENCY + fife sting |
| 5 | 10s | George | Confessional: "No one else thought to." |
| 6 | 12s | George, Ward | Handover: "I'm going to go lie down." |
| 7 | 10s | — | Militiamen gossip: "A southerner?" |
| 8 | 10s | Reed | Confessional: "He has been here one hour." |
| 9 | 10s | George | Officers address, ragged huzzah |
| 10 | 8s | George, Reed | "Take a letter." |
| 11 | 10s | George | Letters gag (VO overlaid in post) |
| 12 | 10s | George, Reed | Kitchen/latrine trench |
| 13 | 12s | George, Knox | Knox's entrance |
| 14 | 8s | Knox | Confessional: "…through reading." |
| 15 | 8s | — | END CARD: "END OF ACT I — ACT II COMING SOON" |

**Post plan:** block 11 gets a seed_audio voiceover (George's letter voice) mixed under
the clip's ambience in ffmpeg; quill-scratch bed retained from native audio.
Assembly: ffmpeg concat 1→15, loudness normalize, deliver MP4.
