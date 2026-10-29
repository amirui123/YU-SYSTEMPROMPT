# Audio Prompt Director — Sources & Credits (v1.0)

All sources opened 2026-10-29 unless noted. Consumption method: full-page read via fetch (chunks noted);
video transcripts via YouTubeToTranscript (real transcripts read in full). Labels: OFFICIAL / COMMUNITY-TESTED /
UNVERIFIED. No copyrighted lyrics reproduced; no artist-voice cloning guided.

## 1. Suno (official)
1. Terms of Service — https://suno.com/terms (redirected from /terms-september-2026), rev 2026-08-10, eff 2026-09-03;
   chunks 0–4 of 10 read (conduct, fees, IP, submissions license, Pro/Premier assignment, free-tier limits, Remix ban,
   commercial-use-by-Download, watermark). Taken: full license matrix, ownership, remix rule.
2. ToS-update blog — https://suno.com/blog/suno-updates-tos (2026-08; full read). Taken: download quotas
   Free 7 lifetime / Pro 20 / Premier 60 / Studio unlimited; paid downloads = commercial rights.
3. v6 FAQ — https://help.suno.com/en/articles/13924481 (full read). Taken: v6/v6-wild/v6-mini tiers, 10 credits = 2 songs,
   Variety slider, Max Mode (>2 min, covers, consistency), retired old models, library preserved.
4. Own-lyrics article — https://help.suno.com/en/articles/2415873 (full read). Taken: input lyrics stay yours.
5. Exclude article — https://help.suno.com/en/articles/3161921 (full read). Taken: Exclude field location.
6. Vocal-gender article — https://help.suno.com/en/articles/10153473 (full read). Taken: Simple male/female words;
   Custom Vocal Gender + style descriptors.
7. Make-longer article — https://help.suno.com/en/articles/2409601 (full read). Taken: Extend + Get Whole Song flow.
8. Downloads/ToS FAQ — https://help.suno.com/en/articles/13614785 (full read). Taken: 1 song = 1 download any format,
   stems included, no rollover, cancel keeps library under free limits.
9. Making-Music category — https://help.suno.com/en/categories/550017-making-music (chunk 0 of 2). Taken: article index
   (Simple Mode, song-length, crop, replace-section, glossary, custom-models…); chunk 1 unread.
10. Introducing-v6 blog — https://suno.com/blog/introducing-v6 (2026-09-09; full read). Taken: WMG/BMG/Believe deals,
    plain-language edit, mashup, sample/isolate/beat, vibe prompting, single-lyric update.

## 2. Udio (official; all help.udio.com + udio.com)
11. Prompt Like a Master — https://help.udio.com/en/articles/10716221-create-a-song-with-your-own-lyrics
    (used prompt-guide URL variant; chunk 0 of 2 read; published 2025-03-07). Taken: topic+tags, custom lyrics editor,
    [Scream]/[Chorus]/[Guitar Solo], (backing), syllable/accent pronunciation, Instrumental Mode, Style Reduction,
    Manual Mode. Chunk 1 unread.
12. Guidance tags — https://help.udio.com/en/articles/…/guidance-tags (full read, 2025-04-30). Taken: 28-tag list,
    `/` autocomplete, guidance-not-commands.
13. Own-lyrics article (full read, 2025-03-14). Taken: Custom mode + Lyrics/Extended Editor + write-for-me/regenerate/history.
14. Extend article (full read, 2025-03-07). Taken: before/after/intro/outro/crop, ≤10 sections, blank = instrumental.
15. Create-first-song article (full read, 2025-03-14). Taken: 32 s default / 2:10 clips, 2 songs per prompt.
16. KillerM's Lyrics Guide (official help-center community guide, 2025-10-08; chunks 0 + 2 of 4). Taken: human>AI lyrics,
    syllable discipline, inpaint rule, section guidelines, deep-dive structures. Chunks 1 + 3 unread.
17. Terms of Service — https://www.udio.com/terms-of-service (rev 2025-11-12; chunks 0–4 of 8). Taken: training use of
    inputs, NO downloads/distribution, NO commercial use, company owns Output + user assignment, personal in-app use only,
    free-user attribution. Chunks 5–8 unread.

## 3. Other vocal generators (official docs)
18. Mureka API `POST /v1/song/generate` — https://platform.mureka.ai/docs/api/operations/post-v1-song-generate.html
    (full read). Taken: lyrics ≤5000, prompt ≤1024, models auto/7.6/o2/8/9/9.5, n≤3, gender, reference/vocal/melody ids,
    stream, async polling, cURL sample.
19. ElevenLabs Music docs + best-practices — https://elevenlabs.io/docs (redirected to
    /docs/overview/capabilities/music) + best-practices page (chunk 0 each). Taken: v1/v2/v2.5, 5-question rule, studio
    vocab, arrangement narration, loop exclusion, timing cues, solo/a-cappella, ~30 s reference.
20. Google Lyria 3.5 docs — https://ai.google.dev/gemini-api/docs/music-generation (chunks 0,3,4,5 of 7). Taken: 30 s
    preview, full songs ~couple min, ≤10 images, [Verse]/[Chorus]/[Bridge], timestamps, instrumental-only,
    lyrics-lang = prompt-lang.

## 4. Open-source (official READMEs/docs)
21. YuE — https://github.com/multimodal-art-projection/YuE (chunk 0 of 6 + README blob chunk 0). Taken: YuE2
    symbolic+audio, Apache-2.0, arXiv 2609.33757, WildSongBench.
22. ACE-Step 1.5 — https://github.com/ace-step/ACE-Step-1.5 (chunk 0 of 28 + README blob chunk 0). Taken: MIT, <2 s A100,
    10 s–10 min, 50+ langs, 1000+ styles, XL 4B DiT. Community params (10–300 s, [tags], (whisper)/(falsetto), BPM/key/seed)
    from third-party guides — COMMUNITY.
23. MusicGen — https://github.com/facebookresearch/audiocraft/blob/main/docs/MUSICGEN.md (chunks 0–1 of 4). Taken: MIT,
    10 models, EnCodec 32 kHz, Transformers usage, 300M/1.5B/3.3B configs. cfg 3–6, ≤30 s — COMMUNITY.
24. Stable Audio Open demo page (OFFICIAL; chunk 0). Taken: ≤47 s, tag-style + BPM.
25. awesome-ai-music-prompts — https://github.com/suno-ai-farm/awesome-ai-music-prompts (chunks 0–1 of 3). Taken:
    cross-platform tips, MusicGen/Stable-Audio examples, 5 related repos. COMMUNITY.

## 5. BGM platforms (official)
26. SOUNDRAW FAQ getting-started — https://docs.channel.io/soundraw-faq/en/articles/How-do-I-get-started-with-SOUNDRAW-b3f6fcee
    (full read). Taken: tag workflow (length/tempo/mood/genre/theme/instruments/edit).
    SOUNDRAW official blog "Revealed" (search snippet only — page JS-blocked): tag-based, no text prompts, Pro Mode, Neo bot.
27. AIVA homepage + pricing — https://www.aiva.ai/ (full read). Taken: 250+ styles, custom models, audio/MIDI influence,
    editor; Free/Standard/Pro tiers + copyright/monétisation/downloads/durations. (help.aiva.ai = 401; Helpdesk via
    COMMUNITY review: sonilo.com blog 2026-09-24.)
28. Beatoven.ai homepage — https://www.beatoven.ai/ (chunk 0 of 2). Taken: maestro text-to-music + maestro SFX
    (text→SFX), MP3/WAV downloads, pay-per-track or subscribe, API. Chunk 1 unread. (help.beatoven.ai fetch failed.)
    Workflow details (title/duration/tempo/genre/emotion) — COMMUNITY (aimusic.so tutorial, aiformusic.org).
29. Mubert API v3 docs — https://mubert.com/api/docs (chunk 0 of 7). Taken: REST+MCP+skill, playlist_index/duration/
    format/mode/intensity, instant durations, URL expiry, quota model.
30. Loudly FAQ — https://www.loudly.com/faq (chunk 0 of 4). Taken: Generator formula, Text-to-Music, Remixer, Sample
    Generator (text→loops/SFX), Stem Splitter, 100% royalty-free commercial, 100% royalties, 50+ platforms, 60–200 BPM.
    No-resell / Pro-ads-$100k / films-special-license lines — OFFICIAL-SNIPPET (section unopened).

## 6. TTS (official)
31. ElevenLabs TTS page — https://elevenlabs.io/text-to-speech (chunk 0 of 9). Taken: Eleven v4, 90+ languages, 7M+ users.
    Sliders/audio-tags — COMMUNITY/UNVERIFIED (API docs not opened).
32. OpenAI TTS guide — https://platform.openai.com/docs/guides/text-to-speech → redirected to
    https://developers.openai.com/api/docs/guides/text-to-speech (chunk 0 of 3). Taken: gpt-4o-mini-tts, 11 voices,
    model+input+voice+instructions, 2027-01-06 deprecation → gpt-realtime-2.1-mini, AI disclosure rule,
    https://openai.com/policies/usage-policies.
33. Google Cloud TTS basics — https://cloud.google.com/text-to-speech/docs/basics (chunk 0 of 2). Taken: text/SSML input,
    MP3/LINEAR16, voice/lang/gender/accent, AudioConfig (rate/pitch/volume), https://cloud.google.com/terms/.

## 7. Video transcripts (real transcripts read in full via YouTubeToTranscript, 2026-10-29)
34. "How to Use Custom Mode Feature Suno AI 2026" (EasyInternet, 2025-12-28) — https://www.youtube.com/watch?v=Q_aLPqvm6P8.
    Taken: Simple/Custom toggle, blank lyrics = instrumental, AI lyric writer (classic/remy models), Weirdness/Style
    Influence 50%, Vocal Gender, multi-option outputs.
35. "How To Extend A Song In Udio (Full Guide) 2025!" (Olivia Santos, 2025-05-11) — https://www.youtube.com/watch?v=JNjeaRhZdw8.
    Taken: select → Extend → intro/before/after/outro → adjust prompt → auto/custom/instrumental → Generate → repeat.
36. "Getting Started with SOUNDRAW…" (SOUNDRAW official channel) — https://www.youtube.com/watch?v=fqLcgF8Hf1M. Taken:
    length/tempo/genre/mood/theme → list → Create Similar → section intensity/builds → Pro Mode (length/BPM/instruments/
    key/stem volumes/fade) → download track+stems → royalty-free under membership.
37. "How to Use Custom Mode in Suno AI (Full Guide 2025)" (Basic Value, 2025-10-04) — https://www.youtube.com/watch?v=2VCRItR1ke4.
    Taken: own-audio upload, Persona (pro), own/AI lyrics, Advanced = pro features, style+gender example.

## 8. GitHub landscape searches (5 queries, 2026-10-29; snippets/leads only)
MusicGen/AudioCraft · ACE-Step · YuE · awesome Suno/AI-music prompts · Stable Audio Open — used for shortlisting; no
verbatim reuse. (Prior mission's 10 GitHub searches covered prompt-engineering repos, not audio.)

## 9. Reused prior research (same repo, same standards)
- `songwriter/reference-sheets.md` Sheet 1 (BPM chart from LowEndCandy 2026-10-10) and Sheet 2 (dastgah/meters from
  Wikipedia Persian metres/Dastgah) — summarized in Sheet B with pointer; not re-fetched.
- Suno v6-era community specs in songwriter §8d (stamped 2026-10-29) — superseded by this mission's official reads
  wherever they conflict; conflicts logged in Sheet E.

## NOT verified (gaps — no definitive Director rules from these)
DiffRhythm · Stable Audio license · ElevenLabs SFX API · Mureka pricing/Terms · SOUNDRAW pricing/Terms · AIVA Terms page
· Beatoven pricing/Terms · Mubert free tier/ownership · Loudly Terms page · ElevenLabs TTS API prompting · ElevenLabs
Music tiers/Terms · Lyria music Terms · fa voices (Google/ElevenLabs/OpenAI) · FA vocal rendering on ALL song generators
· Suno official char limits · Suno Simple-Mode article · Udio current plans page · Udio ToS chunks 5–8 · Suno ToS chunks
5–9 · KillerM chunks 1,3 · Udio prompt-guide chunk 1 · Mubert docs chunks 1–6 · Loudly FAQ chunks 1–3 · Beatoven homepage
chunk 1 · OpenAI TTS chunks 1–2 · Google TTS chunk 1 · ElevenLabs TTS chunks 1–8.
