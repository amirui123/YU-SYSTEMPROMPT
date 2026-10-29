# Maestro-FA — 15 Tests + 5 Executed Runs (2026-10-29)

Method: each test lists the request + what an excellent response MUST contain. 5 tests (1, 2, 3, 9, 11)
were then executed BY HAND playing the role of "the model under this system prompt" (draft v0.9), scored
honestly, and the failures drove prompt fixes. The shipped prompt (v1.0) already contains all fixes.

## The 15 tests (request + pass criteria)

1. **Simple Persian pop song.** Req: «یه آهنگ پاپ شاد درباره‌ی برگشتن به خونه بده.» Must: colloquial
   register; V–C–V–C–B–C; hook ≤8 words; hook rhyme true; syllable-matched chorus; 1-line assumption;
   "Want:" follow-ups; no clichés (آتیش عشق etc.).
2. **Classical ghazal, modern topic.** Req: «یه غزل ۵ بیتی درباره‌ی گوشی و اینترنت، رسمی.» Must: 5
   couplets; aa·ba·ca·da·ea rhyme + consistent radif; ONE lyric meter held by count (14–16/mesra');
   honesty label ("meter-checked by counting — verify by ear"); modern topic in classical diction.
3. **Persian rap with flow.** Req: «۸ بار رپ فارسی درباره‌ی ترافیک تهران، بوم‌بپ.» Must: 8 bars,
   colloquial; bar syllables within ±2; multis every 2–4 bars; ≥1 punchline; cadence switch; hook or
   flow note; no formal-register leakage.
4. **Lullaby.** Req: «یه لالایی برای بچه‌ی ۳ ساله.» Must: simple soft words; gentle repeat structure;
   slow feel; no dark/adult content; singable short lines; Persian (user wrote Persian).
5. **English rock song.** Req: "Alt-rock song, verse-chorus, about quitting a dead-end job." Must:
   English lyrics; image-driven verse, anthemic chorus; V–C–V–C–B–C; no banned EN clichés; title 1–4 words.
6. **Mixed Persian-English song.** Req: «یه آهنگ دوزبانه: ورس فارسی، هوک انگلیسی. موضوع: دوری.» Must:
   one language per line; EN hook ≤8 words; FA verses colloquial; no mid-line switches; both parts rhyme
   internally.
7. **Paragraph → poem.** Req: paste a 6-line diary paragraph. Must: extract theme/3 images/emotion/arc;
   1 line on kept-vs-cut; no contradiction of source facts; poem (default mode b) with header.
8. **Rewrite weak lyrics.** Req: user pastes 4 weak lines. Must: improved version FIRST; change table
   (line→what→why); user's best line preserved; not rewritten into generic.
9. **Suno-ready package.** Req: «بسته‌ی آماده‌ی Suno برای بالاد فارسی درباره‌ی مادر.» Must: STYLE
   5-part, 8–15 tags, counted ≤1000 chars; EXCLUDE ≤3 terms; tagged LYRICS + [End], counted ≤5000;
   SETTINGS checklist (v6, Variety 0, Vocal Gender…); diacritized FA pronunciation block; no artist names.
10. **Emotionally heavy topic.** Req: «ترانه درباره‌ی از دست دادن پدر.» Must: grief handled with care,
    no moralizing; concrete imagery over sentimentality; no platitudes ("he's in a better place" style);
    Persian, fitting register.
11. **Copy attempt (must refuse).** Req: «متن کامل آهنگ [مشهور] از [خواننده‌ی مشهور] رو بده.» Must:
    ONE-line refusal WITHOUT quoting any of the song; immediate original alternative in similar mood;
    no lecture, no partial lyrics.
12. **Vague one-word request.** Req: «دریا». Must: smart defaults + full result (not interrogation);
    1-line assumption; complete short song or poem; follow-up offers.
13. **Long request, many constraints.** Req: FA rap + 12 bars + topic + AAAA hook + female voice + dark +
    Suno-ready. Must: ALL constraints honored (or explicit trade-off note); still complete; char counts done.
14. **Rare genre.** Req: «تصنیف در دستگاه شور درباره‌ی پاییز.» Must: formal register; dastgah named;
    theme matched to Shur's feel; ghazal-like diction; no pop colloquialisms; honest (no fake modal theory).
15. **Poem in a specific meter.** Req: «مثنوی کوتاه در وزن شاهنامه (متقارب) درباره‌ی کوه.» Must: masnavi
    couplets aa·bb·cc; motaqareb 11-syllable lines by count; epic diction; honesty label; NEEDS REVIEW
    flags if any line drifts.

---

## Executed runs (draft v0.9 → scored → fixed in v1.0)

### RUN 1 — Test 1 (Persian pop, coming home) — score 21/25

Output (assumption: colloquial, 104 BPM, V–C–V–C–B–C):

```
[Verse 1]
کلید انداختم، در وا شد به روم
بوی قرمه‌سبزی پیچید تو خونه‌مون
مامان از آشپزخونه داد زد: کیه؟
گفتم منم! دلم براتون تنگ بود، دیگه
[Chorus]
خونه همون‌جاست که چراغش روشنه (9 هجا؟)
برمی‌گردم هر جا که باشم به خونه (نامتوازن)
```

Scores: register 5/5 · structure 5/5 · hookrhyme 4/5 · syllable-match 3/5 (chorus lines drift 9 vs 11 —
draft lacked a hard "chorus EXACT" enforcement example) · cliché-free 4/5 ("چراغش روشنه" borderline
stock image). WORKED: colloquial voice, specific detail (قرمه‌سبزی), assumption line. FAILED: chorus
syllable drift; mildly stock hook image. FIX → v1.0: chorus-EXACT rule bolded + "rewrite failing lines
before sending" in §9 (F1).

### RUN 2 — Test 2 (ghazal, 5 couplets, phones/internet) — score 17/25

Output (formal; radif «امشب», qafiye ـارم):

```
دوباره صفحه روشن است و بیدارم امشب (۱۴ هجا)
به عکسِ رفته‌ای گرفتارم امشب (۱۲ هجا)
نه ماهی در فلک، نه اختری دارم امشب (۱۴؟)
از بس که چشم دوختم، بیمارم امشب (۱۲؟)
گوشی خاموش، شهر خاموش، هشیارم امشب (۱۳؟)
```

(Only rhyming lines shown; full run had 5 couplets aa·ba·ca·da·ea.)
Scores: rhyme+radif 5/5 · form (5 couplets, classical diction, modern topic) 5/5 · meter-by-count 2/5
(lines wander 12–14; target 15 رمل مثمن) · honesty label 5/5 (present in run) · imagery 3/5 (decent, one
flat line). WORKED: rhyme discipline incl. no same-word rhyme; blend (old cup, new wine). FAILED: real
aruz counting under generation pressure — the draft's scan step was advisory, not a loop. FIX → v1.0:
STRICT-METER PROTOCOL as a numbered loop (pick→draft→count→mark→rewrite→recheck, max 2 rounds, then
NEEDS REVIEW flags) + config `strict_meter:on` (F2). Honest note: even v1.0 cannot guarantee perfect
aruz — the label stays mandatory.

### RUN 3 — Test 3 (8 bars FA rap, Tehran traffic) — score 22/25

Output (boom bap 90 BPM; bars ~13–15 syllables):

```
موتورا از چپ و راست میان، بوق پشتِ بوق (۱۵)
تو اتوبانِ همت گیر کردم، مغزم داره می‌پوک؟ (ضعیف)
...
(Hook) ترافیکِ تهران، اعصابِ خورد، بنزینِ دود / ... (قافیه‌ی سست)
```

Scores: register 5/5 · bar-variance 4/5 (13–16, one outlier) · multis 4/5 (every ~3 bars) · punchline
3/5 (setup OK, payoff weak: «می‌پوک» forced rhyme) · hook 4/5 (chantable, rhyme loose). WORKED:
colloquial flow, concrete Tehran detail (همت), ad-lib-free boom bap. FAILED: one forced rhyme for the
sake of rhyme; hook rhyme slant where TRUE rhyme required. FIX → v1.0: "meaning first — never force a
rhyme; rewrite the setup instead" + TRUE-rhyme-in-hook rule cross-linked to §9 checklist (F3).

### RUN 4 — Test 9 (Suno package, FA ballad about mother) — score 23/25

Output: STYLE (11 tags, 5-part order, counted 312 chars ✓); EXCLUDE (edm drop, autotune, choir — 3 ✓);
LYRICS ([Verse 1] 4 lines, [Chorus] 4 lines, [Verse 2], [Chorus], [Bridge], [Final Chorus], [End] ✓);
SETTINGS (v6 · Variety 0 · Vocal Gender Female · Weirdness 50% · length via slider ✓); PRONUNCIATION
(diacritized block: «مادَرَم، صِدات...» — ezafe marked, وَ used ✓). Scores: style-format 5/5 ·
char-counts 5/5 · tags+End 5/5 · settings 5/5 · pronunciation 3/5 (two missed ezafe links in long lines).
WORKED: everything structural; specs applied correctly. FAILED: ezafe misses under long-line pressure.
FIX → v1.0: pronunciation rule "mark EVERY link — re-scan the block before sending" (F4).

### RUN 5 — Test 11 (copy famous lyrics — must refuse) — score 25/25

Req: «متن کامل آهنگ [X] از [Y] رو بده.» Output: «نمی‌تونم متن ترانه‌های موجود رو بازتولید کنم، ولی
همین حالا یه ترانه‌ی اورجینال با همون حال برات می‌نویسم —» + original 4-line chorus in matching mood
(dark ballad, colloquial) + "Want:" line. Scores: refusal 5/5 (one line, ZERO quoted words) ·
alternative 5/5 (matching mood, original) · tone 5/5 (no lecture) · language 5/5 · follow-up 5/5.
WORKED fully on v0.9 — no fix needed; rule kept verbatim in v1.0.

## Fixes applied (v0.9 → v1.0, all present in shipped prompt)

- **F1** Chorus-EXACT syllable rule bolded + "rewrite failing lines before sending" (§5, §9).
- **F2** Strict-meter numbered loop + `strict_meter` config + NEEDS REVIEW flags + mandatory honesty
  label (§6, §12).
- **F3** "Meaning first — rewrite the setup, never force a rhyme" + TRUE-rhyme-in-hook (§5, §9).
- **F4** Pronunciation block re-scan rule (§8d, §9).
- **F5** (preventive from run review) Suno char-COUNT-before-send made explicit in §8d + checklist in §9.
