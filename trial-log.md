# Trial log — u-puan-one-letter-for-your-day-e54e9c36

## Competition
- Slug: `u-puan-one-letter-for-your-day-e54e9c36`
- Title: One Letter for Your Day
- Sponsor: u-puan-one-letter-for-your-day (user-created bounty)
- Prize: $5 total — 1st $2, 2nd $2, 3rd $1. Free to enter.
- Opens: 2026-11-23T21:28:55Z (24 Nov 05:28 WITA). Deadline: 2026-11-24T21:25:00Z (25 Nov 05:25 WITA).
- Kit limits (competition.yaml + RULES.txt, read in full): harness program/v1, runtimes node22 / python3.13, sandbox NO network; program writes one text to `/output/entry.txt`; gate = UTF-8, exactly 1 character, not only whitespace; transcripts_required: true; license: osi; repo_created_after_open: true; max 5 submissions/entrant/day; rule Force_Last (last submit before deadline = final entry, unless an earlier one is picked with `makefun final`).
- Judge: z-ai/glm-5.3-flash, pairwise, no ties, margins 1–5, each pair judged in both orders; 3 blind rounds (next round 2026-11-24T05:27:36Z); final heat: top 500 on the dev board, 3 Swiss rounds + playoff among top 5; 3 fixed house texts play in every heat (an entry byte-identical to one shares its rate and never enters the playoff).
- Judge criteria, in order: (1) the letter is the first letter of a word that describes the day; a letter standing for no day's word loses to any that does. (2) The word is vivid and specific, a sharp picture of the day rather than a vague mood. (3) Funny or surprising, lands at once, the kind a reader repeats to a friend. (4) True to a real day, honest report not performance. (5) The letter suits its word, an initial that fits the sound and shape of the word and is not the obvious pick where a sharper one exists. Obscurity for its own sake does not count.
- Kit: `~/workspace/make-fun/u-puan-one-letter-for-your-day-e54e9c36-kit/` (tarball sha256 c32f0cf0d1c3249966768c37faf4358b27f5cea49fe6e0c88d8e72aab2eeb575; kit.json bundle_sha256 a7aca0ef3aaffb3c1b2e0443345cf2f91125ff1301437e4539f0d0d640ec44b2 — MATCHES the API value from https://make.fun/api/competitions/u-puan-one-letter-for-your-day-e54e9c36/kit).
- Wallet (owner.json): FwUebjzYUBF6uybmEkUkiQf9z35bGGQuUE3GrToXFcUq
- This session started after the opening (24 Nov 06:50 WITA), so its transcript falls inside the competition window.

## Candidate letters (the judge sees only the letter, so it must conjure the word; the pick is the letter whose most natural word is vivid, funny, and true)

| Letter | Word behind it | Verdict |
|---|---|---|
| Z | zombie / zero sleep | Strongest first association, but the rules themselves give "Z for zero sleep" as the example, so it is the most predictable crowd pick (mass tie risk: byte-identical entries share one rate, earlier receipt places above copies) and the likeliest strong house fixed text (a match never enters the playoff, so no prize). Rejected on risk, not on word strength. |
| H | hungover | The single most vivid day word, but the next most predictable pick after Z, with the same tie and fixed-text exposure. Rejected on risk. |
| A | amazing | The rules' example. A vague mood, fails criterion 2 outright. Rejected. |
| F | Friday-feeling / fried | Rules' example again; "Friday-feeling" is cute but thin, "fried" is good yet F will be crowded. Rejected. |
| E | exhausted | True and vivid, but the obvious pick for E and a common crowd letter. Rejected. |
| K | knackered | Vivid, funny, true, but the K in "knackered" is silent, which strains criterion 5 (the initial should fit the sound of the word), and the word is regional British slang. Rejected. |
| G | groggy | Vivid and true, but the judge's first association for G may be "great" or "good", both vague moods that fail criterion 2. Rejected. |
| D | derailed | Sharp picture, funny, true, but the first association may be "dreadful" or "dead", both vague. Rejected. |
| J | jittery | Vivid (too much coffee, shaky hands), but first association may be "joyful", a vague mood. Rejected. |
| T | trainwreck | Vivid picture, but first association is likely "tired" or "terrible", both vague. Rejected. |
| C | cooked / chaotic | "Cooked" is current slang and funny, but first association may be "crazy" or "chaotic", both vague. Rejected. |
| U | unhinged | PICK. See below. |

## Pick: U — "unhinged"
- (1) U is the first letter of "unhinged", a word that describes a day, so the letter stands for a real day's word.
- (2) Vivid and specific: a day that came off its hinges, plans falling apart one after another, strange things happening. A sharp picture of how the day went, not a vague mood.
- (3) Funny and surprising, lands at once: "today was unhinged" is the kind of line a reader repeats to a friend, compressing a whole chaotic day into one word.
- (4) True: an honest report of a day that genuinely went off the rails, ordinary or strange, not a performance.
- (5) The letter suits the word: U is the initial and carries its opening sound, and it is not the obvious pick where a sharper one exists. Z and H carry strong words too, but they are the rules' own examples and the predictable crowd picks; U carries a word just as strong with far less company, so it also dodges the mass-tie pile and the likeliest house fixed texts. "Unhinged" is current everyday slang, not obscurity for its own sake.

## Trials

| Round | Version | Size | Result | Change |
|---|---|---|---|---|
| 0 | (pre-build) trial log + facts recorded | — | — | — |
| 1 | Builder v1 — main.ts, entry: "U" | 1 character / 1 byte, UTF-8, non-whitespace | PASS — local run via ENTRY_OUTPUT twice, byte-identical (sha256s below); stdlib only, no network | Builder session (this session) |

## Preflight (token-free) — PASSED
- Run 1: `ENTRY_OUTPUT=/tmp/one-letter-r1/entry.txt node main.ts` → exit 0.
- Run 2: `ENTRY_OUTPUT=/tmp/one-letter-r2/entry.txt node main.ts` → exit 0.
- Determinism: `cmp` run1 vs run2 → byte-identical.
- Output: `U` — 1 character, 1 byte, gate valid (exactly 1 character, non-whitespace), no trailing newline, UTF-8.
- Run sha256s: run 1 `a25513c7e0f6eaa80a3337ee18081b9e2ed09e00af8531c8f7bb2542764027e7`, run 2 `a25513c7e0f6eaa80a3337ee18081b9e2ed09e00af8531c8f7bb2542764027e7` — identical.

## Build
- main.ts written fresh with the file-write tool in this session (never copied/moved into place). Node 22, stdlib only, no network, deterministic. Writes LETTER to `$ENTRY_OUTPUT` or `/output/entry.txt`, no trailing newline.
- Repo: `~/workspace/make-fun/u-puan-one-letter-for-your-day-e54e9c36/` — main.ts, README.md (3 make.fun badges), LICENSE (MIT), .makefun/owner.json (wallet FwUebjzYUBF6uybmEkUkiQf9z35bGGQuUE3GrToXFcUq), trial-log.md. Commit identity rwnliwan <rwnliwan@users.noreply.github.com>.
- NOT submitted by builder. Coordinator runs check/submit. Blind round 1 at 2026-11-24T05:27:36Z (13:27 WITA) — submit before then to move up.

## Commit record
- Builder commit: `c76fa9e3f0dbe0c396cf012e7bfad0f6684b9e40` — "One Letter for Your Day entry: U for unhinged" (files: main.ts, README.md, LICENSE, .makefun/owner.json, trial-log.md).
- GitHub repo: https://github.com/rwnliwan/u-puan-one-letter-for-your-day-e54e9c36 (public, created after the 2026-11-23T21:28:55Z opening; push + About/topics recorded below).
