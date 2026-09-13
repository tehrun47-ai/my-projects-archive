# پرامپت آماده برای شروع با یه AI جدید — SILO Analyst Platform

اگه می‌خوای Claude (یا هر AI دیگه‌ای) رو در جریان کامل این پروژه‌ی دوم بذاری، این متن رو کپی کن و اول از همه بهش بده:

---

من (مصطفی) یه پروژه‌ی دوم و کاملاً جدا از پروژه‌ی قبلی (SILO Trading Journal) برای همون استاد (سینا ابراهیمی) دارم — اسمش **SILO Analyst Platform / VIP Community**. این پروژه یه پلتفرم ردیابی و امتیازدهی تحلیل‌گرها روی Telegramه.

فایل‌های این پروژه رو (توی همین آرشیو، پوشه‌ی `silo-analyst-platform/`) به همین ترتیب بخون:
- `PROJECT_CONTEXT.md` — این پروژه چیه، Stack فنی‌ش چیه، چرا از پروژه‌ی قبلی جداست
- `CURRENT-STATUS.md` — دقیقاً الان کجاییم، چی تموم شده، چی گیر کرده

**نکات حیاتی:**
1. Repository اصلی: `github.com/sina-ebrahimi-l/silo-analyst-platform` — Private، من (`tehrun47-ai`) بهش دسترسی دارم
2. قبل از هر تغییری، حتماً این فایل‌ها رو مستقیم از خودِ Repository (نه از حافظه یا فرض) بخون، دقیقاً به این ترتیب: `DEV_AGENT.md`، `PROJECT_STATUS.md`، `CONTRIBUTOR_CHECKLIST.md`، `docs/REPOSITORY_ISOLATION.md`، `docs/ARCHITECTURE.md`، `docs/DATA_MODEL.md`، `docs/ROADMAP.md`، `docs/VIP_COMMUNITY_PROTOCOL_V1.md`، `docs/MUSTAFA_IMPLEMENTATION_BRIEF.md`
3. **هیچ‌وقت** به Protocol قدیمی («v0») برنگرد
4. **هیچ‌وقت** `supabase/migrations/0001_core.sql` رو Rewrite نکن
5. **هیچ‌وقت** این Repository رو به کد یا زیرساخت پروژه‌ی دیگه‌ای وابسته نکن
6. مستقیم روی `main` کار نکن؛ Branch جدا بساز
7. خودت PR رو Merge نکن — Review و Merge دست استاده
8. برای دسترسی، یه GitHub Personal Access Token لازمه (Classic، با دسترسی `repo` + `workflow`) — من می‌سازم و بهت می‌دم

**وضعیت فعلی خیلی مهمه:** یه Branch به اسم `feat/protocol-v1-pipeline` از قبل ساخته و Push شده، با کد کامل (Migration + موتور Protocol + ۴۰ تست Pass‌شده)، ولی هنوز به‌خاطر یه خطای سمت گیت‌هاب (HTTP 500) موفق به باز کردن Pull Request نشدیم. اول این‌رو چک کن: شاید همون Branch رو بشه دستی یا از طریق API به PR تبدیل کرد بدون نیاز به کار جدید.
