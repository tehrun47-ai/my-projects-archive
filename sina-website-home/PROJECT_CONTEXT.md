# Sina Website — Home Visual Refinement — Project Context

## این پروژه چیه؟
سومین پروژه‌ی جدا برای همون استاد (سینا ابراهیمی) — این بار نه Trading Journal، نه Analyst Platform، بلکه **بازطراحی بصری صفحه‌ی Home** روی سایت شخصی/تجاری خودش. سایت یه پلتفرم Code-first با Next.js/React/TypeScript هست که قراره پایه‌ی محتوا، آموزش، عضویت، کامیونیتی، تجارت و ابزارهای داخلی بشه — نه فقط یه سایت معرفی.

## این پروژه با دو پروژه‌ی قبلی فرق داره!
این یه Repository کاملاً جدا و مستقله. جزئیات دو پروژه‌ی قبلی توی `../silo-trading-journal/` و `../silo-analyst-platform/` هست — قاطی‌شون نکن.

## Repository اصلی (مال استاد)
`github.com/sina-ebrahimi-l/sina-ebrahimi-website` — Private

من (`tehrun47-ai`) به‌عنوان Collaborator با سطح دسترسی `write` باهاش دعوت شدم (دعوت پذیرفته/فعال شده).

## وضعیت مهاجرت Repository (نکته‌ی حیاتی)
این Repository داره از Framer به Next.js مهاجرت می‌کنه و یه **PR باز و merge-نشده به اسم #1** داره. تا وقتی اون PR merge نشه:
- Branch اصلی توسعه `feat/platform-foundation` هست، نه `main`
- `main` هنوز نسخه‌ی قدیمی/pre-migration رو نگه داشته (فقط مستندات Governance روش sync شده)
- هر Branch کاری باید از `feat/platform-foundation` بیاد و PR هم به همونجا برگرده، نه به `main`

## مأموریت من (Issue #3)
بردن صفحه‌ی Home از حالت Structural/Early Visual به یک صفحه‌ی کامل، حرفه‌ای، Responsive — فقط در حد طراحی/پیاده‌سازی بصری، نه بازطراحی معماری. محدوده‌ی مجاز فایل:
- `apps/web/app/page.tsx`
- `apps/web/components/home/**`
- assetهای Home-local

فایل‌های مشترک (`packages/ui`, globals.css, layout.tsx, Header/Footer, Tailwind config, و...) خارج از محدوده‌ی من هستن؛ هر تغییر اونجا نیاز به هماهنگی جدا داره.

## Stack فنی
- pnpm workspace / monorepo سبک
- Next.js App Router + React + TypeScript
- Tailwind CSS + Design System اختصاصی در `packages/ui`
- PostgreSQL کانونیک، Supabase به‌عنوان provider قابل‌تعویض
- Vercel برای Runtime، Cloudflare برای DNS/Worker/Queue/edge

برای این تسک به‌خصوص (Home) نیازی به Supabase، Cloudflare، Vercel Dashboard یا Production Secrets نیست.

## قوانین سخت‌گیرانه‌ی این پروژه
- هیچ‌وقت مستقیم روی `main` یا `feat/platform-foundation` کامیت نکن
- PR من همیشه به `feat/platform-foundation` می‌ره، نه `main`
- خودم PR رو Merge نمی‌کنم — فقط استاد
- هیچ آمار/تعداد/تاریخ/Testimonial ساختگی اضافه نکن (اعضا، دانش‌پذیران، ساعت آموزشی، سال تجربه، امتیاز ستاره‌ای، و...) — اگه داده‌ی تأییدشده نیست، اون Section مخفی می‌مونه
- تصویر Hero تأییدشده (`sina-home-hero-approved.png`) عوض/بازتولید نمی‌شه
- موکاپ مرجع (`docs/references/home/home-desktop-reference.png`) فقط راهنمای بصریه، نه چیزی که عیناً به‌عنوان تصویر داخل صفحه قرار بگیره یا کپی محتوایی‌ش دقیق دنبال بشه — متن و ساختار مصوب داخل `docs/HOME.md` (مثلاً ۴ شاخه‌ی اکوسیستم، نه ۶ کارت موکاپ) اولویت داره
