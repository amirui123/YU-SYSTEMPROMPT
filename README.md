# YU-SYSTEMPROMPT — سامانهٔ پرامپت پژوهشی فارسی

سامانهٔ پرامپت آمادهٔ استفاده برای **دستیار عمومیِ پژوهش‌محور و ابزارپذیر (فارسی‌زبان)**، ساخته‌شده فقط از منابع واقعی و راستی‌آزمایی‌شده.

> **فرض شفاف:** حوزه و مدل هدف در درخواست اولیه مشخص نبود؛ این نسخه provider-neutral و ماژولار طراحی شد تا با هر مدل/دامنه قابل‌تطبیق باشد. جزئیات مدل هدف را در لایهٔ integration بگذارید، نه در متن prompt.

## شروع سریع

1. `prompt/system_prompt.fa.md` را بخوان و `{{...}}`‌ها را پر کن.
2. از `prompt/modules.fa.md` فقط ماژول‌های لازم را به انتها اضافه کن (راهنمای مونتاژ داخل همان فایل).
3. هر ۱۰ تست `prompt/tests.fa.md` را در نشست تازه اجرا کن؛ تست‌های ۳، ۴، ۵ و ۷ باید ۴/۴ قبول شوند.
4. برای نگهداری: `prompt/improvement-guide.fa.md` — برای منابع: `prompt/sources-and-credits.md`.

## ساختار مخزن

```text
prompt/
  system_prompt.fa.md      # پرامپت نهایی آمادهٔ الصاق (هسته)
  modules.fa.md            # نسخهٔ ماژولار (M0 تا M11)
  tests.fa.md              # ۱۰ تست با رفتار مورد انتظار و جدول امتیاز
  improvement-guide.fa.md  # بهبود، ارزیابی، دفاع چندلایه، مهاجرت مدل
  sources-and-credits.md   # همهٔ منابع با URL، مجوز و مورد استفاده
analysis/
  comparison.md            # فاز ۴: جدول مقایسه، رتبه‌بندی، اجماع/اختلاف، تصمیم‌ها
research/
  github/README.md + items/  # فاز ۱: ۱۰ جست‌وجو، ۱۰۰ نتیجه، ۱۵ مخزن بررسی‌شده
  web/sources.md             # فاز ۲: ۳۱ منبع وب/مقاله با شیوهٔ بررسی
  web/findings.md            # جمع‌بندی یافته‌های وب
  web/videos.md              # فاز ۳: ۴ ویدئو با transcript کامل
```

## اعداد پژوهش

- ۱۰ جست‌وجوی جداگانهٔ گیت‌هاب، ۱۰۰ نتیجهٔ مرور اولیه، ۱۵ مخزن منتخب (فراداده از GitHub API)، ۹ کلون کم‌حجمِ دارای مجوز MIT/Apache-2.0
- ۳۱ منبع وب/مقاله (مستندات رسمی هر سه ارائه‌دهنده، OWASP، NIST، مقاله‌های arXiv) — متن اصلی باز و خوانده شد
- ۴ ویدئو با transcript کامل (Anthropic، OpenAI، Simon Willison، Akamai) — ویدئو «تماشا» نشد، متن گفتار تحلیل شد

## اصول رعایت‌شده

- هیچ متن یا کدی از منابع کپی نشد؛ فقط ایده و الگو.
- از مخازن بی‌مجوز/نامشخص و promptهای لو‌رفته هیچ متنی بازاستفاده نشد.
- هیچ ادعای امنیتیِ prompt-only داده نشد؛ دفاع چندلایه (معماری، schema، مجوز، تأیید انسانی) الزامی است.

## Songwriter-FA (Maestro-FA) — Master Songwriter & Poet system prompt

Production-grade system prompt for AI Studio: writes original songs/poems in any genre, elite in
Persian (forms, aruz, register, dastgah), Suno-ready packages (specs verified 2026-10-29).

- `songwriter/system-prompt.en.md` — main prompt (English, AI Studio edition)
- `songwriter/system-prompt.fa.md` — natural Persian version
- `songwriter/compact.en.md` — compact version (<1,500 words)
- `songwriter/reference-sheets.md` — 4 attachable sheets (genres, Persian forms+meters, rhyme&flow, clichés)
- `songwriter/sources-and-credits.md` — every source with URL + verification date
- `songwriter/tests.md` — 15 tests + 5 executed runs with honest scores + fixes
- `songwriter/report.md` — final report (structure, unverified items, risks, next steps)

## Songwriter system (Maestro-FA v1.0)
Persian lyric/vocal songwriting prompt system in `songwriter/`: main EN prompt (`system-prompt.en.md`, AI Studio
Edition) + natural Persian translation + compact version + 4 reference sheets (genre/BPM, Persian forms+meters,
rhyme&flow, banned clichés) + sources & credits + 15 tests with 5 scored runs + final report. Research: Persian
metres/dastgah, song structure, Suno custom-mode guides, genre BPM chart (2026-10-29).

## Audio director system (Maestro-AD v1.0)
Audio Prompt Director in `audio-director/`: production-grade EN system prompt (AI Studio Edition) that converts
lyrics/text + style/mood + target platform into ready-to-paste prompt packages for 20 tools across 5 categories
(vocal generators, open-source/local, royalty-free BGM, TTS, SFX), with per-platform Persian + license sections,
unknown-platform research-and-adapt, and a freshness protocol. Includes FA translation, compact version, 5 reference
sheets (A–E), sources & credits (37 sources + gap list), maintenance guide with monthly checklist, 15 tests + 5 scored
runs, and final report. Freshness baseline: 2026-10-29.

## App scout system (AppScout v1.0)
Software-discovery agent in `app-scout/`: production-grade EN system prompt (15 modules: request understanding,
10-angle search engine with maintained-fork + alternatives playbooks, 6-axis vetting protocol with trust levels,
legitimate-access router, community-versions handler, piracy-request handler, fixed output format, install helper,
freshness protocol, Persian behavior, iteration mode, silent QC, style, 4 few-shot examples). Includes natural FA
translation, compact version, 6 reference sheets (GitHub cheat, trusted sources, per-OS install commands, vetting
checklist, license cheat, red flags), sources & credits (24 sources + gap list), maintenance guide, 15 tests + 5
live-grounded scored runs, and final report. Freshness baseline: 2026-10-29.

## Deep research system (DeepScout v1.0)
Deep-research agent in `deep-scout/`: production-grade EN system prompt (16 modules: identity, request understanding
+ QUICK/STANDARD/DEEP auto-depth, 10-stage pipeline, search engine with query engineering + GitHub mastery, CRAAP+SIFT
credibility scoring, VERIFIED/LIKELY/UNVERIFIED verification, HIGH–DO-NOT-USE vetting, long-run ops with saturation
stop, untrusted-content safety, fixed a–i output format, freshness, Persian/multilingual, iteration, QC, style,
5 few-shot examples). Includes natural FA translation, compact version (<1,500 words), 8 reference sheets
(query-expansion, GitHub patterns, operators, credibility, vetting, log template, scoring rubric, injection
red-flags), sources & credits (27 entries + dead-end list), maintenance guide, 15 tests + 5 live-grounded scored
runs (23/25/24/23/24), and final report. Freshness baseline: 2026-10-29.
