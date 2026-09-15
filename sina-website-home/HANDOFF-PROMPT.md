# پرامپت آماده برای شروع با یه AI جدید — Sina Website / Home Visual Refinement

اگه می‌خوای Claude (یا هر AI دیگه‌ای) رو در جریان کامل این پروژه‌ی سوم بذاری، این متن رو کپی کن و اول از همه بهش بده:

---

من (مصطفی) یه پروژه‌ی سوم و کاملاً جدا از دو پروژه‌ی قبلی (SILO Trading Journal و SILO Analyst Platform) برای همون استاد (سینا ابراهیمی) دارم — بازطراحی بصری صفحه‌ی Home روی سایت خودش (`sina-ebrahimi-website`)، نه یه پروژه‌ی معاملاتی.

فایل‌های این پروژه رو (توی همین آرشیو، پوشه‌ی `sina-website-home/`) به همین ترتیب بخون:
- `PROJECT_CONTEXT.md` — این پروژه چیه، Repository کجاست، چرا از دو پروژه‌ی قبلی جداست، Stack فنی
- `CURRENT-STATUS.md` — دقیقاً الان کجاییم، چی تموم شده، چی باقی مونده

**نکات حیاتی:**
1. Repository اصلی: `github.com/sina-ebrahimi-l/sina-ebrahimi-website` — Private، من (`tehrun47-ai`) دسترسی `write` دارم
2. Repository داره از Framer به Next.js مهاجرت می‌کنه؛ یه PR باز و merge-نشده به اسم **#1** داره. تا وقتی اون merge نشه، Branch پایه `feat/platform-foundation` هست، نه `main` — هر کار جدید از اونجا شروع و به همونجا PR می‌شه
3. قبل از هر تغییری، حتماً این فایل‌ها رو مستقیم از خودِ Repository بخون، دقیقاً به همین ترتیب: `README.md`, `AGENTS.md`, `CONTRIBUTING.md`, `docs/AGENT_HANDOFF.md`, `docs/PAGE_ASSIGNMENTS.md`, `docs/BRANCH_POLICY.md`, `docs/HOME.md`, `docs/DESIGN_SYSTEM.md`, `docs/ASSET_MANIFEST.md`, `docs/DECISIONS.md`
4. مأموریت من فقط Home (`/`) هست — Issue #3، Branch: `feat/home-visual-refinement`. محدوده: `apps/web/app/page.tsx` + `apps/web/components/home/**` + assetهای Home-local
5. **هیچ‌وقت** فایل‌های مشترک (`packages/ui`, globals.css, layout.tsx, Header/Footer/Nav, Tailwind config, lockfile) رو بدون هماهنگی صریح تغییر نده
6. **هیچ‌وقت** آمار/تعداد/تاریخ/Testimonial ساختگی اضافه نکن — اگه داده‌ی تأییدشده نیست، Section مخفی می‌مونه
7. تصویر Hero تأییدشده (`sina-home-hero-approved.png`) عوض/بازتولید نمی‌شه
8. مستقیم روی `main` یا `feat/platform-foundation` کار نکن؛ Branch جدا (`feat/home-visual-refinement`) بساز/استفاده کن
9. خودت PR رو Merge نکن — Review و Merge دست استاده
10. برای دسترسی، یه GitHub Personal Access Token لازمه (Classic، با دسترسی `repo`) — من می‌سازم و بهت می‌دم

**وضعیت فعلی خیلی مهمه:** Branch `feat/home-visual-refinement` از `feat/platform-foundation` ساخته و Push شده. خلاصه‌ی برداشت اولیه + یه ابهام واقعی (badge «۱۰+ سال تجربه» توی AboutSocialProof.tsx که ممکنه با قانون ضد-آمار-جعلی تداخل داشته باشه) داخل Issue #3 کامنت شده — قبل از ادامه چک کن استاد جوابی داده یا نه. پیاده‌سازی بصری اصلی (بازسازی EcosystemMap به Grid کارتی + Responsive Polish) هنوز شروع نشده.
