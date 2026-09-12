# SILO — وضعیت فعلی (آخرین به‌روزرسانی: طبق آخرین گفتگو با Claude)

## چی رسماً تموم و تأییدشده‌ست
- **P0** — کامل، حذف کامل دیوار فعال‌سازی از هسته
- **P1** — کامل و «Final Approved»
- **P2** — کامل، PR اصلی Merge شده روی `main`
- **Issue #2 (Security Hardening / Migration 0026)** — PR باز شد، Review شد، تأیید و Merge شد
- **Issue #4 (باگ Onboarding)** — PR شماره ۵ (`fix/onboarding-restore-race`) تأیید و Merge شد (۲۰۲۶-۰۹-۱۲)

## چی الان در جریانه
هیچی — همه‌ی کارهای واگذارشده تا این لحظه تموم و Merge شدن. هیچ Issue بازی روی Repository نیست. منتظر Issue/Brief بعدی از طرف استادیم.

## Workflow فعلی پروژه (خیلی مهم — دقیقاً همینو رعایت کن)
1. استاد یه GitHub Issue می‌سازه با جزئیات دقیق کار، و اون رو به `tehrun47-ai` Assign می‌کنه
2. Claude از آخرین `main`، یه Branch جدا و اختصاصی برای همون Issue می‌سازه
3. Claude **فقط** همون کاری که توی Issue خواسته شده رو انجام می‌ده — نه بیشتر، نه فیچر اضافه، نه شروع فاز بعدی
4. تست کامل (رگرسیون SQL + تست‌های TypeScript) اجرا می‌شه
5. Build و Type-check چک می‌شه
6. Commit، Push روی همون Branch، و باز کردن Pull Request به `main`
7. Claude **همون‌جا متوقف می‌شه** — هیچ‌وقت خودش Merge نمی‌کنه، هیچ‌وقت وارد فاز/کار بعدی نمی‌شه بدون دستور جدید

## چی لازم نیست دیگه (طبق دستور صریح استاد)
- من (مصطفی) دیگه لازم نیست پیام‌های Claude رو Copy-Paste کنم و به استاد بدم — همه‌چیز مستقیم روی GitHub اتفاق می‌افته و استاد خودش می‌بینه
- Claude هیچ‌وقت نیازی به دسترسی Vercel یا Supabase نداره و نباید داشته باشه — Deploy و QA کاملاً دست خودِ استاده

## دسترسی‌های فنی
- Repository اصلی (مال استاد): `github.com/sina-ebrahimi-l/silo-trading-journal-app` — Private
- من (`tehrun47-ai`) به‌عنوان Collaborator اضافه شدم
- برای هر بار کار، یه Personal Access Token جدید (یا همون قبلی اگه هنوز معتبره) لازمه — از `github.com/settings/tokens` (نوع Classic، با دسترسی `repo` + `workflow`)
- **نکته‌ی مهم:** توکن رو زود پاک نکن! چون این پروژه چند دور کار داره، بهتره یه توکن با Expiration بلندتر (۳۰ روز) بسازی و تا آخر پروژه نگه‌ش داری، نه اینکه بعد از هر کار پاکش کنی.

## اگه می‌خوای یه AI جدید (Claude تازه، یا ChatGPT) این پروژه رو ادامه بده
فایل `HANDOFF-PROMPT.md` رو بهش بده.
