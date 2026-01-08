## برنامه روزانه فاز ۳: فنی و معماری (Technical Architecture)

هدف فاز ۳ بر اساس `Phase3-Technical-Architecture.md`:

- نهایی‌کردن Stack و معماری سیستم (Monolithic MVP آماده برای Migration)  
- طراحی دیتابیس، جداول Custom و Indexها  
- تعریف APIها، امنیت، Performance Strategy، DevOps/Infrastructure و استراتژی تست  
- آماده‌سازی محیط توسعه و CI/CD برای شروع توسعه MVP در فاز ۴  

این فاز معمولاً حدود **۴–۶ هفته** در ابتدای کار فنی طول می‌کشد (بخشی هم‌پوشان با Sprint 0 و 1 در فاز ۴).

نقش‌های اصلی:

- **Tech Lead / Architect**  
- **WordPress / PHP Developer**  
- **DevOps Engineer (پاره‌وقت)**  
- **Frontend Lead (React)**  
- **Security/Performance Specialist (در صورت وجود یا نقش مشترک)**  

الگوی هفتگی:

- **شنبه تا چهارشنبه**: طراحی معماری، PoC فنی، نوشتن اسکریپت‌ها و تنظیمات  
- **پنج‌شنبه**: ریویو معماری/کد، مستندسازی در `Phase3-Technical-Architecture.md`  
- **جمعه**: تصمیم‌گیری مدیریتی/فنی، Freeze بخش‌های معماری و برنامه‌ریزی هفته بعد  

---

## هفته ۱ – Stack، افزونه‌ها و ساختار کلی معماری

### شنبه
- **Tech Lead**
  - مرور `Phase3-Technical-Architecture.md` و `Phase4-Development-Roadmap.md` برای هم‌ترازی با MVP Features  
  - نهایی‌کردن انتخاب Stack (WordPress + BuddyBoss + PHP 8.2 + MySQL 8 + Redis + Nginx + Cloudflare + React/Vite/Tailwind)  
- **DevOps**
  - آماده‌سازی محیط توسعه محلی (Docker Compose اولیه مطابق مثال در سند Phase3)  

### یکشنبه
- **WordPress Developer**
  - نصب محلی WordPress، BuddyBoss، افزونه‌های ضروری (ACF, WooCommerce, Members, WP Mail SMTP, Wordfence, Redis Cache)  
  - تست اولیه کارکرد BuddyBoss و لاگین/ثبت‌نام پایه  
- **Tech Lead**
  - مرور محدودیت‌ها/امکانات BuddyBoss و ثبت آن‌ها در بخشی به‌نام *Technical Constraints*  

### دوشنبه
- **Tech Lead + Dev**
  - مرور جدول «افزونه‌های WordPress ضروری» و تأیید نسخه‌ها/نیازمندی‌ها  
  - ساخت فایل‌های پیکربندی پایه (wp-config، Redis config، Cloudflare plan assumptions)  

### سه‌شنبه
- **معماری High-Level**
  - ترسیم و بازبینی Diagram معماری High-level (Client → CDN → Nginx → WordPress/BuddyBoss/Corlink Plugin → DB/Redis → External Services)  
  - تصمیم روی:
    - نحوه استفاده از React (Embedded در صفحات خاص یا SPA بخش‌محور)  
    - مرز بین PHP Templates و React Components  

### چهارشنبه
- **جلسه Architecture Review (Tech + Product)**
  - تأیید Monolithic Modular Architecture برای MVP  
  - ثبت Migration Path به Microservices برای آینده (بدون پیچیده‌کردن MVP)  

### پنج‌شنبه – مستندسازی
- به‌روزرسانی `Phase3-Technical-Architecture.md` بخش:
  - انتخاب Stack (با نسخه‌ها و دلایل نهایی)  
  - Architecture Diagrams (با توضیحات)  

### جمعه – تصمیم‌گیری
- تأیید Stack نهایی و معماری کلی  
- تصمیم روی:
  - چه چیزهایی حتماً در این فاز پیاده‌سازی شود (DevOps, DB, API Design, Security Baseline)  
  - چه چیزهایی می‌تواند به موازات توسعه جلو برود (مثلاً Load Testing پیشرفته)  

---

## هفته ۲ – طراحی دیتابیس و جداول Custom

### شنبه
- **DB/Backend Dev**
  - مرور کامل بخش ERD و جداول Custom (`corlink_user_profiles`, `corlink_user_skills`, …)  
  - هم‌ترازی با نیازهای UX/Business (از فاز ۱ و ۲)  

### یکشنبه
- **DB Design**
  - بازطراحی/تأیید schema جداول بر اساس:
    - کارایی برای Search/Matching  
    - سادگی برای گزارش‌گیری اولیه  
  - مرور انواع داده‌ها (ENUM, VARCHAR, JSON, TIMESTAMP) و تنظیم Defaults  

### دوشنبه
- **اسکریپت‌های Migration**
  - نوشتن SQLهای ایجاد جداول (همان که در Phase3 آمده) در قالب:
    - اسکریپت مستقل DB Migration  
    - یا کلاس Activation در Plugin `corlink-core`  

### سه‌شنبه
- **ایجاد PoC داده**
  - Seedکردن تعدادی User/Profiles/Skills/Goals تستی  
  - اجرای Queryهای نمونه:
    - جستجوی کاربر بر اساس مهارت/نقش/مکان  
    - استخراج Match Scores  

### چهارشنبه
- **Optimization اولیه**
  - بررسی Indexها (`EXPLAIN` روی Queryهای اصلی Search/Matching)  
  - تنظیم Indexهای ترکیبی (location + role_type + availability, user_id + skill_name,…)  

### پنج‌شنبه – مستندسازی دیتابیس
- به‌روزرسانی بخش‌های:
  - ERD کامل  
  - Data Types و Constraints  
  - Migration Scripts  
در `Phase3-Technical-Architecture.md`

### جمعه – تأیید معماری داده
- Tech Lead:
  - تأیید Schema نسخه ۱٫۰ برای MVP  
  - ثبت موارد «برای بعد» (مثلاً Sharding/Partitioning، Read Replica)  

---

## هفته ۳ – طراحی API، امنیت پایه و معماری Plugin

### شنبه
- **Backend Dev + Tech Lead**
  - مرور بخش API Design (Endpoints برای Auth, Profile, Matching, Search, Messaging, Subscription, Notifications)  
  - Mapping این Endpoints به User Stories و فازهای توسعه در `Phase4-Development-Roadmap`  

### یکشنبه
- **طراحی Plugin `corlink-core`**
  - ایجاد اسکلت Plugin:
    - `corlink-core.php`  
    - `includes/class-corlink-core.php`  
    - `includes/class-matching-algorithm.php`  
    - `includes/class-profile-extensions.php`  
    - `includes/class-api-endpoints.php`  
  - ثبت نام‌گذاری استاندارد کلاس‌ها و فضاهای نام (Namespace) در مستند  

### دوشنبه
- **API Skeleton**
  - پیاده‌سازی ساده (بدون منطق پیچیده) برای:
    - `/profile` GET/PUT  
    - `/matching/suggestions` GET (برگرداندن داده Mock)  
  - استفاده از WordPress REST API (`register_rest_route`) و ساخت ساختار پاسخ استاندارد (`success/data/message/errors/meta`)  

### سه‌شنبه
- **امنیت پایه API**
  - پیاده‌سازی Middleware/Callbackهای Authorization:
    - چک توکن JWT یا Session WordPress  
    - محدود کردن endpointها براساس نقش (Role)  
  - تنظیم Rate Limiting در Nginx/Cloudflare برای مسیرهای حساس (Auth, Matching, Search)

### چهارشنبه
- **جلسه API Review (Tech + Dev + Frontend Lead)**
  - مرور قراردادهای API:  
    - Endpoint, Method, Payload, Response, Error Codes  
  - ثبت JSON Schemas برای پاسخ‌های کلیدی (Profile, Suggestions, Messages)  

### پنج‌شنبه – مستندسازی API
- تکمیل بخش‌های:
  - REST API Endpoints  
  - API Response Format  
  - Authentication & Authorization  
  - Rate Limiting & Versioning  
در `Phase3-Technical-Architecture.md`

### جمعه – مدیریت و Align با Frontend
- جلسه مشترک با Frontend Lead:
  - تأیید قراردادهای API برای استفاده در فاز ۴  
  - ثبت هر نیاز اضافی (Pagination, Sorting, Filtering, Error Codes)  

---

## هفته ۴ – امنیت، Performance و DevOps/Infrastructure

### شنبه
- **Security Focus**
  - مرور بخش Security در Phase3  
  - تنظیم سیاست‌های Password، TLS، PII Protection، Data Retention (در سطح طراحی)  
  - تعریف Security Headers (X-Content-Type-Options, CSP, HSTS, …) در Nginx Template  

### یکشنبه
- **Input Validation & Sanitization**
  - پیاده‌سازی Helperهای مشترک در Plugin برای:
    - Email/URL Validation  
    - Text Sanitization (`sanitize_text_field`, `wp_kses`,…)  
  - اطمینان از استفاده از `$wpdb->prepare()` در Queryهای Custom  

### دوشنبه
- **Performance & Caching**
  - طراحی استراتژی Caching چندلایه (Browser, CDN, Page Cache, Object Cache, OPcache)  
  - تنظیمات اولیه Redis Object Cache + WP Super Cache در محیط Staging  
  - تعریف کلیدهای Cache برای: Match Scores, Profile Summaries, Suggestions  

### سه‌شنبه
- **DevOps Setup**
  - تنظیم GitHub Actions (یا ابزار مشابه) برای:
    - Run Tests (PHPUnit, Jest)  
    - Build Frontend (Vite)  
    - Package Deployment Artifact  
  - تنظیم اسکریپت‌های ساده Deployment به Staging (SFTP/SSH/rsync)  

### چهارشنبه
- **Infrastructure Planning**
  - نهایی‌کردن نیازمندی‌های سرور Production/Staging:
    - CPU/RAM/Storage/Network  
  - طراحی Backup Strategy (DB/Files/Config) و زمان‌بندی آن  

### پنج‌شنبه – مستندسازی کامل فنی
- به‌روزرسانی بخش‌های:
  - Security (Auth, Data Security, XSS/SQLi Prevention, File Upload Security, API Security)  
  - Performance & Optimization (DB, Frontend, Server, KPIs)  
  - DevOps & Infrastructure (Docker Compose, CI/CD, Deployment, Backup, Monitoring)  

### جمعه – تأیید Architecture برای ورود به توسعه MVP
- Tech Lead:
  - چک این‌که تمام بلوک‌های زیر حداقل در نسخه ۰٫۹ آماده هستند:
    - DB Schema  
    - Core Plugin Structure  
    - API Contract  
    - Security Baseline  
    - Dev Environment & CI/CD Skeleton  
  - اگر نقص مهمی وجود دارد، تعریف Mini-Sprint ۱ هفته‌ای برای تکمیل آن

---

## هفته ۵–۶ (در صورت نیاز) – PoCها، تست Load اولیه و Harden کردن Before Dev

### شنبه تا چهارشنبه
- **PoCهای هدفمند (در صورت ریسک):**
  - PoC Matching Performance روی دیتای فرضی  
  - PoC Search Performance با Indexها و Full-text  
  - PoC Messaging Load (در حد ساده) با BuddyBoss  
- **Performance Testing پایه**
  - اجرای تست سبک با K6 یا ابزار مشابه روی endpointهای Matching/Search/Profile  
  - چک این‌که اهداف اولیه Response Time (در سند Phase3) منطقی و دست‌یافتنی است  

### پنج‌شنبه – به‌روزرسانی مستندات بر اساس PoC
- ثبت نتایج PoC، تغییرات پیشنهادی در معماری/تنظیمات  
- به‌روزرسانی بخش «Performance Testing» و «Load Testing» در Phase3  

### جمعه – Freeze معماری فاز ۳
- تصمیم رسمی:
  - Architecture v1 برای MVP «منجمد» است و تنها Fix/Adjustment کوچک در حین توسعه مجاز است  
  - هر تغییر بزرگ معماری باید از کانال Change Management (پس از MVP) عبور کند  

---

## الگوی ثابت کاری فاز ۳ (هفته‌ای)

- **شنبه**: طراحی/بازبینی معماری (DB, API, Security, Infra)  
- **یکشنبه**: پیاده‌سازی اسکریپت‌ها و PoCهای فنی  
- **دوشنبه**: تنظیمات Performance/Caching/Validation  
- **سه‌شنبه**: DevOps & CI/CD & Environment Setup  
- **چهارشنبه**: Architecture/Code Review چندجانبه (Tech + Dev + DevOps + در صورت نیاز Product)  
- **پنج‌شنبه**: مستندسازی در `Phase3-Technical-Architecture.md`, ERD, API Docs, Runbooks  
- **جمعه**: تصمیم‌گیری روی Freeze بخش‌ها، تعریف ریسک‌ها و اولویت‌های هفته بعد  

خروجی این فاز باید وضعیتی باشد که تیم توسعه (فاز ۴) بتواند **بدون ابهام، روی معماری پایدار و محیط آماده**، توسعه MVP را شروع کند.


