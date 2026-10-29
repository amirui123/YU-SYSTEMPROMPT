# Maestro-FA — Final Report (2026-10-29)

## (a) What was built and why structured this way

**Built:** `Maestro-FA`, a production-grade system prompt turning any chat model (tuned for Google AI
Studio + Gemini) into a Master Songwriter & Poet with elite Persian ability. Deliverables in
`songwriter/`: `system-prompt.en.md` (main, AI Studio edition), `system-prompt.fa.md` (natural Persian
version), `compact.en.md` (<1,500 words), `reference-sheets.md` (4 attachable sheets: genres · Persian
forms+meters · rhyme&flow · banned clichés), `sources-and-credits.md`, `tests.md` (15 tests, 5 executed
runs with honest scores), this report.

**Structure rationale:** 12 sections follow the brief's modules with two deliberate adaptations:
(1) Safety & copyright moved from §10 → **§2** (constraints-before-capabilities: per prompt-engineering
research, early hard rules produce more reliable refusals and cleaner instruction hierarchy);
(2) multilingual rules **folded into §3 intake** (one language decision point — separate language sections
contradict each other in long prompts). Generation flow mirrors use: intake → genre lookup → craft engine
→ Persian module (if FA) → text-to-song (if source text) → output mode → silent QC → styled delivery +
quick commands. Time-sensitive Suno specs live in §8d with a verification stamp so they can be
re-verified without touching the rest. Compact references (tables, not prose) are embedded because a
system prompt cannot add knowledge the model lacks — it can only organize what it retrieves.

## (b) What could NOT be verified

- **Suno + Persian quality** and whether diacritics actually improve Suno's Persian pronunciation —
  method is reasoned, not lab-tested. Test with real generations.
- **"Suno blocks artist names"** — widely reported, not confirmed from an opened official page today;
  the prompt avoids names regardless (safe either way).
- **Dastgah mood associations** — conventional pedagogy, flagged `~`/verify-by-ear in the prompt.
- **BPM cells marked `~`** — typical ranges only; `✓` cells are verified (LowEndCandy, Oct 2026).
- **Any Suno behavior "today"** — specs change fast; the prompt stamps its verification date (2026-10-29)
  and tells the model to remind about re-verification for big projects.
- Search-result snippets were used only to FIND pages; every citation comes from pages actually opened
  (see `sources-and-credits.md`).

## (c) Biggest risks & weaknesses

1. **Aruz accuracy is the #1 risk.** Test run 2 scored meter 2/5: LLMs drift on 14–16-syllable counts
   under generation pressure. Mitigation shipped: numbered scan-and-fix loop + NEEDS REVIEW flags +
   mandatory honesty label — but a human ear (or a syllable-counting script) remains the real QA.
2. **Persian rhyme subtlety.** Same-word "rhymes", weak haraka matches, and register leakage (formal
   words in rap) are the typical failures; the prompt has explicit rules + blacklist, but edge cases
   (regional pronunciations) will slip.
3. **Suno spec rot.** v6-only status, char limits, and slider names WILL change; §8d is the section most
   likely to go stale. Re-verify quarterly.
4. **Copyright boundary on "style of".** The prompt draws the line at genre/mood/structure/imagery, but a
   strong model can still drift toward paraphrase of famous hooks — the §9 "mental search" check is a
   heuristic, not a guarantee.
5. **Over-generation on vague prompts.** Smart defaults can misfire (e.g. one-word «دریا» → wrong genre
   guess). The 1-line assumption + quick commands are the recovery path; teach users the commands.
6. **Translation drift (FA version).** The Persian prompt is a natural translation, not a certified
   equivalent — behavior may differ slightly from the EN version on the same model.

## (d) How to keep improving it

1. **Run the remaining 10 tests** (tests 4–8, 10, 12–15 in `tests.md`) against Gemini in AI Studio with
   Temperature 0.9; log failures per §9 criterion; patch the prompt — one rule per failure.
2. **Build a golden set:** 10–20 ideal input→output pairs (esp. ghazal + Suno packages); regression-test
   every prompt edit against them.
3. **Aruz harness:** write a small syllable-counter for Persian (or human-scan) and score strict-form
   outputs numerically; track meter-score per version.
4. **Suno loop:** generate 5+ real Suno tracks from §8d packages (Persian + English); feed pronunciation
   failures back into §6 diacritics rules.
5. **Version + date-stamp** every edit; re-verify §8d specs quarterly; keep a changelog at the top of
   `system-prompt.en.md`.

## (e) The 5 changes that would make the biggest difference next

1. **A real aruz scorer** (script or human protocol) wired into the test loop — turns the weakest link
   into a measured, improvable metric.
2. **A golden-set regression file** (20 pairs) — prevents every future edit from silently breaking what
   works.
3. **Suno generation trials in Persian** — the only way to validate §8d + §6 pronunciation for the actual
   target platform.
4. **A "style-card" library** (20–30 reference styles described in sound-words, no artist names) as a 5th
   reference sheet — makes "in the style of" requests consistent without copyright risk.
5. **Per-genre few-shots expansion** (rap FA, tasnif, rock EN, lullaby) — 3 examples cover the mechanism;
   6–8 would anchor quality across the genre table.
