# Maestro-AD — Maintenance Guide (v1.0)

How to keep the Director correct as platforms change. Freshness baseline: 2026-10-29.

## 1. What goes stale fastest (check in this order)
1. **Model/version names** (Suno v6→v7?, Mureka 9.5→10?, ElevenLabs v2.5→v3, Lyria 3.5→4) — new generations ship
   every few months; old names in packs confuse users immediately.
2. **Limits** (char caps, clip durations, download quotas) — especially Suno caps (officially unstated; community
   figures drift per version) and Udio sections/clips.
3. **License/Terms** — Udio proved Terms can flip (paid-owned → company-owned). Re-open Suno + Udio Terms every cycle.
4. **Pricing/tiers** — quotas and commercial grants move with pricing pages.
5. **Deprecation clocks** — OpenAI TTS shutdown 2027-01-06 (migrate guidance to `gpt-realtime-2.1-mini`); retired Suno
   models; ACE-Step/YuE/AudioCraft releases + license changes (re-verify MIT/Apache on each bump).

## 2. Monthly checklist (copy into a tracking issue each month)
- [ ] Re-open: Suno Terms + v6 FAQ + pricing · Udio Terms + plans page · Mureka docs + Terms/pricing · ElevenLabs
  music + TTS docs · Lyria docs. Record deltas in Sheet E log.
- [ ] Close Sheet-E gaps: SOUNDRAW/AIVA/Beatoven/Mubert/Loudly pricing + Terms pages (open for the first time);
  Stable Audio license; ElevenLabs SFX; DiffRhythm docs.
- [ ] Check open-source repos for releases: ACE-Step, YuE, AudioCraft (versions + licenses + param changes).
- [ ] Check Google TTS Supported Voices for `fa` + ElevenLabs/OpenAI language lists; update Sheet A/C Persian rows.
- [ ] Run ≥1 Persian test clip (native → Finglish → hyphenated) on a vocal platform; log result (platform/model/date/
  verdict) in Sheet C §C3 and the contradiction log.
- [ ] Re-verify the 8 contradiction-log rows; resolve or restate each.
- [ ] If any pack changed: bump version (v1.1…), update freshness stamp in prompt + sheets + tests, note delta in report.

## 3. How to update the files (keep them in sync)
- Facts live in **one** place: `reference-sheets.md`. The EN/FA prompts carry only stamped summaries; `compact.en.md`
  even less. Change the sheet first, then mirror the stamp lines in the prompts.
- Every changed fact keeps its label; upgraded facts (UNVERIFIED → OFFICIAL) cite the new source URL + access date in
  `sources-and-credits.md` and leave the gap list.
- Tests: after any pack change, re-run the affected tests in `tests.md` and append a dated run row; never edit old
  scored runs (append-only history).

## 4. Versioning
`v1.0` = 2026-10-29 baseline (this release). Minor = monthly refresh (v1.1, v1.2…). Major = paradigm change (new
platform category, router change, safety-rule change). Stamp format everywhere: `Freshness: YYYY-MM-DD`.

## 5. Quick triage prompts (paste to any web-enabled assistant for the monthly pass)
1. "List current Suno models, credit costs, Style/Lyrics char limits, download quotas per tier, with official URLs."
2. "Udio current Terms: who owns output, downloads allowed?, commercial use?, with official URLs."
3. "Mureka / ElevenLabs Music / Lyria: latest models + limits + pricing/terms URLs."
4. "SOUNDRAW, AIVA, Beatoven, Mubert, Loudly: current pricing tiers + terms URLs + commercial grants."
5. "ACE-Step, YuE, MusicGen, Stable Audio: latest release + license."
6. "OpenAI TTS + Google TTS + ElevenLabs TTS: current models, Persian/fa support, terms URLs."
