# Audio Prompt Director — Reference Sheets (v1.0)

Companion to `system-prompt.en.md` (`Maestro-AD v1.0`). Freshness baseline: **2026-10-29**.
Labels: **OFFICIAL** (opened official page) · **OFFICIAL-SNIPPET** (official page seen only as search
snippet, section not opened) · **COMMUNITY-TESTED** (credible community tests/guides) · **UNVERIFIED**
(not confirmed — do not present as fact). Full source list: `sources-and-credits.md`.

---

## Sheet A — Platform format / limits / Persian / license matrix

### A1. Vocal song generators

| # | Platform / models | Input paradigm | Fields & limits | Tags / syntax | Duration & extend | Persian support | License (free vs paid + Terms link) |
|---|---|---|---|---|---|---|---|
| 1 | **Suno** — v6, v6-wild (paid), v6-mini (all/free). Old models retired; old outputs playable/remasterable/coverable (OFFICIAL v6 FAQ) | Simple mode: one NL description. Custom mode: Lyrics + Style + Advanced Options (OFFICIAL help + 2 video transcripts) | Style/Lyrics char limits: OFFICIAL silent; COMMUNITY-TESTED version-dependent (v5-era ≈ Style 200 / Lyrics 3000 / Title 80; v6-era reports ≈ Style 1000 / Lyrics 5000) — always verify in-app. 10 credits = 2 songs (OFFICIAL) | Section + vocal/instrument tags in Lyrics, e.g. `[Verse] [Chorus] [Guitar Solo]`; Exclude field; Vocal Gender M/F; Variety slider (0 = full control); Weirdness + Style Influence sliders (OFFICIAL help + transcripts) | Native length not stated officially (≈4 min COMMUNITY); Extend (keep-point + new lyrics/style + Get Whole Song); Max Mode for >2 min songs, covers, vocal consistency, costs more (OFFICIAL) | No official FA statement found → **UNVERIFIED**. Workarounds untested: Finglish/phonetic respelling, syllable breaks | **Terms (OFFICIAL, opened): https://suno.com/terms (rev 2026-08-10, eff 2026-09-03).** FREE: personal/non-commercial only, 7 lifetime trial downloads. PAID (Pro 20/mo, Premier 60/mo, Studio unlimited downloads): ownership of Output assigned to user + commercial use ONLY via permitted Download; watermark/fingerprint must stay; stream-ripping banned; rights survive cancel. REMIX: always non-commercial, any tier. Input lyrics stay yours. Voice Model: own voice only |
| 2 | **Udio** — standard + MiniMax speech-02 fallback for voiceovers (OFFICIAL) | Prompt box (topic + genre tags) or Custom Lyrics Editor; Manual Mode = exact tags only, no free text (OFFICIAL) | Prompt char limit not stated officially → UNVERIFIED | 28 official guidance tags, `/` autocomplete: `[Verse] [Chorus] [Intro] [Outro] [Bridge] [Hook] [Pre-chorus] [Refrain] [Post-chorus] [Drop] [Interlude] [Instrumental Break] [Instrumental] [Build] [Pre-hook] [Pre-drop] [Pre-refrain] [Break] [All] [Breakdown] [Instrumental Bridge] [Sample] [Solo] [Ensemble] [Post-hook] [Spoken Word] [Choir] [Announcer]` + vocal tags `[Scream]`, instrument tags `[Guitar Solo]`; `(…)` = backing vocals. Guidance, not hard commands (OFFICIAL) | Clips: 32 s (default) or 2:10 (OFFICIAL). Extend: intro/before/after/outro, crop, ≤10 sections total; blank lyrics = instrumental break (OFFICIAL + Extend transcript) | No official FA statement → **UNVERIFIED**. Official pronunciation tools are Latin-centric (syllable breaks `Un-be-liev-a-ble`, spelled acronyms, accented chars for stress) — FA effect untested | **Terms (OFFICIAL, opened): https://www.udio.com/terms-of-service (rev 2025-11-12).** Company owns ALL Output (user assigns rights); **NO downloads, NO commercial use, personal in-app use only — free AND paid alike**; inputs used for training; free users must credit Udio on public use. ⚠️ Changed from pre-UMG-settlement terms (paid used to own output). Verify current plans page before any commercial assumption |
| 3 | **Mureka** — `auto` (latest), 7.6, o2, 8, 9, 9.5; o2: no vocal_id/melody_id (OFFICIAL API docs) | API: `lyrics` (required) + `prompt` (style) + optional `reference_id / vocal_id / melody_id` + `gender` + `stream` (OFFICIAL) | lyrics ≤ **5000** chars; prompt ≤ **1024** chars; n ≤ 3 songs/req (billed per song); async task, poll `song/query/{task_id}` (OFFICIAL). cURL sample: prompt `"r&b, slow, passionate, male vocal"` | Section tags in lyrics (`[Verse]` per official sample) (OFFICIAL) | Not stated in opened endpoint doc → UNVERIFIED | No statement → **UNVERIFIED** | Docs opened: `platform.mureka.ai/docs/.../post-v1-song-generate.html` (OFFICIAL). Pricing/ownership/commercial terms NOT opened → **no definitive license rules**; verify official Terms + pricing before commercial use |
| 4 | **ElevenLabs Music** — v1 / v2 / v2.5 (OFFICIAL docs) | Natural-language composition plan + optional ~30 s audio reference (OFFICIAL best-practices) | `music_length_ms` param; v2.5 API ≤ ~4100 chars (COMMUNITY: music_v2_5 API reports) | 5-question rule (genre/mood/tempo/voices/instruments); studio vocab; narrate the arrangement; timing cues; loop-exclusion phrasing; solo/a-cappella isolation for single voice; sound-design method (OFFICIAL) | Clip preview ≈30 s; full songs ≈ couple of minutes (OFFICIAL docs) | Multilingual claimed; FA unconfirmed → **UNVERIFIED** | Best-practices describe output as commercial-cleared (OFFICIAL docs); tier/Terms details NOT opened → verify official Terms + pricing before commercial use |
| 5 | **Google Lyria 3.5** (Gemini API) (OFFICIAL docs) | Single text prompt (+ optional ≤10 images for image→music); API call (OFFICIAL) | Prompt text; custom-lyrics mode; timestamps (OFFICIAL) | `[Verse] [Chorus] [Bridge]`; timestamp structure `[0:00-0:10]`; instrumental-only mode; **lyrics language = prompt language** (OFFICIAL) | 30 s clip preview; full songs ≈ couple of minutes (OFFICIAL) | lyric-lang=prompt-lang mechanism is official; FA output quality untested → **UNVERIFIED** | Music-specific license NOT opened → verify Gemini API / AI Studio Terms before commercial use |

### A2. Open-source / local models

| # | Model | License (OFFICIAL) | Input paradigm | Key params / limits | Persian |
|---|---|---|---|---|---|
| 6 | **ACE-Step 1.5** (ACE-Step team) | **MIT** (OFFICIAL README) | caption + lyrics + params; <2 s on A100; 10 s–10 min; 50+ langs; 1000+ styles; XL 4B DiT (OFFICIAL) | Community params: 10–300 s, `[tags]`, `(whisper)/(falsetto)` vocal styles, BPM/key/seed — COMMUNITY-TESTED, verify in repo | "50+ langs" official; FA unconfirmed → **UNVERIFIED** |
| 7 | **YuE / YuE2** (multimodal-art-projection) | **Apache-2.0** (OFFICIAL README) | genre-file + lyrics-file; symbolic+audio; arXiv 2609.33757; WildSongBench vs Suno v5/v6 (OFFICIAL) | See repo README (6 chunks; full param list not extracted) → details UNVERIFIED | Not stated → **UNVERIFIED** |
| 8 | **MusicGen** (Meta AudioCraft) | **MIT** (OFFICIAL) | text caption (+ optional melody); 10 models; EnCodec 32 kHz (OFFICIAL) | ≤30 s typical; cfg 3–6 (COMMUNITY); training configs small 300M / med 1.5B / large 3.3B (OFFICIAL) | Not stated → **UNVERIFIED** |
| 9 | **Stable Audio Open** (Stability AI) | NOT opened → verify on official page; no claim here | tag-style caption + BPM; ≤47 s (OFFICIAL demo) | As left | Not stated → **UNVERIFIED** |
| — | DiffRhythm | NOT opened → excluded from definitive rules; research gap (see Sheet E) | — | — | — |

### A3. Royalty-free BGM generators

| # | Platform | Input paradigm (OFFICIAL unless noted) | Key controls | License (free vs paid + Terms link) |
|---|---|---|---|---|
| 10 | **SOUNDRAW** | Tag-based, NO free-text generation prompt: Generate Music tab → Length + Tempo (BPM) → Mood/Genre/Theme tags → song list → instrument include/exclude → edit arrangement/structure. Chatbot "Neo" only navigates. (OFFICIAL FAQ + official video transcript) | Pro Mode: length, BPM, instruments, key, stem volumes, fade out; per-section intensity + builds; Create Similar; download track + stems (OFFICIAL transcript) | Royalty-free, "fully licensed … under the terms of your membership agreement" (OFFICIAL transcript). Free-vs-paid tiers NOT opened → UNVERIFIED; check official pricing + Terms (footer of soundraw.io) |
| 11 | **AIVA** (AIVA Technologies SARL) | Style picker (250+ styles) or custom style model; audio/MIDI influence upload; piano-roll editor; section insert/delete, BPM, dynamics, MIDI import/export (OFFICIAL homepage + COMMUNITY review of Helpdesk) | Track durations: Free ≤3:00, Standard ≤5:00, Pro ≤5:30 (OFFICIAL pricing) | **(OFFICIAL pricing, opened: https://www.aiva.ai/.)** FREE €0: copyright owned by AIVA, NO monetization, must credit AIVA, 3 downloads/mo, MP3+MIDI. STANDARD €11/mo: AIVA owns, LIMITED monetization (YouTube/Twitch/TikTok/Instagram only), 15/mo. PRO €33/mo: copyright owned by YOU, full monetization, 300/mo, all formats + WAV. SACEM-recognized (COMMUNITY). Terms page not opened → confirm on official Terms |
| 12 | **Beatoven.ai** (maestro model) | NL description → "maestro crafts soundtrack" (text-to-music) + choices UI (title/duration/tempo/genre/emotion per COMMUNITY tutorial); API exists (OFFICIAL homepage) | Download MP3/WAV; pay-per-track or subscribe for minutes (OFFICIAL homepage) | Page title "Royalty Free AI Music Generator" (OFFICIAL-SNIPPET-level: homepage title). Tier/Terms details NOT opened → UNVERIFIED; check official Terms + pricing |
| 13 | **Mubert API v3** | REST + MCP server (21 tools) + skill; NOT lyric-based: `playlist_index, duration, format, mode (loop), intensity`, library filters incl. BPM/genre (OFFICIAL API docs) | Instant pre-rendered durations: 5,6,8,10,15,20,30,40,60,180,240,300 s; else rendered from scratch; track URLs expire; 1 stream/client; Text-2-Music + Image-2-Music modes, 150+ genres/40+ moods per official blog (OFFICIAL) | Commercial API licensing, quota/seat-based; self-serve credentials by email (OFFICIAL docs). Free tier / ownership NOT opened → UNVERIFIED; confirm contract + Terms |
| 14 | **Loudly** | Music Generator = song-builder formula (genre, duration, energy, instruments, structure, tempo, key → 3 tracks, <5 s) + Text-to-Music + Remixer + Sample Generator (text→loops/samples/SFX, e.g. "Synth pad in A minor 80 BPM") + Stem Splitter + Studio + Distribution (OFFICIAL FAQ) | Tempo 60–200 BPM; structure presets (classic, slow burn); genre blending; WAV/MP3 + stems (OFFICIAL FAQ) | 100% royalty-free, safe commercial + non-commercial, no extra licensing; keep 100% streaming royalties; distribution to 50+ platforms incl. Spotify/Apple/TikTok (OFFICIAL FAQ). Limits per OFFICIAL-SNIPPET (section not opened — verify): no resell/sublicense/stock-library; Pro ads ≤$100k spend; films/TV need special license (help@loudly.com). Terms page not opened → confirm |

### A4. TTS / voice / singing

| # | Provider | Input paradigm (OFFICIAL) | Key facts | Persian | License note |
|---|---|---|---|---|---|
| 15 | **ElevenLabs TTS** (Eleven v4; 90+ langs; 7M+ users) | text + voice pick + model; sliders (stability/similarity: COMMUNITY-TESTED, not in opened page) | Product page only opened; API prompting details NOT opened → UNVERIFIED | "90+ languages" official; FA voice unconfirmed → **UNVERIFIED** | Terms NOT opened → verify official Terms |
| 16 | **OpenAI TTS** (`gpt-4o-mini-tts`, 11 voices) | API: `model + input + voice + instructions` ("Speak in a cheerful and positive tone") (OFFICIAL guide) | ⚠️ tts-1/tts-1-hd/gpt-4o-mini-tts deprecated, shutdown **2027-01-06** → migrate to `gpt-realtime-2.1-mini` via Realtime API (OFFICIAL). Must disclose AI voice to end users (OFFICIAL) | Multilingual claimed; FA untested → **UNVERIFIED** | Usage policies (OFFICIAL, in-page link): https://openai.com/policies/usage-policies |
| 17 | **Google Cloud TTS** | text or **SSML** → MP3/LINEAR16; voice = languageCode + name + gender/accent; AudioConfig: rate/pitch/volume/sample-rate (OFFICIAL basics) | SSML fully supported incl. `<phoneme>`/breaks (OFFICIAL) | fa voice NOT verified in opened page → **UNVERIFIED** (check Supported Voices page) | GCP Terms (OFFICIAL, in-page link): https://cloud.google.com/terms/ |

### A5. SFX generators

| # | Tool | Input paradigm | Notes |
|---|---|---|---|
| 18 | **Beatoven maestro SFX** | text prompt → "high-fidelity sound effect" (OFFICIAL homepage) | Param details NOT opened → UNVERIFIED |
| 19 | **Loudly Sample Generator** | text → loops/samples/one-shots/SFX, e.g. "Synth pad in A minor 80 BPM" (OFFICIAL FAQ) | Musical-SFX style; include key + BPM in prompt |
| 20 | **ElevenLabs SFX / others** | NOT opened → no definitive rules; gap (Sheet E) | Use generic SFX recipe (Sheet D) labeled UNVERIFIED |

---

## Sheet B — Style vocabulary (cross-platform descriptors)

### B1. Genre / mood / tempo cores (use 3–6 tags max for tag-fields; narrate for NL fields)
- **Genres:** pop, rock, indie-rock, alt-rock, punk, metal, hip-hop, trap, drill, boombap, r&b, neo-soul, funk, disco, house, deep-house, techno, trance, dubstep, drum-and-bass, ambient, lofi, chillwave, synthwave, jazz, bossa-nova, blues, country, folk, americana, latin, reggaeton, afrobeats, dancehall, k-pop, j-pop, arab-pop, persian-pop, classical, cinematic, orchestral, epic-trailer, gospel, edm, phonk, hyperpop.
- **Moods:** euphoric, uplifting, melancholic, nostalgic, dark, haunting, dreamy, ethereal, aggressive, defiant, rebellious, romantic, sensual, hopeful, triumphant, mysterious, eerie, playful, quirky, chill, laid-back, energetic, anthemic, intimate, epic, bittersweet.
- **Tempo anchors (BPM, COMMUNITY chart 2026-10-10, cross-checked):** lofi 70–90 · hip-hop 85–115 · pop 100–130 · house 118–130 · techno 120–150 · trap 130–150 (half-time feel) · drum-and-bass 160–180 · dubstep 140 (half-time) · rock 110–140 · metal 140–200+ · jazz swing 120–180 · bossa 120–140 · reggaeton/dembow ≈95–100 · afrobeats 100–120 · cinematic 80–120 · trailer 140+ w/ half-time hits. (Full table: `songwriter/reference-sheets.md` Sheet 1.)
- **Era/production:** 80s retro, 90s alternative, y2k, vintage vinyl, lo-fi tape, polished radio-ready, raw garage, arena-sized, stadium, acoustic unplugged, orchestral hybrid, analog synth, digital crisp.

### B2. Voices (never a living artist's name; descriptors only)
- **Register/gender:** male vocal, female vocal, duet, choir, gospel choir, children's choir, spoken word, whisper, falsetto, baritone, soprano, alto, tenor, raspy, gritty, smooth, breathy, smoky, husky, angelic, operatic, soulful, nasal folk timbre.
- **Delivery:** belted chorus, soft verse → explosive chorus, call-and-response, ad-libs, layered harmonies, octave doubles, spoken intro, sung-through, rap-sung hybrid, melodic rap, chant, shout chorus.
- **Udio vocal tags:** `[Scream] [Spoken Word] [Choir] [Announcer]` (+ `[Announcer: Shouting]` style per community guide). **ACE-Step:** `(whisper) (falsetto)` (COMMUNITY).

### B3. Persian / dastgah module (descriptors for style fields; all FA-vocal claims UNVERIFIED)
- **Dastgah (melodic systems):** Shur, Mahur, Homayun (Bayat-e Esfahan related feel), Segah, Chahargah, Rast-Panjgah, Nava; **Avaz:** Abu-Ata, Bayat-e Tork, Afshari, Dashti, Esfahani.
- **Prompt phrasing (EN style fields):** `persian pop, Shur dastgah-inspired melody, tahrir vocal ornamentation` · `iranian folk, Bandari 6/8 rhythm, ney + daf` · `cinematic middle-eastern, Chahargah mode, kamancheh lead, epic percussion`.
- **Instruments (EN spellings):** tar, setar, kamancheh (spike fiddle), santur (hammered dulcimer), daf (frame drum), tombak (goblet drum), ney (end-blown flute), barbat/oud, qanun, ghaychak, sorna, karna, dotar, tanbur, robab, bendir, zarb.
- **Rhythms:** Bandari 6/8, Persian pop 4/4, 2/4 folk, free-meter avaz intro → rhythmic verse (describe arc in NL fields).
- **Vocal:** `tahrir melisma`, `nasal folk timbre`, `male persian vocal`, `female persian vocal`, `duet`, `call-and-response`. ⚠️ Whether any vocal generator renders FA lyrics correctly is **UNVERIFIED for every platform** — always offer the Finglish/phonetic fallback + test-clip loop (Sheet C §C4).

### B4. Production / arrangement narrations (ElevenLabs-style NL + Lyria + text-to-music)
Template: `[era+genre] at [BPM] in [key]; [texture]; arrangement: [intro 4 bars sparse] → [verse adds X] →
[pre-chorus lift] → [chorus full, doubled vocals] → [breakdown strips to Y] → [final chorus + ad-libs] → [outro]. Mix: [wide/punchy/intimate]; no [excluded elements].`
- Textures: warm analog pads, plucky oud-like riff, driving four-on-floor, syncopated latin percussion, swelling strings, gritty distorted 808s, sparkling arps, vinyl crackle bed.
- Dynamics words: sparse, stripped, builds, lifts, explodes, drops, breaks down, swells, fades, stingers, risers, impacts.

---

## Sheet C — Lyric formatting · pronunciation · negative prompts

### C1. Section-tag syntax per platform
- **Suno (COMMUNITY-TESTED, matches official Exclude/v6 behavior):** `[Intro] [Verse] [Pre-Chorus] [Chorus] [Hook]
  [Post-Chorus] [Bridge] [Breakdown] [Drop] [Interlude] [Instrumental Break] [Guitar Solo] [Outro] [End]` + inline
  performance notes `[Soft Vocals] [Belted] [Whispered] [Spoken]`; `( backing line )` = backing vocals. Keep tags on
  their own lines; do not over-tag (≤1 tag per 2–4 lines).
- **Udio (OFFICIAL 28 tags):** as Sheet A + vocal/instrument tags `[Scream] [Guitar Solo]`; `(…)` backing vocals.
  KillerM guide (official help center): human-written lyrics beat AI clichés; mind syllable counts; you can inpaint
  lyrics keeping syllable count; second verse/chorus variations add life; `[Final Chorus]`-style custom tags work.
- **Mureka (OFFICIAL sample):** `[Verse]`-style tags inside `lyrics` (≤5000 chars).
- **Lyria (OFFICIAL):** `[Verse]/[Chorus]/[Bridge]` + `[0:00-0:10]` timestamps in custom-lyrics mode.
- **ACE-Step (COMMUNITY):** `[tags]`, `(whisper)/(falsetto)`. **MusicGen/Stable Audio:** no lyrics — caption only.

### C2. Lyric-prep rules (portable)
1. One idea per section; chorus = simplest + most repetitive; verse = story/detail; bridge = contrast (new rhyme, new
   rhythm, stream-of-consciousness allowed — KillerM).
2. Count syllables per line; keep verse lines even (±2); chorus lines shorter.
3. Mark non-sung sounds: `Whoa oh oh`, `[Vocalise]`, `[Instrumental Break]` — never leave the model guessing.
4. Extend-planning: write per-section lyrics sized to the platform's clip length (Udio 32 s/2:10; Suno ≈ verse+chorus
   per generation — COMMUNITY).
5. Never reproduce copyrighted lyrics; user-supplied originals stay theirs (Suno OFFICIAL).

### C3. Pronunciation engineering
- **Udio (OFFICIAL):** syllable-breaks `Un-be-liev-a-ble`; spell acronyms (`F B I`); accented chars for stress
  (`café`-style stress marking — Latin examples; FA effect UNVERIFIED).
- **Suno (COMMUNITY-TESTED):** phonetic respelling (write words as they sound); repeat-word emphasis; simpler
  consonant clusters for non-English; split diphthongs across notes with hyphens.
- **Persian fallback chain (UNVERIFIED, test-clip required):** (1) native script; (2) Finglish phonetic respelling
  (`delam barat tang شده` → `delam baraat tang shode`); (3) hyphenated syllables (`de-lam ba-raat`); (4) accented
  stress vowels (`delám baráat`); (5) shorten lines + slow tempo + sparse arrangement so mumble is less likely.
- **Google TTS (OFFICIAL SSML):** `<phoneme alphabet="ipa" ph="…">`, `<break time="500ms"/>`, `<prosody
  rate="slow" pitch="+2st">`, `<say-as>`; best tool for exact FA pronunciation IF a fa voice exists (voice list
  UNVERIFIED — check Supported Voices page).
- **OpenAI TTS (OFFICIAL):** no SSML; steer with `instructions` ("Speak slowly, Persian accent, pause between
  sentences"); try respelled input. **ElevenLabs TTS:** text + voice + sliders (COMMUNITY); audio-tag support
  UNVERIFIED.

### C4. Negative prompts / exclusions per platform
| Platform | Mechanism | Example |
|---|---|---|
| Suno | Exclude field, Custom → Advanced (OFFICIAL) | `rap, screaming, choir, saxophone, 80s drums` |
| Udio | Style Reduction slider/tags + Manual Mode (exact tags only) (OFFICIAL) | reduce `metal`; Manual: `[Verse] pop, acoustic` only |
| ElevenLabs Music | NL loop-exclusion phrasing (OFFICIAL) | `…and stop before any guitar solo; no drums in the intro; do not add choir` |
| Lyria | NL "instrumental-only" + negative phrasing (OFFICIAL) | `instrumental only, no vocals, no speech` |
| Mureka | none verified → UNVERIFIED; try negative adjectives in prompt, labeled as guess | `uplifting pop, no rap section` (UNVERIFIED) |
| SOUNDRAW | instrument include/exclude toggles (OFFICIAL) | exclude: brass, synth |
| AIVA/Beatoven/Mubert/Loudly | choice-based or unverified → use positive descriptors; negatives UNVERIFIED | — |
| Open-source | negative prompt / negative concept support varies → UNVERIFIED per repo | check repo flags |

---

## Sheet D — Iteration playbook · TTS & SFX recipes

### D1. Diagnose → fix (vocal generators)
| Symptom | Likely cause | Fix (platform) |
|---|---|---|
| Wrong genre/mood | vague style, too many tags | Suno: Variety→0, Style Influence 75–85 (COMMUNITY), fewer tags; Udio: Manual Mode + exact tags; ElevenLabs: re-narrate with studio vocab |
| Garbled / wrong-language vocals | lyric density, script issues | shorten lines, phonetic respell (C3), slower tempo, sparse arrangement; test 1 clip before full song |
| Vocals where instrumental wanted | missing markers | `[Instrumental Break]` / Instrumental Mode (Udio OFFICIAL); lyrics blank (Suno transcript); `instrumental only` (Lyria OFFICIAL) |
| Song too short / abrupt end | clip limits | Suno Extend + Get Whole Song; Udio extend ≤10 sections; ACE-Step duration param; Lyria timestamps |
| Style drift across sections | context loss | Udio: extend prompt restates genre + tags; Suno: same Style field + Max Mode for consistency (OFFICIAL) |
| Unwanted element (choir/rap/solo) | no exclusion | Sheet C §C4 per platform |
| Lyrics changed by model | AI-lyrics mode on | paste Custom Lyrics; Udio Manual Mode; keep syllable counts for inpaint (KillerM) |
| Singer gender wrong | unspecified | Suno Vocal Gender + `male/female vocal` in Style (OFFICIAL); Mureka `gender` param (OFFICIAL) |

### D2. Extend / remix / cover workflows
- **Suno (OFFICIAL):** Extend from keep-point → new lyrics/style → Create → Get Whole Song. Remix/Edit menu: remaster,
  cover, replace-section, crop (article index OFFICIAL; per-article details partially unread). ⚠️ Remixes = non-commercial always.
- **Udio (OFFICIAL + transcript):** select song → Extend → intro/before/after/outro/crop → auto/custom/instrumental →
  Generate → repeat to ≤10 sections. Trimming + audio-upload remix exist (article index). ⚠️ ToS: no downloads at all.
- **Mureka (OFFICIAL API):** `reference_id` (style), `vocal_id` (voice), `melody_id` (melody, no combos), `stream` for
  playback-while-generating.

### D3. TTS recipes
- **Narration/podcast (any):** clean text → voice with `narration` sample → (Google) SSML breaks between paragraphs;
  (OpenAI) instructions "warm documentary narrator, medium pace"; (ElevenLabs) stability high-ish, similarity mid (COMMUNITY).
- **IVR/assistant:** short sentences; explicit pauses; test numbers/dates readback; Google `<say-as interpret-as="telephone">`.
- **Persian TTS:** Google SSML `<phoneme>` IF fa voice exists (UNVERIFIED); else OpenAI instructions + respelled FA
  (UNVERIFIED); always 1-paragraph test first.
- **Singing-ish/spoken-word over music:** prefer Udio `[Spoken Word]` / Suno `[Spoken]` (COMMUNITY) over TTS comping.

### D4. SFX recipes (text→SFX)
- **Beatoven maestro SFX (OFFICIAL paradigm):** single-scene prompt: `[subject] + [action] + [material/space] + [quality]`,
  e.g. `heavy wooden door creaking shut in a stone hallway, close-mic, no reverb tail` (pattern generalized — params UNVERIFIED).
- **Loudly Sample Generator (OFFICIAL):** musical phrasing with key + BPM: `dark riser into dubstep drop, D minor, 140 BPM`;
  `vinyl crackle bed, no melody` (pattern from official example).
- One sound per prompt; no music beds unless asked; generate 3 takes, keep best (Loudly returns 3 by default).

---

## Sheet E — Freshness · contradictions · unknown-platform template

### E1. Freshness protocol (binding on the Director)
1. Every pack carries `Freshness: 2026-10-29` + per-fact labels. Facts older than ~90 days are "stale-risk".
2. **With web access:** before finalizing any pack, re-check: (a) platform's official docs/help Terms+pricing pages;
   (b) model/version names; (c) limits (chars, durations, downloads). If changed → new pack wins, note the delta.
3. **Without web access:** say so in one line; use stamped knowledge; mark all limit/license facts "as of 2026-10-29 —
   verify in-app"; never invent new model names or loosened rights.
4. Never silently resolve conflicts — surface them (log below) and pick only with user consent or a labeled default.

### E2. Contradiction / gap log (must surface, never silently pick)
| # | Conflict | Status |
|---|---|---|
| 1 | Suno Style/Lyrics char limits: 200/3000/80 vs 1000/5000 vs <950 | OFFICIAL silent; COMMUNITY version-dependent; verify in-app |
| 2 | Suno native song length: ~4 min vs Max-Mode->2 min framing | OFFICIAL: Max Mode for >2 min; native figure COMMUNITY |
| 3 | Suno mode naming: "Custom" vs "Advanced" | both seen live on suno.com 2026-08-26 (COMMUNITY); transcripts (2025–26) say Simple/Custom |
| 4 | Udio commercial rights: old (paid owns + commercial OK) vs ToS Nov 2025 (company owns, none) | Terms CHANGED; current ToS wins; warn loudly |
| 5 | Udio max length: 2:10 clips ×10 sections vs "up to 15 min" (2024 video blog) | OFFICIAL: ≤10 sections; total-time claims COMMUNITY/old |
| 6 | Artist-name prompts: Udio officially teaches `in the style of X` vs Suno reportedly blocks names | Udio OFFICIAL (no voice copy claimed); Suno block UNVERIFIED officially — Director still refuses living-artist cloning; descriptors only |
| 7 | Persian rendering quality on every vocal platform | zero official statements found → ALL UNVERIFIED; test-clip loop mandatory |
| 8 | Stable Audio license, DiffRhythm, ElevenLabs SFX, Beatoven/Mureka/SOUNDRAW/Mubert/Loudly-Terms tiers | NOT opened → no definitive rules; gaps for monthly refresh |

### E3. Unknown-platform research-and-adapt template
When the target platform/model is unknown to the Director:
1. Ask for (or fetch, with web): official docs URL, input fields + limits, tag syntax, duration/extend, pricing/Terms URL.
2. Classify paradigm: (a) field+tags (Suno-like) · (b) NL composition plan (ElevenLabs-like) · (c) single text/image→API
   (Lyria-like) · (d) caption (MusicGen-like) · (e) param/formula (SOUNDRAW/Mubert/Loudly-like) · (f) file-pair (YuE-like).
3. Emit the pack in the closest paradigm, every line labeled with a source; mark ALL unconfirmed facts UNVERIFIED.
4. Give the user a 5-line "confirm in-app" checklist (limits, tags, duration, Persian test, Terms).
5. Without web: build from user-pasted docs only; refuse to guess limits/rights.

### E4. Monthly maintenance checklist (see `maintenance-guide.md`)
- [ ] Re-open Suno Terms + v6 FAQ + pricing; Udio Terms + plans; Mureka docs+terms; ElevenLabs music+TTS docs; Lyria docs
- [ ] Re-open SOUNDRAW/AIVA/Beatoven/Mubert/Loudly pricing + Terms (close Sheet E gaps)
- [ ] Check open-source repos (ACE-Step, YuE, AudioCraft) for new releases/licenses
- [ ] Check OpenAI TTS deprecation clock (shutdown 2027-01-06) + Google voices list (fa?)
- [ ] Run Persian test clips on ≥1 vocal platform; update Sheet A/C with results
- [ ] Update freshness stamp + contradiction log; bump version if packs changed
