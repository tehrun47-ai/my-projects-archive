# Sina Website — Home Visual Refinement — وضعیت فعلی

## چی تا الان انجام شده
- ✅ بریف کامل از استاد دریافت شد (Issue #3، Repository `sina-ebrahimi-website`)
- ✅ همه‌ی ۱۰ فایل مستندات اجباری کامل خونده شد: README.md, AGENTS.md, CONTRIBUTING.md, docs/AGENT_HANDOFF.md, docs/PAGE_ASSIGNMENTS.md, docs/BRANCH_POLICY.md, docs/HOME.md, docs/DESIGN_SYSTEM.md, docs/ASSET_MANIFEST.md, docs/DECISIONS.md
- ✅ کد فعلی Home بررسی شد: `apps/web/app/page.tsx` + هر ۴ کامپوننت زیر `apps/web/components/home/**` (EcosystemMap, AboutSocialProof, LatestRail, VerticalTestimonials)
- ✅ تأیید شد سطح دسترسی من روی Repository `write` هست (نه صرفاً دعوت‌شده‌ی معلق)
- ✅ Branch جدا ساخته و Push شد: `feat/home-visual-refinement` (از `feat/platform-foundation`, commit `96432f6`)
- ✅ خلاصه‌ی شروع‌کار (برداشت، فایل‌های مجاز، یه ابهام واقعی) داخل Issue #3 ثبت شد

## نتیجه‌ی بررسی وضعیت فعلی کد نسبت به Spec
- `latestItems` و `testimonials` هر دو خالی هستن — درست و مطابق قانون «بدون داده‌ی جعلی»
- Stats Bar اصلاً توی کد وجود نداره — درست، طبق `docs/HOME.md` که میگه Stats bar حذف شده
- شکاف اصلی بصری: `EcosystemMap.tsx` فعلاً یه لیست افقی تقسیم‌شده‌ست (divide-y)، نه Grid کارتی مثل موکاپ مرجع — باید بازسازی بصری بشه، ولی با حفظ ساختار ۴‌شاخه‌ای مصوب `docs/HOME.md` (نه ۶ کارت موکاپ)

## ابهام ثبت‌شده در Issue #3 (منتظر پاسخ استاد)
کامپوننت `AboutSocialProof.tsx` یه Badge ثابت داره: «۱۰+ سال تجربه بازار». طبق `docs/HOME.md`، ادعای «سال‌های تجربه»ی تأییدنشده جزو محتوای ممنوعه‌ست. پرسیده شده این خط از قبل کپی مصوب صفحه‌ی About هست یا باید حذف/کلی‌تر بشه — تا پاسخ نیومده دست‌نخورده می‌مونه.

## قدم بعدی
شروع پیاده‌سازی بصری (بازسازی EcosystemMap به Grid کارتی + پالیش Responsive Hero/About/Final CTA طبق `docs/DESIGN_SYSTEM.md`)، بعد Validation کامل (`lint/typecheck/test/build`)، بعد باز کردن PR به `feat/platform-foundation` با گزارش کامل طبق فرمت خواسته‌شده در بریف.
