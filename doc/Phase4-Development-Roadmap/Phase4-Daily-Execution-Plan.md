## برنامه روزانه فاز ۴: توسعه (Development Roadmap) تا لانچ MVP

این فایل بر اساس `Phase4-Development-Roadmap.md` و `ROADMAP.md`، یک برنامه **روزبه‌روز (الگوی هفتگی)** از شروع توسعه تا **لانچ MVP** ارائه می‌دهد.

- طبق فازبندی توسعه: Sprint 0 تا Sprint 10 (مجموعاً حدود **۲۱ هفته (~۵ ماه)** تا آماده شدن برای Launch/Beta و آماده‌سازی لانچ عمومی)  
- در عمل:  
  - **Sprint 0** = آماده‌سازی فنی (بخشاً هم‌پوشان با فاز ۳)  
  - **Sprint 1–9** = توسعه MVP  
  - **Sprint 10** = Beta Test و رفع باگ و آماده‌سازی Launch  

الگوی هفته:

- **شنبه تا چهارشنبه**: توسعه، تست، Code Review، هم‌ترازی روزانه  
- **پنج‌شنبه**: مرور Sprint, Demo داخلی، به‌روزرسانی مستندات و Backlog  
- **جمعه**: بررسی مدیریتی/محصولی، تنظیم Sprint بعدی (در کنار جلسه رسمی Sprint Planning ابتدای Sprint)  

نقش‌ها:

- **Developers (WordPress/PHP, Frontend React, Full-stack)**  
- **QA Engineer**  
- **Product Manager / Owner**  
- **Tech Lead / Architect**  
- **DevOps (پاره‌وقت)**  

در ادامه، برای هر Sprint، الگوی روزانه و تمرکزها را مشخص می‌کنیم.

---

## Sprint 0 (۱ هفته) – آماده‌سازی محیط و زیرساخت

### شنبه
- **DevOps / WP Dev**
  - راه‌اندازی محیط توسعه محلی (Docker/LocalWP) براساس تنظیمات Phase3  
  - نصب WordPress، BuddyBoss، افزونه‌های ضروری، تنظیم اولیه دیتابیس  
- **Tech Lead**
  - چک‌لیست نصب و Setup را مستند می‌کند (Installation Guide داخلی)

### یکشنبه
- **DevOps**
  - راه‌اندازی محیط Staging (روی هاست/سرور تست)  
  - تنظیم دسترسی‌ها، SSL اولیه (در صورت امکان)، اتصال به Git  
- **Developers**
  - کلون کردن Repo، تست Build Frontend (اگر پروژه React جداست)، تست دسترسی به APIها  

### دوشنبه
- **Developers**
  - ساخت ساختار پوشه‌ها (Theme/Child Theme، Plugin `corlink-core`, Frontend src) مطابق Phase3  
  - راه‌اندازی Linting/Formatting (PHP CS Fixer, ESLint, Prettier) در پروژه  

### سه‌شنبه
- **Tech Lead + Developers**
  - تست ابتدایی Performance (TTFB, Basic Page Load) روی محیط Staging  
  - فعال‌کردن Redis Object Cache و Page Cache  

### چهارشنبه
- **Product + Tech Lead**
  - اطمینان از آماده بودن محیط برای Sprint 1  
  - مرور Backlog Sprint 1 (Auth &基础 زیرساخت) و تقسیم تسک‌های اولیه  

### پنج‌شنبه – ریویو و مستندسازی
- مستندسازی:
  - Setup Guide (Dev, Staging)  
  - Known Issues (اگر هست)  
- آپدیت `Phase4-Development-Roadmap.md`، بخش Sprint 0 با وضعیت واقعی تسک‌ها  

### جمعه – مدیریت
- تأیید اتمام Sprint 0 (طبق اهداف سند)  
- Finalize لیست User Stories و Tasks برای Sprint 1  

---

## الگوی روزانه عمومی برای Sprintهای ۲ هفته‌ای (Sprint 1 تا 10)

برای جلوگیری از تکرار، یک الگوی روزانه ثابت برای هر Sprint تعریف می‌کنیم و سپس برای هر Sprint تمرکز و Featureهای آن را مشخص می‌کنیم.

### شنبه (Day 1 Sprint)
- **صبح – Sprint Planning (تیم کامل)**
  - مرور هدف Sprint (Sprint Goal)  
  - انتخاب User Stories مطابق `Phase4-Development-Roadmap`  
  - شکستن هر Story به Tasks ۰٫۵–۲ روزه  
  - تخمین نهایی (Story Points/Hours) و چک Capacity تیم  
- **بعدازظهر – آماده‌سازی فنی**
  - Developers: ایجاد Branchهای اصلی Sprint، تنظیم Feature Flags (در صورت نیاز)  
  - DevOps: اطمینان از سلامت Staging برای تست‌های Sprint  

### یکشنبه
- **Developers**
  - کار روی Tasks با Priority 1 (Backend + Frontend)  
  - شروع پیاده‌سازی ساختارهای اصلی (بدون UI نهایی در صورت نیاز)  
- **QA**
  - آماده‌سازی Test Cases برای Stories اصلی Sprint  
- **Daily Standup (۱۵ دقیقه)**

### دوشنبه
- **توسعه ادامه**
  - تمرکز روی تکمیل Backend/Database بخش Stories  
  - شروع پیاده‌سازی UI (در صورت آماده‌بودن طرح‌ها از فاز ۲)  
- **Code Review**
  - Merge منظم به Branch Sprint (نه مستقیماً main) با PR و Review  

### سه‌شنبه
- **Integration Day**
  - اتصال Frontend به APIهای Backend  
  - رفع مشکلات Integration (Auth, Data shape, Error handling)  
- **QA**
  - تست‌های اولیه روی Staging/Dev برای Stories تقریباً آماده  

### چهارشنبه
- **Stabilization Day**
  - Fix باگ‌های کشف‌شده  
  - Refactorهای کوچک برای خوانایی/Performance  
  - به‌روزرسانی مستندات فنی (READMEهای ماژول‌ها، توضیح Endpointها)  

### پنج‌شنبه (اواسط Sprint)
- **Mini Review داخلی**
  - Demo داخلی Features نیمه‌کامل/کامل تیم به Product/UX  
  - تصمیم روی Scope Adjust (افزودن/حذف جزئیات کوچک برای رسیدن به هدف Sprint)  
- **مستندسازی**
  - به‌روزرسانی `Phase4-Development-Roadmap.md` برای وضعیت Stories  

### جمعه
- **Product + Tech Lead**
  - مرور پیشرفت نسبت به Sprint Goal  
  - شناسایی ریسک‌ها (تاخیر، پیچیدگی فنی، Blockers)  
  - تنظیم Focus هفته دوم Sprint (روی تکمیل/پولیش و نه شروع Feature جدید زیاد)  

### شنبه (Day 8 Sprint)
- تمرکز روی تکمیل همه Stories باز با Priority بالا  
- Block داستان‌های جدید بزرگ؛ فقط کوچک‌ترین Stories مجازند اگر ظرفیت هست  

### یکشنبه
- **QA Full Pass**
  - تست کامل جریان‌های مرتبط با Sprint  
  - ثبت باگ‌ها در Tracker (Bug/Task)  

### دوشنبه
- **Bug Fixing Day 1**
  - تمرکز Develop روی رفع باگ‌های Critical/High  
  - Merge سریع پس از Code Review سبک (Hotfix flow داخلی)  

### سه‌شنبه
- **Bug Fixing Day 2 + Performance Tweaks**
  - باگ‌های Medium/Low  
  - تنظیم اولیه Performance (Caching, Query Optimization) مرتبط با Stories  

### چهارشنبه (End of Sprint)
- **Sprint Review**
  - Demo Features به Product/Stakeholders  
  - بررسی این‌که کدام Stories به‌طور کامل Done شده‌اند (طبق Definition of Done)  
- **Sprint Retrospective**
  - Start / Stop / Continue  
  - Action Items برای Sprint بعد  

### پنج‌شنبه/جمعه (فاصله بین Sprintها – در عمل با شروع Sprint بعد هم‌پوشان)
- جمع‌بندی مستندات، به‌روزرسانی Backlog، پاک‌سازی Branchها  
- آماده‌سازی برای Sprint بعدی (هماهنگ با فاز ۵ – Go-to-Market در صورت نزدیک‌شدن به Launch)  

---

## تمرکز هر Sprint (۱ تا ۱۰) + نکات کلیدی روزانه

در این بخش، برای هر Sprint، مهم‌ترین محورهای کاری (بر اساس Phase4) را همراه با تأکیدهای روزانه ذکر می‌کنیم.

### Sprint 1 – زیرساخت و احراز هویت

**Stories کلیدی:**  
US-001 ثبت‌نام، US-002 ورود، US-003 بازیابی رمز، امنیت پایه فرم‌ها

- **شنبه (Planning):**  
  - انتخاب Stories Auth + تنظیم کارهای DevOps مرتبط (Rate limiting, CSRF, Email Verification)  
- **یکشنبه–دوشنبه:**  
  - پیاده‌سازی فرم‌های ثبت‌نام/ورود/فراموشی رمز در BuddyBoss/Theme + Endpointهای مرتبط  
  - اتصال به Email Service (SendGrid/Mailgun) و تست ایمیل تایید  
- **سه‌شنبه–چهارشنبه:**  
  - تست End-to-End زیرفرآیند: ثبت‌نام → تایید ایمیل → ورود → فراموشی رمز  
  - اضافه‌کردن Validation و پیام‌های خطای کاربرپسند  
- **پنج‌شنبه–جمعه:**  
  - مرور امنیت Auth (Brute-force protection, Lockout پس از چند تلاش، HTTPS)  
  - به‌روزرسانی مستندات Auth در Phase3/Phase4  

### Sprint 2 – پروفایل کاربری – بخش اول (اطلاعات پایه)

**Stories:**  
US-002 تکمیل پروفایل، US-003 مهارت‌ها (بخش اول)، آپلود عکس

- **شنبه (Planning):**  
  - تقسیم Tasks: ساخت جداولProfile, Skills، Formهای ویرایش، نمایش پروفایل  
- **یکشنبه–سه‌شنبه:**  
  - پیاده‌سازی فرم پروفایل (نام، شهر، نقش، بیوگرافی) با ACF و افزونه، UI مطابق فاز ۲  
  - سیستم مهارت‌های اولیه (افزودن تا ۱۰ Skill، سطح مهارت)  
  - آپلود عکس پروفایل و نمایش در UI  
- **چهارشنبه:**  
  - تست کامل Flow تکمیل پروفایل از نگاه کاربر جدید  
- **پنج‌شنبه–جمعه:**  
  - مرور با UX: آیا فرم طولانی است؟ نیاز به Onboarding Stepper؟  
  - اصلاحات کوچک برای افزایش نرخ تکمیل پروفایل  

### Sprint 3 – پروفایل کاربری – بخش دوم (رزومه، حریم خصوصی، لینک‌ها)

**Stories:**  
US-004 رزومه، US-005 حریم خصوصی، لینک‌های اجتماعی

- **شنبه–سه‌شنبه:**  
  - پیاده‌سازی آپلود رزومه (PDF، ۵MB)، ذخیره امن، نمایش/دانلود محدود (مثلاً فقط Premium)  
  - تنظیمات حریم خصوصی (Public/Private/Connections Only) + تنظیم روی فیلدها  
  - افزودن LinkedIn/GitHub/Portfolio با Validation URL  
- **چهارشنبه–پنج‌شنبه:**  
  - تست‌های حریم خصوصی:  
    - کاربر مهمان چه می‌بیند؟  
    - کاربر لاگین چه می‌بیند؟  
    - فقط Connection چه می‌بیند؟  
- **جمعه:**  
  - مرور معیارهای «Profile Completion Rate» و تنظیم Analytics برای آن  

### Sprint 4 – سیستم تطبیق – الگوریتم

**Stories:**  
US-006 پیشنهادات، US-007 امتیاز تطبیق، ساخت جدول Match_Scores و Cron

- **شنبه (Planning):**  
  - تعریف دقیق فرمول امتیازدهی (وزن مهارت/هدف/نقش/مکان) در سطح کد و مستند  
- **یکشنبه–سه‌شنبه:**  
  - پیاده‌سازی کلاس `Matching_Algorithm` در Plugin  
  - نوشتن توابع محاسبه Skill Match, Goal Match, Role Match, Location Match و Total Score  
  - ایجاد Cron Job برای محاسبه دوره‌ای Matchها  
- **چهارشنبه:**  
  - تست الگوریتم با داده‌های Seed‌شده، ساخت چند سناریوی تست مشخص (Matchهای بالا/پایین)  
- **پنج‌شنبه–جمعه:**  
  - Refactor برای Performance (آماده‌سازی Indexها و Caching روی Match_Scores)  
  - مستندسازی فرمول‌ها در Phase3/Phase4 (برای شفافیت کاربران/تیم)  

### Sprint 5 – نمایش پیشنهادات و جستجو (UI + فیلترها)

**Stories:**  
US-008 فیلترها، US-009 دلایل تطبیق، US-014 جستجو  

- **شنبه–دوشنبه:**  
  - پیاده‌سازی صفحه Suggestions (React یا Template) با کارت‌های پیشنهاد + Match Score + دلایل تطبیق  
  - پیاده‌سازی فیلترها (مهارت، موقعیت، تجربه) و اتصال به API Search/Matching  
- **سه‌شنبه–چهارشنبه:**  
  - صفحه Search مستقل با Search bar + Filters + نتایج  
  - Pagination/Infinite Scroll ساده  
- **پنج‌شنبه–جمعه:**  
  - تست کاربری داخلی برای جریان: Dashboard → Suggestions → Profile → Send Request/Message  

### Sprint 6 – پیام‌رسانی (Messaging)

**Stories:**  
US-010 ارسال پیام، US-012 اعلان‌ها (در حد MVP)

- **شنبه–دوشنبه:**  
  - پیکربندی و اطمینان از کارکرد BuddyBoss Messaging  
  - ساخت/سفارشی‌سازی UI صفحه چت (لیست مکالمات + چت) مطابق Design System  
- **سه‌شنبه–چهارشنبه:**  
  - پیاده‌سازی اعلان‌های ابتدایی (In-app + Email) برای پیام جدید  
- **پنج‌شنبه–جمعه:**  
  - تست جریان: مشاهده پروفایل → ارسال پیام → پاسخ → نمایش وضعیت پیام (خوانده شده/نشده به‌صورت ساده)  

### Sprint 7 – درخواست همکاری (Connection Requests)

**Stories:**  
US-011 ارسال درخواست همکاری، US-013 مدیریت درخواست‌ها

- **شنبه–سه‌شنبه:**  
  - استفاده از سیستم Connection BuddyBoss برای ارسال/پذیرفتن درخواست همکاری  
  - UI برای لیست درخواست‌های ارسالی/دریافتی، دکمه Accept/Reject، پیام همراه  
- **چهارشنبه:**  
  - تست کامل جریان: Suggestions → Profile → Send Request → Notify → Accept/Reject → تبدیل به Connection  
- **پنج‌شنبه–جمعه:**  
  - تنظیم Analytics برای Tracking درخواست‌ها، نرخ قبول، زمان پاسخ  

### Sprint 8 – داشبورد و صفحه اصلی

**Stories:**  
Dashboard Overview, Widgets, Landing Page

- **شنبه–دوشنبه:**  
  - پیاده‌سازی Dashboard طبق Mockups:  
    - کارت خلاصه پیشنهادها، پیام‌ها، درخواست‌ها  
    - ویجت وضعیت تکمیل پروفایل  
- **سه‌شنبه–چهارشنبه:**  
  - پیاده‌سازی Landing Page (Home) با Hero، Features، Stats، CTAها، Testimonials (نسخه MVP)  
- **پنج‌شنبه–جمعه:**  
  - تست UX داخلی: آیا کاربر تازه‌وارد می‌فهمد چه کاری باید انجام دهد؟  

### Sprint 9 – بهینه‌سازی و پولیش

**Stories:**  
Performance, Security, SEO, Cross-browser, Responsive

- **شنبه–سه‌شنبه:**  
  - بهینه‌سازی سرعت (Caching, Minification, Lazy loading images، Tailwind Purge)  
  - رفع Warningها/باگ‌های Performance در Lighthouse/PageSpeed  
- **چهارشنبه:**  
  - Security Audit اولیه:  
    - فرم‌ها، Uploadها، ریدایرکت‌ها، Permissionها  
- **پنج‌شنبه–جمعه:**  
  - تست Cross-browser و Responsive روی دستگاه‌های مختلف  
  - Fix UI/UX Issues که از تست‌ها بیرون می‌آید  

### Sprint 10 – تست Beta و آماده‌سازی Launch

**Stories/Tasks:**  
دعوت کاربران Beta، جمع‌آوری بازخورد، Fix باگ‌ها، تست Load ابتدایی، آماده‌سازی Launch

- **شنبه–دوشنبه:**  
  - دعوت ۲۰–۵۰ کاربر Beta (مطابق فاز ۵ – Go-to-Market)  
  - مانیتور استفاده، جمع‌آوری باگ‌ها و Feedbackها  
- **سه‌شنبه–چهارشنبه:**  
  - Fix باگ‌های Critical/High که برای MVP غیرقابل‌قبول هستند  
  - تست Load ساده روی مسیرهای Matching/Search/Auth  
- **پنج‌شنبه–جمعه:**  
  - آماده‌سازی Launch Checklist (هم‌تراز با `Phase5-Legal-Growth`):  
    - Terms/Privacy/Cookie/Help/FAQ  
    - Monitoring/Backup/Support readiness  

---

## نقش پنج‌شنبه و جمعه در کل فاز ۴

- **پنج‌شنبه‌ها:**
  - ریویو فنی و محصولی Sprint جاری  
  - Demo داخلی، Sync با UX/Legal/Marketing در صورت نزدیک‌شدن به Launch  
  - به‌روزرسانی مستندات (`Phase4-Development-Roadmap`, API Docs, READMEها)  

- **جمعه‌ها:**
  - جلسه سبک مدیریتی (Founders + Product + Tech Lead):  
    - آیا در مسیر هستیم؟ (Velocity, Burn-down, Risks)  
    - آیا Scope نیاز به Adjust دارد؟  
    - آماده‌سازی واضح برای شروع هفته بعد (Saturday–Wednesday tasks)  

با این ساختار، از **روز ۰ توسعه (Sprint 0)** تا **روز لانچ MVP (پایان Sprint 10 و اجرای Launch Plan)**، تیم‌ها هر روز می‌دانند:

- چه چیزی باید ساخته/تست/مستند شود  
- چه زمانی تصمیم‌گیری و Alignment مدیریتی انجام می‌شود  
- چگونه خروجی‌ها با مستندات فازهای ۱–۳ و فاز ۵ منطبق می‌ماند.  


