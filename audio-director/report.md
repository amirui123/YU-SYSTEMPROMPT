# Audio Prompt Director — Final Report (v1.0, 2026-10-29)

## a. What was built
`Maestro-AD v1.0`, a production-grade English system prompt (AI Studio Edition) that turns lyrics/text + style/mood +
target platform into ready-to-paste prompt packages. Coverage: **20 tools in 5 categories** — vocal generators (Suno v6,
Udio, Mureka, ElevenLabs Music, Lyria), open-source/local (ACE-Step 1.5, YuE2, MusicGen, Stable Audio Open), royalty-free
BGM (SOUNDRAW, AIVA, Beatoven, Mubert, Loudly), TTS (ElevenLabs, OpenAI, Google), SFX (Beatoven maestro, Loudly Sample
Gen). Plus: unknown-platform research-and-adapt, per-platform Persian sections, per-platform license sections, freshness
protocol, 15 safety/quality modules' behavior specified in 12 prompt sections.

## b. Research ledger (Phase 1, all 2026-10-29)
- Web searches: 16 total (5 GitHub-scoped + 11 landscape/leads). GitHub API metadata + 9 repo clones belong to the prior
  mission and were reused only for method, not audio facts.
- Pages opened & read: **30+** (Suno: ToS chunks 0–4, 2 blogs, 6 help articles, 1 category; Udio: ToS chunks 0–4, 5 help
  articles; Mureka API endpoint; ElevenLabs music+TTS; Lyria chunks 0,3,4,5; YuE/ACE-Step/MUSICGEN READMEs; awesome list;
  SOUNDRAW FAQ; AIVA homepage; Beatoven homepage; Mubert docs chunk 0; Loudly FAQ chunk 0; OpenAI + Google TTS guides).
- Video transcripts (real, read in full): **4** (Suno Custom 2026, Suno Custom 2025, Udio Extend 2025, SOUNDRAW official).
- Cross-checked conflicts: 8 logged (Sheet E) — none silently resolved. Persian: zero official FA statements found on any
  song platform → every FA-vocal claim UNVERIFIED with a test-clip fallback chain.

## c. Design decisions (Phases 2–3)
- 8-paradigm router (field+tags / NL plan / single-prompt API / caption / param-formula / file-pair / TTS / SFX) instead of
  20 bespoke builders — new platforms slot into one paradigm (§9).
- Labels on every fact (OFFICIAL/COMMUNITY/UNVERIFIED) + freshness stamp + no-web behavior, so the Director degrades
  honestly instead of hallucinating.
- Bulky knowledge in 5 reference sheets; the main prompt carries stamped summaries; compact stays <1,500 words.
- Safety-first §2 (no lyric reproduction, no living-artist cloning, Terms-gated commercial advice) placed before builders.
- Persian as a first-class engine (§5 + Sheet B3/C3), honest about UNVERIFIED status, with Finglish/hyphen/accent chain.

## d. Deliverables (Phase 4, all in `audio-director/`)
`system-prompt.en.md` (main, AI Studio header) · `system-prompt.fa.md` (natural Persian) · `compact.en.md` (<1,500 words)
· `reference-sheets.md` (Sheets A–E: platform/license/Persian matrix, style vocab + dastgah, lyric/pronunciation/
negative, iteration + TTS/SFX, freshness + contradiction log) · `sources-and-credits.md` (37 numbered sources + gap list)
· `maintenance-guide.md` (monthly checklist + triage prompts) · `tests.md` (15 tests + 5 runs) · `report.md` (this file).

## e. Verification (Phase 5)
15 tests specified (T1–T15: packs per category, cap discipline, license routing, unknown-platform, safety refusal,
freshness). 5 runs hand-executed against the spec: R1 24/25, R2 23/25, R3 25/25, R4 24/25, R5 25/25 — 5 fixes (F1–F5)
folded into v1.0 (duration question, custom-tag labeling, duration caps in license lines, never-invent-numbers rule,
Finglish auto-offer). Live AI Studio runs are the user's step; re-append scores to `tests.md` (append-only).

## f. Known limits & next refresh
- Gaps (Sheet E §E2 + sources §NOT-verified): DiffRhythm, Stable Audio license, ElevenLabs SFX, Mureka/SOUNDRAW/Beatoven/
  Mubert/Loudly Terms+tiers, Lyria music Terms, fa voices, Suno official caps, Udio plans page, unread doc chunks.
- Monthly pass per `maintenance-guide.md`; deprecation watch: OpenAI TTS 2027-01-06; Terms re-check Suno + Udio first.
- No definitive Director rules were written for unopened platforms (per user order) — all such rows say UNVERIFIED + where
  to verify.
