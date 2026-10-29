# بررسی ویدئوها با متن کاملِ transcript/captions

**روش مشترک:** صفحهٔ ویدئوی YouTube و فرادادهٔ آن باز شد و متن گفتار با ابزار `fetch_page` واکشی شد؛ برای دو ویدئو متن در صفحهٔ خود ناشر/سخنران بود و برای دو مورد از YouTubeToTranscript.com، سرویس مستقل استخراج transcript، گرفته شد. همهٔ chunkهای transcript در دسترس واکشی و خوانده شد: Anthropic (۰–۳)، Girl Geek X (۰–۲)، Simon Willison (۰–۳)، Akamai (۰–۵). این‌ها «تحلیل‌شده» هستند چون متن گفتار واقعاً در دسترس بود؛ خود ویدئو را در مرورگر پخش/بینایی‌سنجی نکردم و هم‌زمانی کپشن با صوت یا محتوای تصویری را مستقل راستی‌آزمایی نکردم. برای دو استخراجِ شخص ثالث، ابزار وابسته به YouTube نیست و تأیید رسمی/وابستگی ندارد. بنابراین تحلیل به transcript متکی است؛ ادعای بررسی اسلاید/جزئیات صرفاً دیداری نمی‌کنم.

## 1) Anthropic — Prompting 101 | Code w/ Claude

- ویدئو: https://www.youtube.com/watch?v=ysPbXH0LpIE
- متن transcript: https://youtubetotranscript.com/transcript?v=ysPbXH0LpIE&current_language_code=en
- ناشر/گویندگان: کانال رسمی Anthropic؛ Hannah Moran و Christian Ryan، Applied AI.
- تاریخ/مدت: ارائه در 2025-05-22، انتشار کانال 2025-07-31، مدت 24:52 (فرادادهٔ صفحهٔ YouTube).
- روش: صفحهٔ رسمی YouTube را باز کردم و description/گویندگان/مدت را خواندم؛ transcript انگلیسی را از YouTubeToTranscript.com در چهار chunk (همهٔ متن، 0–3) دریافت کردم.
- برداشت: مثال واقعی‌نما و تکرارشونده نشان می‌دهد prompt خوب با آزمون تجربی رشد می‌کند: ابتدا مسئله را کم‌تعریف می‌گذارند و مدل سناریوی اسکی را اشتباه می‌فهمد؛ سپس زمینهٔ فرم و دادهٔ ثابت، ساختار XML، چند نمونه، ترتیب تحلیل فرم سپس طرح، قید عدم حدس، یادآوری task و قالب خروجی را اضافه می‌کنند. این ویدئو بهترین شاهد عملی برای context، example، ترتیب گام‌ها و eval است.
- محدودیت: مدل و تنظیمات نمایش‌داده‌شدهٔ نسخهٔ Claude در 2025 است؛ جمله‌های مربوط به chain-of-thought/«scratchpad» و تنظیمات مدل را راهنمای امروز یا مجوز افشای reasoning تلقی نمی‌کنم. تجربهٔ یک demo و شرکتِ ارائه‌دهنده است، نه مطالعهٔ مستقل. Transcript استخراجی ممکن است خطای ASR داشته باشد و timestamp نداشت.

## 2) Ashley Pilipiszyn (OpenAI) — Prompt Design & Engineering for GPT-3

- ویدئو: https://www.youtube.com/watch?v=2ltOaInDD-s
- صفحهٔ ناشر و transcript: https://girlgeek.io/prompt-design-engineering-for-gpt-3-ashley-pilipiszyn-with-openai-video-transcript/
- ناشر/گوینده: Girl Geek X Elevate 2021؛ سخنران در زمان ارائه Technical Director در OpenAI.
- تاریخ/مدت: 2021-03-26، 21:40 (صفحهٔ YouTube/ناشر).
- روش: صفحهٔ YouTube را برای فراداده/لینک transcript باز کردم؛ transcript کامل در صفحهٔ ناشر Girl Geek X بود و در سه chunk (0–2) خوانده شد.
- برداشت: مثال‌های صفر/یک‌نمونه‌ای، مثال نقض، برچسب‌گذاری/طبقه‌بندی و context برای نشان دادن task؛ شخصی‌سازی prompt و ترکیب taskها؛ نکتهٔ مفید: درخواست `unknown` در سؤال بی‌پاسخ باید به‌شکل نمونه/قرارداد طراحی شود، نه امید به لحن confident. پاسخ به پرسش audience دربارهٔ bias بر زمینه/مثال تأکید می‌کند.
- محدودیت: ویدئو مربوط به GPT-3 API و اصطلاحات/temperature/top-p/پارامترهای Playground سال 2021 است؛ آن‌ها در prompt نهایی وارد نشده‌اند. تجربهٔ ارائه‌دهنده و دمو، نه ارزیابی مستقل؛ متن صفحهٔ ناشر کلمات transcript را فراهم می‌کند، اما caption timing را ندارد.

## 3) Simon Willison — Prompt Injection, explained

- ویدئو: https://www.youtube.com/watch?v=FgxwCaL6UTA
- transcript/اسلاید/یادداشت: https://simonwillison.net/2023/May/2/prompt-injection-explained/
- گوینده: Simon Willison؛ ارائهٔ webinar LangChain، 12:16 برش YouTube از ارائهٔ یک‌ساعته.
- تاریخ: 2023-05-02 (یادداشت/متن)؛ ویدئو در کانال فردی منتشر شد.
- روش: صفحهٔ مقالهٔ خود سخنران را باز کردم؛ متن کامل همان 12 دقیقهٔ برش در چهار chunk (0–3)، همراه اسلایدهای ثابت، در دسترس بود. فراداده ویدئو از صفحهٔ YouTube خوانده شد.
- برداشت: تزریق به کاربردِ مدل/مرز اعتماد مربوط است و با «خواهش بیشتر در system prompt» حل نمی‌شود. وقتی مدل ابزار/ایمیل/اطلاعات خصوصی می‌بیند، خطر از تغییر پاسخ به اقدام، حذف یا exfiltration می‌رسد. سخنران dual-LLM/quarantine را به‌عنوان طرح احتمالی و پرهزینه مطرح می‌کند، نه درمان قطعی؛ نکتهٔ پایدار امروز: محتوای نامطمئن و مسیر ابزار را جدا کن و least privilege/approval به‌کار ببر.
- محدودیت/ارزیابی انتقادی: ارائه از 2023 است و بعضی حکم‌های مطلق/پیش‌بینی‌ها دیدگاه سخنران‌اند. گزارهٔ «امنیت احتمالاتی هیچ امنیتی نیست» را به‌عنوان استدلال او ثبت می‌کنم، نه عدد تجربی؛ در سامانهٔ ما دفاع prompt-only هم رد می‌شود، اما دفاع چندلایه طبق OWASP همچنان مفید است.

## 4) Akamai Developers — Prompt Engineering in Web Development | Using LangChain and Templates with OpenAI

- ویدئو: https://www.youtube.com/watch?v=pK6WzlTOlYw
- متن transcript: https://youtubetotranscript.com/transcript?v=pK6WzlTOlYw&current_language_code=en
- ناشر/گوینده: Akamai Developers؛ دموی توسعهٔ وب/Qwik و OpenAI API.
- تاریخ/مدت: 2023-09-11، 51:15 طبق فرادادهٔ صفحهٔ YouTube.
- روش: صفحهٔ YouTube و metadata/chapters را باز کردم؛ transcript انگلیسی را از سرویس مستقل YouTubeToTranscript.com در شش chunk (0–5) دریافت و کامل خواندم.
- برداشت: جدا کردن UI ورودی کمینه از قالب prompt سمت backend، iterative refinement و few-shot به‌صورت زنده؛ خروجی باید برای برنامه قابل‌خواندن باشد و promptهای تکراری بهتر است template باشند. اشتباهات خود demo (تلاش برای parse پاسخ آزاد با regex، خطای off-by-one) ارزشمند است: در نسخهٔ جدید از JSON Schema/structured outputs در صورت پشتیبانی و اعتبارسنجی مستقل استفاده شود، نه parse شکنندهٔ متن آزاد.
- محدودیت: ویدئوی 2023، نمونهٔ آموزشی/مورد بازی‌گونه؛ کارایی LangChain یا روش prompt را مقایسهٔ علمی نمی‌کند. API/library ممکن است تغییر کرده باشد؛ هیچ کد/متن از transcript به محصول کپی نشده است.

## جمع‌بندی چهارتایی

- مهارت‌های پایدار و مشترک: task روشن، context و متغیرها، مثال، خروجی قراردادی، رگرسیون و اصلاح بر اساس خطا.
- دو ویدئو قدیمی بیشترین خطرِ اطلاعات منسوخ دارند (تنظیمات GPT-3، API و LangChain) و برای الگوی معماری/اشتباه‌ها استفاده شدند، نه دستور deployment.
- ویدئوهای Anthropic و Simon مسئلهٔ trust boundary را نشان می‌دهند؛ تنها Simon مستقیماً تزریق را موضوع می‌گیرد. هیچ‌یک نشان نمی‌دهد یک system prompt به‌تنهایی حفاظت کامل ایجاد می‌کند.
- دادهٔ ویدئو در وزن‌دهی شواهد از مقالهٔ داوری‌شده/NIST/OWASP/مستندات جاری پایین‌تر است؛ فقط تجربهٔ ارائه/مثال عملی را مکمل می‌کند.
