# منابع و اعتبارها (Sources & Credits)

> اصل: از هیچ منبعی متن یا کد verbatim کپی نشده است. ستون «چه چیزی گرفته شد» فقط ایده/الگو/شاهد را می‌گوید. جزئیات کامل بررسی در `research/` هست.

## الف) مخازن گیت‌هاب (۱۵ مورد بررسی‌شده، فراداده از GitHub API در ۲۰۲۶-۱۰-۲۹)

| مخزن | URL | مجوز (طبق API) | چه چیزی گرفته شد |
|---|---|---|---|
| microsoft/PromptKit | https://github.com/microsoft/PromptKit | MIT | ایدهٔ پرامپت ماژولار (persona/protocol/format/template) — مبنای `modules.fa.md` |
| promptfoo/promptfoo | https://github.com/promptfoo/promptfoo | MIT | الگوی assert قطعی + rubric + رگرسیون — مبنای `tests.fa.md` و بخش eval راهنما |
| stanfordnlp/dspy | https://github.com/stanfordnlp/dspy | MIT | ایدهٔ جداکردن قرارداد وظیفه از متن prompt و بهینه‌سازی با معیار — در راهنمای بهبود |
| langchain-ai/langgraph | https://github.com/langchain-ai/langgraph | MIT | الگوی وضعیت صریح و human-in-the-loop — در مرز ابزار و M3 |
| dair-ai/Prompt-Engineering-Guide | https://github.com/dair-ai/Prompt-Engineering-Guide | MIT | نقشهٔ تکنیک‌ها برای پوشش کامل پژوهش؛ بدون کپی متن |
| danielmiessler/fabric | https://github.com/danielmiessler/fabric | MIT | ایدهٔ patternهای وظیفه‌محور قابل‌استفادهٔ مجدد — در M1 و M2 |
| openai/openai-cookbook | https://github.com/openai/openai-cookbook | MIT | راهنمای پیاده‌سازی APIمحور (tool calling، خروجی ساختاریافته) — در M5 و M11 |
| google-gemini/cookbook | https://github.com/google-gemini/cookbook | Apache-2.0 | نمونه‌های Gemini (grounding، خروجی ساختاریافته) — در M11 |
| anthropics/prompt-eng-interactive-tutorial | https://github.com/anthropics/prompt-eng-interactive-tutorial | بدون مجوز اعلام‌شده | فقط ایدهٔ آموزشی؛ کپی نشد |
| anthropics/courses | https://github.com/anthropics/courses | NOASSERTION | فقط ایدهٔ آموزشی؛ کپی نشد |
| Piebald-AI/claude-code-system-prompts | https://github.com/Piebald-AI/claude-code-system-prompts | MIT (مخزن) | یافتهٔ سطح‌بالا: prompt عامل چندبخشی/شرطی است، نه یک رشته — در طراحی ماژولار؛ هیچ متنی کپی نشد |
| asgeirtj/system_prompts_leaks | https://github.com/asgeirtj/system_prompts_leaks | CC0-1.0 (فرادادهٔ مخزن) | فقط مشاهدهٔ الگوی کلی؛ هیچ متن prompt شخص ثالث کپی/اقتباس نشد (اصالت و حقوق نامشخص) |
| f/prompts.chat | https://github.com/f/prompts.chat | NOASSERTION | فقط شناخت الگوهای رایج قالب؛ کپی نشد |
| langfuse/langfuse | https://github.com/langfuse/langfuse | NOASSERTION (طبق API) | ایدهٔ چرخهٔ نسخه→اجرا→بازبینی→بهبود — در راهنمای بهبود؛ کپی نشد |
| TrustAI-laboratory/learn-prompt-hacking | https://github.com/TrustAI-laboratory/learn-prompt-hacking | MIT | دسته‌بندی حمله‌ها برای طراحی تست‌های ۳ تا ۵ و ۹ |

یادداشت تکی هر مخزن: `research/github/items/` — فهرست: `research/github/README.md`

## ب) منابع وب و مقاله‌ها (۳۱ منبع، متن اصلی باز و خوانده شد)

| منبع | URL | تاریخ/نسخه | چه چیزی گرفته شد |
|---|---|---|---|
| Anthropic — Prompt engineering overview | https://platform.claude.com/docs/en/build-with-claude/prompt-engineering/overview | سند زنده (بررسی ۲۰۲۶-۱۰-۲۹) | اول معیار و eval، بعد prompt — در راهنمای بهبود |
| Anthropic — Prompting best practices | https://platform.claude.com/docs/en/build-with-claude/prompt-engineering/claude-prompting-best-practices | سند جاری | دستور روشن، مثال متنوع، XML، راهنمای خاص‌مدل — در هسته و M11 |
| Anthropic — Mitigate jailbreaks | https://platform.claude.com/docs/en/test-and-evaluate/strengthen-guardrails/mitigate-jailbreaks | سند زنده | محتوای ابزار = دادهٔ نامطمئن، کمترین مجوز، غربالگری — در بخش ۴ هسته |
| Anthropic — Define tools | https://platform.claude.com/docs/en/agents-and-tools/tool-use/define-tools | سند زنده | کارت ابزار (کاربرد/عدم‌کاربرد/محدودیت) — در M3 |
| Anthropic — Building effective agents | https://www.anthropic.com/engineering/building-effective-agents | ۲۰۲۴-۱۲-۱۹ | شروع ساده، ابزارِ خوب‌مستندشده — در M3 و M11 |
| Anthropic — Multi-agent research system | https://www.anthropic.com/engineering/multi-agent-research-system | صفحهٔ رسمی (حدود ۲۰۲۵) | delegation صریح و هزینهٔ توکن چندعاملی — در تحلیل (رد برای دستیار عمومی) |
| Anthropic — Long-running agents | https://www.anthropic.com/engineering/effective-harnesses-for-long-running-agents | ۲۰۲۵-۱۱-۲۶ | کار مرحله‌ای و معیار عبور — در راهنمای بهبود |
| Google — Prompt design strategies | https://ai.google.dev/gemini-api/docs/prompting-strategies | سند زنده | دستور روشن، شکستن کار، fallback — در هسته |
| Google — Gemini 3 developer guide | https://ai.google.dev/gemini-api/docs/gemini-3 | سند زنده | concise/direct برای مدل جدید، effort در API — در M11 |
| Google — Live API best practices | https://ai.google.dev/gemini-api/docs/live-api/best-practices | سند زنده | ترتیب persona→قواعد→ابزار→guardrail — در ساختار ماژول‌ها |
| OpenAI — Prompt engineering | https://developers.openai.com/api/docs/guides/prompt-engineering | سند زنده | نقش/هدف/دستور/مثال — در هسته |
| OpenAI — Agent builder safety | https://developers.openai.com/api/docs/guides/agent-builder-safety | سند زنده | دادهٔ نامطمئن در developer-message نچسبان، schema، تأیید ابزار — در بخش ۳ و ۴ هسته |
| OpenAI — Evaluation best practices | https://developers.openai.com/api/docs/guides/evaluation-best-practices | سند زنده | eval برای خروجی متغیر + قضاوت انسانی — در راهنمای بهبود |
| OpenAI — Function calling | https://developers.openai.com/api/docs/guides/function-calling | سند زنده | چرخهٔ فراخوان/اجرا/نتیجه در کد — در M3 |
| OpenAI — Structured outputs | https://developers.openai.com/api/docs/guides/structured-outputs | سند زنده | schema = کنترل قالب، نه تضمین حقیقت — در M5 |
| OWASP — LLM01:2025 Prompt Injection | https://genai.owasp.org/llmrisk/llm01-prompt-injection/ | ۲۰۲۵ | دسته‌بندی direct/indirect و ۷ راهبرد کاهش — در بخش ۴ هسته و تست‌ها |
| NIST — AI RMF GenAI Profile | https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.600-1.pdf | ۲۰۲۴-۰۷ | چارچوب ریسک چرخه‌عمر — در راهنمای بهبود |
| Wei et al. — Chain-of-Thought | https://arxiv.org/abs/2201.11903 | ۲۰۲۲ | استدلال مرحله‌ای برای مسائل پیچیده؛ بدون تعمیم کور — در تحلیل |
| Wang et al. — Self-Consistency | https://arxiv.org/abs/2203.11171 | ۲۰۲۲–۲۰۲۳ | رأی چندمسیره با هزینهٔ چندبرابر — در تحلیل (مشروط) |
| Yao et al. — ReAct | https://arxiv.org/abs/2210.03629 | ۲۰۲۲–۲۰۲۳ | درهم‌تنیدگی فکر/اقدام/مشاهده — در M3 |
| Shinn et al. — Reflexion | https://arxiv.org/abs/2303.11366 | ۲۰۲۳ | بازخورد زبانی با سیگنال بیرونی — در M10 (مشروط) |
| Yao et al. — Tree of Thoughts | https://arxiv.org/abs/2305.10601 | ۲۰۲۳ | جست‌وجوی شاخه‌ای پرهزینه — در تحلیل (رد برای گفت‌وگوی عادی) |
| Liu et al. — Lost in the Middle | https://arxiv.org/abs/2307.03172 | ۲۰۲۳ | حساسیت به جایگاه context — در M11 (eval placement) |
| Madaan et al. — Self-Refine | https://arxiv.org/abs/2303.17651 | ۲۰۲۳ | بازنویسی با بازخورد، با ریسک تثبیت خطا — در M10 (مشروط) |
| Lewis et al. — RAG | https://arxiv.org/abs/2005.11401 | ۲۰۲۰ | حافظهٔ پارامتری + بازیابی — در M4 |
| Wallace et al. — Instruction Hierarchy | https://arxiv.org/abs/2404.13208 | ۲۰۲۴ | تقدم دستور ممتاز (آموزشی، نه تضمین prompt-only) — در بخش ۴ هسته |
| Hines et al. — Spotlighting | https://arxiv.org/abs/2403.14720 | ۲۰۲۴ | نشانه‌گذاری منشأ به‌عنوان کمک، نه قفل — در M4 |
| Yi et al. — BIPIA | https://arxiv.org/abs/2312.14197 | ۲۰۲۳–۲۰۲۵ | بنچمارک تزریق غیرمستقیم — در تست ۴ |
| Zhan et al. — InjecAgent | https://arxiv.org/abs/2403.02691 | ۲۰۲۴ | بنچمارک تزریق در عامل ابزارمحور — در تست‌های ۴ و ۷ |
| Zhu et al. — PromptRobust | https://arxiv.org/abs/2306.04528 | ۲۰۲۳–۲۰۲۴ | نویز/تایپو در eval — در تست ۱۰ |
| Promptfoo docs — Assertions | https://www.promptfoo.dev/docs/configuration/expected-outputs/ | مستندات زنده | انواع assert — در راهنمای بهبود |

جدول کامل با شیوهٔ بررسی و رتبه‌بندی اعتبار: `research/web/sources.md` — جمع‌بندی: `research/web/findings.md`

## ج) ویدئوها (۴ ویدئو، transcript کامل خوانده شد — ویدئو «تماشا» نشد)

| ویدئو | URL | دسترسی | چه چیزی گرفته شد |
|---|---|---|---|
| Anthropic — Prompting 101 | Code w/ Claude | https://www.youtube.com/watch?v=ysPbXH0LpIE | transcript کامل (۴ chunk) از سرویس مستقل | تکرار تجربی prompt، context ثابت، XML، مثال، ترتیب تحلیل — در M2 و راهنما |
| OpenAI/Girl Geek X — Prompt Design for GPT-3 | https://www.youtube.com/watch?v=2ltOaInDD-s | transcript کامل صفحهٔ ناشر (۳ chunk) | few-shot، مثال نقض، قرارداد «نامشخص» — در هسته؛ تنظیمات ۲۰۲۱ نادیده گرفته شد |
| Simon Willison — Prompt Injection explained | https://www.youtube.com/watch?v=FgxwCaL6UTA | transcript+اسلاید صفحهٔ سخنران (۴ chunk) | رد دفاع prompt-only، جداسازی trust boundary — در بخش ۴ هسته |
| Akamai — Prompt Engineering in Web Dev | https://www.youtube.com/watch?v=pK6WzlTOlYw | transcript کامل (۶ chunk) از سرویس مستقل | template سمت backend، خروجی قابل-parse، درسِ شکست regex — در M5 |

تحلیل کامل: `research/web/videos.md`
