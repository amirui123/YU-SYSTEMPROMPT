# Maestro-FA — Sources & Credits (all pages below were opened and read 2026-10-29)

## Time-sensitive: Suno / AI-music specs (verified 2026-10-29)

1. **HookGenius — Suno Custom Mode 2026** (opened 2026-10-29; page: updated July 2026, checked on
   Suno 8 Sept 2026). URL: https://hookgenius.app/learn/suno-custom-mode-guide/
   Taken: v6 is the only Suno model since 9 Sept 2026; Style ≤1000 chars (200 on V4 & older); Lyrics
   ≤5000 (3000 older; ~3000 stays the sweet spot); Title ≤100 (80 older); order Genre→Mood→
   Instruments→Vocals→Production; web label "Advanced" vs iOS "Custom"; 8–12 comma tags, key first.
   Resolved the 200/3000 vs 1000/5000 conflict found across guides (it's version-dependent).
2. **sunnoai.com — Suno AI Prompts guide** (opened 2026-10-29; written for v5.5, current since
   26 March 2026). URL: https://sunnoai.com/prompt/
   Taken: five-part style formula (genre→mood→vocal 3 layers→instrumentation→production+BPM); 8–15 tags
   sweet spot, 1st tag weighs most; field-separation table (what goes in Style vs Lyrics vs Exclude vs
   sliders); full meta-tag reference (structure/vocals/instruments/dynamics); pipe-stacked tags;
   section-scoped cues; inline paren cues; end with [End]; ALL CAPS = intensity (1–2 lines max).
3. **Undetectr — Suno Custom Mode & Every V6 Setting** (opened 2026-10-29; rewritten for V6,
   updated 25 Sept 2026). URL: https://undetectr.com/blog/suno-ai-custom-mode-guide
   Taken: Custom/Advanced route (suno.com/create); Lyrics field + tags; Style field; Advanced Options:
   Exclude (documented: "enter any information you do not want"), Vocal Gender (Male/Female + voice
   defined in Style), Creative Sliders — Weirdness (Safe→Chaos, 50% normal), Style Influence
   (Loose→Strong), Audio Influence (audio uploads only); V6: Variety slider (0 = keep style literal),
   Max Mode, model picker (v6 / v6-wild / v6-mini); help centre: user retains ownership of original
   input lyrics.

## Songwriting craft (opened 2026-10-29)

4. **Wikipedia — Song structure.** URL: https://en.wikipedia.org/wiki/Song_structure
   Taken: verse–chorus form; standard pop format (intro–V–PC–C–V–PC–C–B–C + optional outro); verse = new
   lyrics vs chorus = same lyrics; pre-chorus/bridge placement; rock/metal solos after middle chorus.
5. **Wikipedia — Rhyme scheme.** URL: https://en.wikipedia.org/wiki/Rhyme_scheme
   Taken: letter notation; AAAA = fast flow vs ABCABC = slow unfold; AABB couplets = self-contained
   statements; ABAB/ABCB/ABBA + forms list (ballad stanza ABCB, limerick AABBA, etc.); chain rhyme.

## Persian poetry & music (opened 2026-10-29)

6. **Wikipedia — Persian metres** (chunks 0–1). URL: https://en.wikipedia.org/wiki/Persian_metres
   Taken: quantitative verse (short/long/overlong); final syllable always long; never >2 shorts in a
   row; masnavi 11-syllable (or 10) meters + Elwell-Sutton codes: motaqareb 1.1.11 (Shahnameh, Bustan,
   Bani Adam), hazaj 2.1.11 (Vis & Ramin, Khosrow & Shirin), ramal 2.4.11 (Rumi's Masnavi, Conference of
   the Birds), hazaj-10 5.1.10 (Leyli & Majnun), xafif 4.5.11 (Sanai, Haft Peykar); lyric tetrameter
   14–16 syllables, 70% in 7 meters incl. 2.4.15, 2.1.16, 3.1.15, 4.1.15, 4.7.14, 3.3.14 (+4.5.11 in 8
   Hafez ghazals); rubai: two 13-syllable patterns (3.3.13 / 5.1.13, rubai-only), rhyme AA·BA; lyric
   rhyme = rhyming matla + same rhyme at each couplet's end; Nezami's Khamsa (~29,000 couplets).
7. **Wikipedia — Aruz.** URL: https://en.wikipedia.org/wiki/Aruz
   Taken: stub only — redirected to Persian metres (above); 'aruz = Persian/Turkic/Urdu prosody, 16
   original + 3 Persian-added meters (from this stub).
8. **Wikipedia — Dastgah** (chunks 0–1). URL: https://en.wikipedia.org/wiki/Dastgah
   Taken: 7 principal + āvāz in Mirza Abdollah's radif order (Shur + Bayat-e Tork/Dashti/Abu-Ata/Afshari;
   Segah; Nava; Homayun + Bayat-e Esfahan; Chahargah; Mahur; Rast-Panjgah; less common Bayat-e Kord,
   Shushtar); Mâhur≈Ionian/major, Shur≈Phrygian; radif = 365 gushehs; codified by Mirza Abdollah
   (1843–1918); UNESCO Intangible Heritage 2009. Dastgah MOODS in the prompt are conventional
   associations, not from this article — flagged accordingly.

## Tempo (opened 2026-10-29)

9. **LowEndCandy — BPM by Genre** (article dated 2026-10-10). URL: https://lowendcandy.com/blog/bpm-by-genre-chart/
   Taken (all marked ✓ in the prompt): hip-hop 80–110 (boom bap 85–95), lo-fi 70–90, trap 130–150
   (felt 70), R&B 60–100, pop 100–130, reggaeton 90–100, disco/funk 100–130, deep house 118–125, house
   120–130 (124/126), tech house 124–128, techno 125–150 (130–140 common), trance 128–140 (138),
   UK garage 130–135, dubstep 138–142 (felt 70), DnB 160–180 (170–175 sweet), jungle 160–170, hardstyle
   150–160; "typical ranges, not rules." All other BPM cells in the prompt are marked `~` (typical).

## Reused prior research (this repo, not re-opened today)

- Prompt-system design patterns (role definition, constraints-first, output formats, few-shot examples,
  self-checks, injection defense): `research/web/findings.md`, `analysis/comparison.md`,
  `prompt/sources-and-credits.md` (researched 2026-10-29 with full URL lists inside those files).
- Persian diacritics method condensed into §6 from `prompt/persian-lyric-vocalizer.en.md` (Vocalizer-FA
  v1.1, this repo).

## NOT verified (marked as such wherever used)

- Suno singing **Persian** lyrics well; diacritics-improve-pronunciation trick (our method, user-test it).
- "Suno blocks real artist names" (widely reported; not confirmed from an opened official page today —
  prompt treats it as a must-avoid regardless, which is safe either way).
- Dastgah mood associations (conventional pedagogy; verify by ear).
- BPM cells marked `~`; exact Suno behavior on any given day (verify in-app; specs change fast).
- Web-search result snippets (Suno guides roundup, BPM roundup) were used only to FIND pages; nothing is
  cited from snippets — only from pages actually opened above.
