# HIS EXCELLENCY — Series Bible (v1)

A cinematic, ultra-realistic mockumentary sitcom about George Washington and the
Continental Army, from the first day of the Revolutionary War onward.

**Format:** 5-minute episodes · hundreds of them · YouTube
**DNA:** The Office (US) mockumentary grammar · South Park irreverence · early-Simpsons
joke quality, integrity, and catharsis
**Look:** Ultra-photoreal period film. 1775 is rendered dead straight — costumes, light,
mud, muskets. Nothing anachronistic is ever on screen.

---

## The premise

An unexplained documentary crew is embedded with the Continental Army starting July 1775.
No one ever questions why. The war is real, the stakes are real, the history is real —
but the army is also the worst-run workplace in North America, and George Washington is
the new regional manager of the American Revolution.

## The comedy engine

**Period-real world, modern office soul.** Everything visible is authentic 1775. The
comedy comes from behavior: staff meetings, passive-aggressive memos (by courier),
performance reviews of militiamen, interdepartmental beef (Virginia vs. New England),
a boss obsessed with decorum commanding people who vote on whether to obey him.

Truth is the best writer on staff: the powder shortage, elected officers, the rum
ration, Lee's dogs, Knox the bookseller — all real. **Rule: compress history, never
falsify it past comedy tolerance.** Every episode ends with a historical-notes block in
its script file listing what's documented vs. compressed.

## Mockumentary grammar

- Talking-head confessionals (subject seated, direct address, shallow focus, HQ interior
  or tent backdrop) cut against scenes.
- Handheld coverage, snap zooms, push-ins on reactions.
- Characters glance at the lens. Reed is the primary camera-look character (the Jim).
- The crew is never acknowledged in dialogue. Ever.

## Tone rules (the early-Simpsons clause)

1. Every episode has a real emotional floor — one sincere beat, earned, never mocked.
2. Historical figures get roasted for ego, hypocrisy, and pettiness — but they stay
   human and stay competent enough to explain why history happened.
3. No joke survives if it requires the characters to be stupid. They're flawed, not dumb.
4. PG-13. War is present but not gratuitous. Death is treated with weight when shown.
5. Catharsis is mandatory. The last 60 seconds pay something off emotionally.

## Core cast (season one)

| Character | Age | Office archetype | The real hook |
|---|---|---|---|
| **George Washington** | 43 | The boss — competent but vain, image-obsessed, secretly insecure | Wore his uniform to Congress "just in case." Says polite things aloud, writes savage letters at night. Wants to be loved AND obeyed; will settle for obeyed. |
| **Joseph Reed** | 33 | The Jim — George's secretary/aide, wry, camera-look guy | Philadelphia lawyer who keeps drafting resignation letters he never sends. Sees everything. |
| **Charles Lee** | 44 | The passed-over rival — brilliant, feral, no filter | Actual European war experience, travels with a pack of dogs, refers to himself in the third person. Openly believes he should have the job. |
| **Henry Knox** | 25 | The golden retriever — pure enthusiasm, zero credentials | Boston bookseller who learned artillery from books. The British are using his shop as a stable. Will one day drag 60 tons of cannon across Massachusetts, because nobody told him it was impossible. |
| **Horatio Gates** | 47 | The Toby — adjutant general, loves forms, kills every vibe | Delivers catastrophic news in the tone of a man reading a grocery list. |
| **The Army** | — | The branch office | 14,000 New England militiamen who elected their own officers, negotiate their rum ration collectively, and do not care for Virginians. |

Recurring: Artemas Ward (outgoing boss, just wants to lie down), Martha Washington
(letters only for now — the heart of the show), the Cannon (a camp cannon that misfires;
it is never fixed; it is the show's Jim-face).

## Running gags (established in the pilot)

- **The letters:** George's polite public face hard-cut against voiceover of his real,
  brutal correspondence. (His actual letters are this funny. Use them.)
- **"His Excellency":** everyone deploys the title with a different agenda.
- **Non-negotiable:** the entire camp answering in unison when the rum ration comes up.
- **Lee's dogs:** always one more dog than last time.
- **The Cannon:** misfires at structurally significant moments.
- **"Take a letter":** George's tell that he is furious.

## Episode template (5:00)

| Beat | Length | Job |
|---|---|---|
| Cold open | ~35s | Visual gag + hook, ends on title card |
| Act 1 | ~90s | Premise of the week + confessional introductions |
| Act 2 | ~100s | Escalation, B-plot brush, biggest laughs |
| Act 3 | ~70s | Turn — the real stakes surface; the sincere beat |
| Tag | ~20s | Callback gag + closing confessional |

~28–32 shots of 6–15 seconds. Every shot is one Seedance generation.

## Production spec

- **Video model:** Seedance 2.0 (`seedance_2_0`), `std` mode, **1080p**, 16:9,
  native audio ON (dialogue spoken on camera, lip-synced).
- **Character consistency:** locked cast reference portraits (Soul / Soul Cast),
  attached as `image_references` on every shot that character appears in.
- **Shot duration:** 6–15s per Seedance constraints. Dialogue ≤ 2 short lines per shot.
- **Confessional setup (reusable prompt block):** subject seated slightly off-center,
  17th-century wainscoted room (Vassall House HQ), window light from left, documentary
  handheld micro-shake, shallow depth of field.
- **Assembly:** ffmpeg concat of shots in script order; fife-and-drum title sting;
  end card.
- **Every episode lives in** `episodes/eNNN-slug/` with `script.md` (human),
  `shots.md` (per-shot Seedance prompts), `production.md` (job IDs, credits, retries).

## The long game (episode runway)

Siege of Boston alone is a season: powder bluff, smallpox, recruiting crisis
(everyone's enlistment expires December 31 — the whole army quits at Christmas),
Knox's cannon road trip, Dorchester Heights. Then New York (the worst year of
George's life), Trenton, Valley Forge, the Conway Cabal (pure office politics),
spies, Yorktown, the presidency ("new job, same energy"). Hundreds of episodes
without inventing a single event.
