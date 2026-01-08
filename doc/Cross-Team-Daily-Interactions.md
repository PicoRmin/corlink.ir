## تعاملات روزانه بین تیم‌ها (از روز ۰ تا لانچ MVP)

این سند توضیح می‌دهد **چه تیمی در هر روز با چه تیم‌های دیگری، روی چه موضوعی و به چه شکل تعامل دارد** تا فازهای ۱ تا ۴ (و آماده‌سازی فاز ۵) بدون گپ و دوباره‌کاری جلو بروند.

تیم‌های اصلی:

- **تیم مدیریت / Founders / Product Owner (PO)**
- **تیم استراتژی و تحقیق بازار (Strategy/Research)**
- **تیم UX / UI (Design)**
- **تیم فنی و معماری (Architecture / Tech Lead)**
- **تیم توسعه (Development – Backend/Frontend/WordPress)**
- **تیم DevOps / Infrastructure**
- **تیم QA / تست**
- **تیم Legal & Growth/Marketing** (بیشتر در نزدیکی لانچ و فاز ۵)

الگوی کلی برای کل فازها:

- شنبه تا چهارشنبه: **تعاملات عملیاتی و روزمره** (طراحی، توسعه، تصمیم‌گیری‌های تاکتیکال)  
- پنج‌شنبه: **تعاملات ریویو و گزارش بین تیم‌ها**  
- جمعه: **تعاملات مدیریتی و تصمیم‌گیری کلان**  

در ادامه، برای هر روز هفته، تعاملات کلیدی را به‌صورت **ثابت (برای کل دوره)** و سپس نکات خاص برای فازها توضیح می‌دهیم.

---

## شنبه – هم‌ترازی هفتگی و Kickoff تسک‌ها

### ۱. جلسه هم‌ترازی هفتگی (Weekly Alignment)

- **شرکت‌کنندگان:**  
  - مدیریت/Founders  
  - Product Owner  
  - Tech Lead  
  - نماینده UX  
  - نماینده Research (در فازهای ۱ و ۲)  
  - نماینده Dev (اگر Sprint در حال اجراست)  

- **خروجی‌ها:**  
  - اهداف هفته برای هر تیم (Objectives هفتگی)  
  - لیست Featureها/Deliverableهای کلیدی هفته (مثلاً: تکمیل Wireframes پروفایل، نهایی‌کردن API پروفایل، تحویل صفحه Suggestions در Dev و …)  
  - لیست Blockerهای فعلی و مسئول رفع آن‌ها  

### ۲. تعاملات فاز به فاز در شنبه

- **فاز ۱ (تحقیق و استراتژی):**
  - Product + Research: مرور وضعیت تحلیل بازار/رقبا و تعیین اینکه این هفته روی کدام بخش کار می‌شود (SWOT، Personas، Market Size، Pricing).  
  - Research + UX: انتقال یافته‌های جدید بازار به UX برای استفاده در Personas و Flows.  

- **فاز ۲ (UX/Design):**
  - Product + UX: مرور User Stories مهم این هفته، اولویت صفحات (Home, Dashboard, Suggestions, Profile, ...)  
  - UX + Tech Lead: بررسی آیا طراحی پیشنهادی با محدودیت‌های فنی (BuddyBoss/WordPress) سازگار است یا باید از الان در نظر گرفته شود.  

- **فاز ۳ (معماری):**
  - Tech Lead + DevOps: تصمیم روی تسک‌های این هفته در زیرساخت (DB Schema، CI/CD، Caching، Security).  
  - Tech Lead + Dev: هماهنگی روی این‌که چه بخش‌هایی از معماری باید قبل از شروع Storyهای خاص آماده باشد.  

- **فاز ۴ (توسعه – وقتی Sprint در جریان است):**
  - Product + Dev + QA + UX: **Sprint Planning / Re-planning هفتگی** (اگر هفته اول Sprint است، همان Sprint Planning؛ اگر هفته دوم است، Micro-planning برای تکمیل Storyها).  

---

## یکشنبه – اجرای عمیق و هم‌ترازی تاکتیکال

### ۱. Daily Standup بین تیم‌های اجرایی

- **شرکت‌کنندگان:** Dev, QA, UX (در صورت وابستگی آن Sprint), Tech Lead, Product  
- **فرمت:**  
  - دیروز چه کردیم؟  
  - امروز روی چه کار می‌کنیم؟  
  - چه Blockerهایی داریم که نیاز به کمک دیگران (Product/UX/TechLead) دارد؟  

### 2. تعاملات خاص

- **Research ↔ Product (در فاز ۱):**
  - هماهنگی روی پرسشنامه‌ها، لیست رقبا، تعیین کاربران هدف برای مصاحبه این هفته.  

- **UX ↔ Product (در فاز ۲):**
  - بازبینی Wireframe/Mockupهایی که در روز قبل طراحی شده و تنظیم تغییرات لازم قبل از ساخت نسخه نهایی.  
  - Product پاسخ سوالات «این المان چه هدف بیزینسی دارد؟» را می‌دهد.  

- **UX ↔ Tech Lead / Dev (در فاز ۲ و ۴):**
  - اگر UI پیشنهادی شامل الگوی جدیدی است (مثلاً Card خاص یا Interaction پیچیده)، Dev و UX یک تماس/جلسه کوتاه ۳۰ دقیقه‌ای برای بررسی امکان‌پذیری فنی و هزینه توسعه برگزار می‌کنند.  

- **Dev ↔ Tech Lead (در فاز ۳ و ۴):**
  - هماهنگی روی ساخت ماژول‌ها/Pluginها (مثلاً `corlink-core`) و تقسیم کار: چه کسی روی Matching Algorithm کار می‌کند، چه کسی روی API، چه کسی روی Frontend.  

---

## دوشنبه – کنترل ریسک و هم‌ترازی بین UX/Tech/Research

### ۱. جلسه کوتاه Risk & Dependencies (اختیاری ولی توصیه‌شده، هفته‌ای ۱ بار دوشنبه)

- **شرکت‌کنندگان:** Product, Tech Lead, UX Lead، در صورت نیاز Research  
- **موضوعات:**  
  - آیا چیزی که Research این هفته درمی‌آورد، روی UX/Dev این Sprint تاثیر می‌گذارد؟  
  - آیا تغییری در MVP Scope لازم شده پیش از آن‌که Dev شروع/ادامه دهد؟  
  - آیا dependency خاصی (مثلاً تصمیم معماری، انتخاب Plugin، تصمیم قیمت‌گذاری) Blocker شده؟  

### ۲. تعاملات روزمره

- **Research ↔ UX (فاز ۱ و اوایل فاز ۲):**
  - انتقال سریع Insightهای جدید مصاحبه/تحقیقات به UX؛ مثلاً:
    - «کاربران می‌گویند فرم‌های طولانی را رها می‌کنند» → UX باید Flow Onboarding را سبک‌تر کند.  

- **UX ↔ Dev (زمانی که Design به Implementation می‌رسد):**
  - UX، لینک Figma + شرح رفتار را برای Dev می‌فرستد و در صورت ابهام، یک جلسه ۱۵–۳۰ دقیقه‌ای Clarification برگزار می‌شود.  

- **Tech Lead ↔ DevOps:**
  - هماهنگی روی تنظیمات Performance، Logging, Monitoring که Dev این هفته به آن نیاز دارد.  

---

## سه‌شنبه – هماهنگی عمقی بین فازها (Research, UX, Tech, Dev)

### ۱. Hand-off و Sync بین فازها

- **فاز ۱ → فاز ۲ (در اوایل پروژه):**
  - Research/Strategy + UX:  
    - مرور Personas, Customer Journeys, Value Prop و تبدیل آن به Flowهای قابل طراحی.  

- **فاز ۲ → فاز ۴:**
  - UX + Dev:  
    - تحویل Mockup/Prototype نهایی برای صفحات خاص (مثلاً Profile، Suggestions، Messaging)  
    - Dev سوالات پیاده‌سازی را مطرح می‌کند (Breakpointها، States، رفتار در Error/Empty)  

- **فاز ۳ → فاز ۴:**
  - Tech Lead + Dev:  
    - هماهنگی روی این‌که کدام Tableها، APIها، Caching Layerها برای Stories این Sprint آماده/کامل هستند.  

### ۲. هماهنگی بین Legal/Growth و Product (در نزدیک لانچ)

- **Product ↔ Legal/Growth (فاز ۵ در حال نزدیک شدن):**
  - Product نیازمندی‌های UX/Flow (Terms, Privacy, Cookie Consent, Pricing Page) را به تیم Legal/Growth منتقل می‌کند.  
  - Legal تایید می‌کند که MVP Flowها مطابق با Terms/Privacy Draftها هستند.  

---

## چهارشنبه – پیش‌مرور خروجی‌ها و آماده‌سازی گزارش

### ۱. پیش‌مرور (Pre-review) داخلی

- **Dev ↔ QA:**
  - QA نسخه‌های آماده/نزدیک آماده را بررسی می‌کند و لیست باگ‌ها را تهیه می‌کند.  
- **UX ↔ Dev:**
  - نمایش سریع پیاده‌سازی صفحات طراحی‌شده و مقایسه با Design (Visual QA)  

### ۲. آماده‌سازی برای پنج‌شنبه

- **Product ↔ همه تیم‌ها:**
  - جمع‌آوری نقاط کلیدی پیشرفت و چالش‌ها برای گزارش پنج‌شنبه:  
    - در Research چه چیزی کشف شد؟  
    - در UX چه صفحه‌هایی نهایی/Freeze شده‌اند؟  
    - در Tech/Dev چه Featureهایی Complete هستند؟  
    - در QA چه باگ‌های بحرانی هست؟  

---

## پنج‌شنبه – روز ریویو و گزارش بین‌تیمی

### ۱. گزارش تیم‌ها به Product/مدیریت

- **Research/Strategy → Product:**
  - خلاصه یک‌صفحه‌ای Findings مهم هفته (اگر هنوز در فاز ۱ هستیم).  

- **UX → Product + Dev:**
  - لیست صفحاتی که Design Freeze شده و برای Development آماده است.  
  - لیست موارد UX که پیاده‌سازی‌شان به بعد از MVP منتقل شده (Parking Lot).  

- **Tech/Architecture → Product/Dev/DevOps:**
  - تغییرات مهم معماری (DB, API, Caching, Security).  
  - ریسک‌های فنی شناسایی‌شده.  

- **Dev → Product + QA:**
  - Featureهایی که این هفته Merge شده و قابل Demo هستند.  

- **QA → همه:**
  - وضعیت تست‌ها، باگ‌های Critical/High باز، آمادگی برای Beta/Launch (در فازهای آخر).  

### ۲. جلسه Review هفتگی (حدود ۶۰–۹۰ دقیقه)

- **شرکت‌کنندگان:** همه لیدها (Product, Tech, UX, Dev, QA, DevOps, Research، در صورت نیاز Legal/Growth)  
- **ساختار:**  
  1. مرور اهداف هفته و آن‌چه تحقق یافته.  
  2. Demo Features/Flows اصلی هفته.  
  3. مرور KPIهای کوتاه‌مدت (Velocity, Story Points Done, کیفیت تحویل‌ها، وضعیت Performance/Errors در Staging).  
  4. تصمیم‌گیری‌های کوتاه‌مدت (مثلاً حذف/تعویق Featureهای کم‌اهمیت).  

### ۳. به‌روزرسانی مستندات مشترک

- **Product + Tech Lead + UX Lead:**  
  - آپدیت بخش‌های وضعیت در:
    - `ROADMAP.md` (Milestoneها)  
    - اسناد فازها (بخش «چک‌لیست اجرای فاز» و «معیارهای موفقیت»)  

---

## جمعه – تصمیم‌گیری کلان و برنامه‌ریزی هفته بعد

### ۱. جلسه مدیریتی (Founders + PM + Tech Lead)

- **موضوعات اصلی:**  
  - آیا پروژه در مسیر زمان‌بندی کلی تا لانچ MVP هست؟  
  - آیا ریسک بحرانی جدیدی ظاهر شده؟ (فنی، بازار، قانونی، منابع انسانی)  
  - آیا لازم است Scope MVP کم/زیاد شود؟  

### ۲. تعاملات با هر تیم (در حد خلاصه و تصمیم)

- **با Product/Research:**
  - تعیین این‌که آیا نیاز به تحقیقات بیشتر (مصاحبه، تست بازار) قبل از تصمیم بعدی هست یا نه.  

- **با UX:**
  - تعیین Design Freezeهای جدید: چه بخش‌هایی دیگر قابل تغییر نیستند مگر در صورت Bug/مشکل جدی.  

- **با Tech/Dev/DevOps:**
  - تأیید این‌که Architecture/Infrastructure فعلی، Bottleneck جدی برای هفته/اسپرینت بعد نیست.  

- **با QA:**
  - تعیین تمرکز تست هفته بعد (مثلاً: Regression روی Auth/Profiles، یا Scenarioهای Matching).  

### ۳. خروجی کلیدی جمعه

- لیست **تصمیم‌های کلان هفته** (Decision Log):  
  - تغییر در MVP Scope  
  - تغییر در ترتیب فازها یا Sprints  
  - تصمیم‌های معماری/زیرساختی مهم  
  - تصمیم‌های مارکتینگ/Legal مرتبط با Product  

این Decision Log باید در محل مشترکی (مثلاً یک بخش در `ROADMAP.md` یا سیستم مدیریت پروژه) ثبت شود تا در آینده علت تصمیم‌ها روشن باشد.

---

## نکات خاص تعامل بین تیم‌ها در هر فاز

### فاز ۱ – Research/Strategy محور

- تعامل سنگین **Research ↔ Product ↔ UX**  
- Tech در این فاز بیشتر نقش مشاور دارد (برای بررسی امکان‌پذیری ایده‌ها).  
- Legal/Marketing فقط در حد مشورت سطح بالا وارد می‌شوند.  

### فاز ۲ – UX/Design محور

- تعامل سنگین **UX ↔ Product ↔ Tech ↔ Dev**:  
  - Product: معنا و هدف بیزینسی هر صفحه/Flow  
  - Tech/Dev: محدودیت‌ها و امکان‌پذیری فنی  
- Research هنوز با UX در ارتباط است (آوردن Insightهای جدید)  

### فاز ۳ – Architecture محور

- تعامل سنگین **Tech Lead ↔ Dev ↔ DevOps ↔ Product**:  
  - Product فقط در حد «نیازهای بیزینسی» و «اولویت‌ها» ورودی می‌دهد.  
  - UX بیشتر نقش مشاهده و هماهنگی دارد که Design و Architecture هم‌راستا باشند (مثلاً APIهایی که UX نیاز دارد).  

### فاز ۴ – Development/QA محور

- تعامل شدید **Dev ↔ QA ↔ UX ↔ Product ↔ Tech Lead** تقریباً هر روز:  
  - Dev ↔ UX: اطمینان از پیاده‌سازی درست Design  
  - Dev ↔ QA: تست Featureها و رفع سریع باگ‌ها  
  - Product ↔ Dev/UX: تضمین این‌که خروجی واقعاً همان چیزی است که برای MVP لازم است، نه کمتر و نه بیشتر  
  - Tech Lead ↔ Dev/DevOps: کنترل کیفیت معماری، Performance، Security  

### نزدیک Launch / فاز ۵

- تعاملات **Product ↔ Legal ↔ Marketing ↔ Tech/Dev** شدیدتر می‌شود:  
  - اطمینان از هماهنگی Terms/Privacy/Flows  
  - هماهنگی پیام‌های مارکتینگ با واقعیات Product  
  - هماهنگی Launch Checklist (فنی + بیزینسی + حقوقی)  

---

## نتیجه

این سند به همراه برنامه‌های روزانه هر فاز:

- `Phase1-Daily-Execution-Plan.md`  
- `Phase2-Daily-Execution-Plan.md`  
- `Phase3-Daily-Execution-Plan.md`  
- `Phase4-Daily-Execution-Plan.md`  
- و `ROADMAP-Daily-Execution-Plan.md`  

نشان می‌دهد که **در هر روز، چه تعاملاتی بین کدام تیم‌ها لازم است** تا:

- تصمیم‌ها سریع و هماهنگ گرفته شوند  
- خروجی هر فاز بدون گپ به فاز بعد منتقل شود  
- تا روز لانچ MVP، هیچ تیمی «در خلأ» کار نکند و همه تصویر کلی و وابستگی‌ها را بدانند.  


