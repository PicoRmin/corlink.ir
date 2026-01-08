## برنامه روزانه فاز ۲: طراحی و تجربه کاربری (از شروع طراحی تا آماده‌شدن برای توسعه)

این برنامه بر اساس سند `Phase2-Design-UX.md` و `ROADMAP.md` برای حدود **۱۰ هفته کاری** طراحی شده تا خروجی‌های زیر را با کیفیت بالا تحویل دهد:

- User Stories کامل و تأییدشده  
- Sitemap و User Flows نهایی  
- Wireframeها و Mockupهای High-fidelity  
- Design System کامل و مستند  
- Prototype قابل کلیک + گزارش Usability Testing  

الگوی کلی:

- **شنبه تا چهارشنبه**: کار طراحی، تحقیق UX و هم‌ترازی با Product/Dev  
- **پنج‌شنبه**: ریویو، Sync با تیم فنی، به‌روزرسانی مستندات  
- **جمعه**: جمع‌بندی مدیریتی، تصمیم‌گیری روی نسخه‌های Design و آماده‌سازی هفته بعد  

نقش‌های اصلی:

- **UX Designer / UX Researcher**  
- **UI Designer / Visual Designer**  
- **Product Manager**  
- **نماینده فنی (Tech Lead یا Dev)** برای بررسی امکان‌پذیری  

---

## هفته ۱ – هم‌ترازی روی Scope UX و User Stories

### شنبه
- **Product + UX**
  - مرور کامل سند `Phase1-Research-Strategy` (Personas, Journeys, MVP, KPIs)  
  - مرور کامل `Phase2-Design-UX.md` (User Stories, Sitemap, Flows, Design System)  
  - ساخت **Design Brief** مختصر شامل:
    - اهداف UX در MVP  
    - کاربران اصلی و سناریوهای کلیدی  
    - محدودیت‌ها (BuddyBoss/WordPress، بودجه، زمان)  

### یکشنبه
- **UX Designer**
  - شکستن User Stories به **Epicهای UX** (Onboarding, Profile, Matching, Messaging, Search, Dashboard)  
  - مپ کردن User Stories به Flows کلان (از سند Phase2) برای هر Epic  
- **Product**
  - تأیید Priority User Stories برای MVP (چه چیزهایی حتماً در موج اول طراحی شوند)

### دوشنبه
- **UX Research**
  - تبدیل Customer Journeyهای فاز ۱ به سناریوهای تست UX (Tasks اصلی کاربران)  
  - تعریف سناریوهای Usability Testing (اولیه) بر اساس بخش «Usability Testing Scenarios» در Phase2  

### سه‌شنبه
- **تیم UX + Product**
  - کار روی **Information Architecture**:
    - مرور Sitemap پیشنهادی  
    - اصلاح/ادغام صفحات غیرضروری (کاهش پیچیدگی MVP)  
  - نهایی‌سازی ساختار Navigation سطح ۱ و ۲

### چهارشنبه
- **جلسه مشترک UX + Dev**
  - مرور Sitemap و User Flows  
  - بررسی محدودیت‌های BuddyBoss و Theme در Navigation, Profile, Messaging  
  - ثبت Items «نیاز به Custom Plugin/Theme» برای فاز ۳ و ۴  

### پنج‌شنبه – ریویو و مستندسازی
- به‌روزرسانی `Phase2-Design-UX.md` در بخش:
  - User Stories (اگر نیاز به اصلاح نام/Acceptance Criteria هست)  
  - Sitemap (پس از حذف/ادغام صفحات)  
- تولید یک **خلاصه هفتگی Design** برای مدیریت و Dev:
  - چه چیزهایی نهایی شد؟  
  - چه تصمیم‌هایی گرفته شد؟  

### جمعه – مدیریت و هم‌ترازی
- Product + UX Lead:
  - تأیید Epicهای UX برای دو هفته بعد (Wireframes Core Flows)  
  - اولویت‌بندی صفحات: Home, Onboarding, Dashboard, Suggestions, Profile, Messaging, Search  

---

## هفته ۲ – Wireframeهای Low-fidelity برای Flows اصلی

### شنبه
- **UX Designer**
  - طراحی Wireframe Low-fidelity برای:
    - صفحه اصلی (Home)  
    - صفحه ثبت‌نام/ورود  
  - تمرکز روی Layout، Hierarchy، CTAها، نه روی رنگ و جزئیات بصری  

### یکشنبه
- **UX Designer**
  - Wireframe برای Flow ثبت‌نام + تأیید ایمیل + Onboarding step-by-step (مطابق Flow 1 در Phase2)  
  - اضافه کردن یادداشت‌های UX روی Wireframeها (Annotations)  
- **Product**
  - Review و کامنت روی Wireframeها (Business Constraints, Messaging)

### دوشنبه
- **UX Designer**
  - Wireframe برای Dashboard کاربر (Overview + Widgets: پیشنهادات، پیام‌ها، درخواست‌ها، آمار)  
  - Wireframe برای صفحه Suggestions (لیست پیشنهادات، Match Score, Filters Sidebar)  

### سه‌شنبه
- **UX Designer**
  - Wireframe برای صفحه Profile (خود کاربر + دیگران)  
  - Wireframe برای Messaging (لیست مکالمات + صفحه چت)  
  - Wireframe برای Search & Filters  

### چهارشنبه
- **جلسه Design Review (UX + Product + Dev)**
  - مرور همه Wireframeها (Core Flows)  
  - بررسی:
    - آیا Flowها با User Stories و MVP Scope منطبق‌اند؟  
    - آیا چیزی اضافه/غیرضروری برای MVP وجود دارد؟  
    - آیا از نظر فنی در WordPress/BuddyBoss قابل پیاده‌سازی است؟  
  - ساخت لیست تغییرات (Change List) برای هفته بعد  

### پنج‌شنبه – ریویو و نسخه ۰٫۹ Wireframes
- به‌روزرسانی Wireframeها طبق Feedback  
- خروجی:  
  - یک فایل Figma/Balsamiq با همه Wireframeهای Low-fi  
  - مستندسازی در `Phase2-Design-UX.md` بخش Wireframes (لینک‌ها + توضیح صفحات)

### جمعه – مدیریت
- Product + UX Lead:
  - تأیید Wireframeهای نسخه ۰٫۹ به‌عنوان مبنای ورود به **Mid-fi/Hi-fi Mockups**  
  - به‌روزرسانی Backlog UX برای هفته ۳ (Component Design, Design System v1)  

---

## هفته ۳ – پایه‌گذاری Design System و Components

### شنبه
- **UI Designer**
  - تعریف و فاینال‌سازی **Color Palette** بر اساس بخش Color Palette در سند Phase2  
  - تست Contrast (WCAG 2.1 AA) برای رنگ‌های متن/پس‌زمینه/Primary  
- **UX**
  - اطمینان از هم‌راست‌سازی رنگ‌ها با Use-caseها (Success, Error, Warning, Info)

### یکشنبه
- **UI Designer**
  - تعریف کامل Typography Scale (H1–H6, Body, Caption, Button) مطابق جدول Typography  
  - تنظیم Styleهای متنی در Figma (Text Styles)  

### دوشنبه
- **UI/UX**
  - طراحی و مستندسازی Components پایه:
    - Buttons (Primary, Secondary, Ghost, Icon)  
    - Inputs, Textareas, Select, Checkbox, Radio  
    - Cards (Default, Elevated, Outlined)  
  - ثبت States (Default, Hover, Active, Disabled, Error, Success)

### سه‌شنبه
- **UI Designer**
  - طراحی Components ثانویه:
    - Badges, Tags  
    - Avatars  
    - Progress Bar, Tooltips  
    - Modals, Toasts  
- **Dev Representative**
  - بررسی امکان پیاده‌سازی Components در Tailwind/React (Phase3/4)  

### چهارشنبه
- **Design System Review**
  - جلسه ۹۰ دقیقه‌ای: مرور Design System (Colors, Typography, Components, Spacing, Shadows, Radius, Animations)  
  - تصمیم روی نسخه ۰٫۹ Design System  

### پنج‌شنبه – مستندسازی Design System
- به‌روزرسانی بخش **Design System** در `Phase2-Design-UX.md` مطابق خروجی Figma  
- ساخت یک صفحه Style Guide (در Figma یا مستند PDF) برای Devها  

### جمعه – مدیریت
- Product + UX + Tech Lead:
  - تأیید Design System v1 برای استفاده در Mockups  
  - ثبت هر محدودیت فنی/زمانی (مثلاً حذف بعضی Animations در MVP برای سادگی)  

---

## هفته ۴ و ۵ – Mockups High-fidelity برای Flows MVP

### شنبه (هفته ۴)
- **UI Designer**
  - تبدیل Wireframe صفحه اصلی به Mockup High-fi با استفاده از Design System  
  - دقت روی:
    - Hero, Value Prop, CTAها، Social Proof  
    - Responsive behavior Desktop/Mobile (نسخه اولیه)

### یکشنبه
- **UI Designer**
  - Mockup صفحه Auth (ورود، ثبت‌نام، بازیابی رمز)  
  - توجه به Error States، Helper Text، Validation States (مطابق بخش Input States)  

### دوشنبه
- **UI/UX**
  - Mockup Flow Onboarding کامل (مراحل متوالی)  
  - نمایش Progress, Tips, نمونه متن مناسب در جای درست  

### سه‌شنبه
- **UI Designer**
  - Mockup Dashboard:  
    - Cards خلاصه (پیشنهادات جدید، پیام‌ها، درخواست‌ها)  
    - لیست پیشنهادات در Dashboard یا لینک به صفحه Suggestions  

### چهارشنبه
- **Design Review هفتگی (UI + UX + Product + Dev)**
  - مرور Mockups هفته ۴، ثبت Feedback و Change Requests  

### پنج‌شنبه – تکمیل اصلاحات
- اصلاح Mockupهای هفته ۴ طبق Feedback  
- آپدیت لینک‌ها و اسامی صفحات در `Phase2-Design-UX.md` (بخش Wireframes و Mockups)

### جمعه – مدیریت
- تأیید نهایی Mockups صفحات: Home, Auth, Onboarding, Dashboard  
- آماده‌سازی لیست صفحات هفته ۵:
  - Suggestions, Profile, Messaging, Search

---

### شنبه (هفته ۵)
- **UI Designer**
  - Mockup صفحه Suggestions (لیست پیشنهادات، Match Score Badge, Filters)  
  - طراحی Visual برای Match Score (Progress Bar/Badge)

### یکشنبه
- **UI/UX**
  - Mockup صفحه Profile (خود + دیگران):
    - Header، Avatar بزرگ، Role, Location  
    - Sections: About, Skills, Goals, Links, Match Score (برای دیگران)  

### دوشنبه
- **UI Designer**
  - Mockup Messaging:
    - Layout دو ستونه (لیست مکالمات + چت) Desktop  
    - نسخه Mobile (لیست و چت جداگانه)  

### سه‌شنبه
- **UI Designer**
  - Mockup Search & Filters & Results:
    - Search bar, Filters Sidebar, Results Cards  
    - Pagination / Infinite Scroll (تصمیم مشترک با Dev)  

### چهارشنبه
- **Design Review**
  - مرور همه Mockups High-fi برای Core MVP Flows  
  - بررسی:
    - هم‌راستایی با User Stories  
    - سادگی UX و قابل‌پیاده‌سازی بودن در زمان MVP  

### پنج‌شنبه – مستندسازی و نسخه ۱٫۰ Mockups
- نهایی‌سازی Mockups و ساخت:
  - Figma Prototype اولیه (بدون تعاملات پیچیده)  
  - Export اسکرین‌ها برای مستندات داخلی/ارائه  
- به‌روزرسانی `Phase2-Design-UX.md` با:
  - لیست صفحات Mockup شده  
  - لینک Prototype

### جمعه – مدیریت
- تأیید Mockups نسخه ۱٫۰ برای تحویل به تیم توسعه (Phase3/4)  
- ثبت هر Feature/Animation که به بعد از MVP موکول می‌شود (Design Parking Lot)  

---

## هفته ۶ – ساخت Prototype تعاملی

### شنبه
- **UX/UI**
  - لینک‌کردن صفحات در Figma/Adobe XD برای ساخت Prototype کامل جریان:
    - ثبت‌نام → Onboarding → Dashboard → Suggestions → Profile → Messaging → Search  

### یکشنبه
- اضافه‌کردن Micro-interactions مهم:
  - Hover states روی Cards و Buttons  
  - Modal باز/بسته شدن (برای Actions مهم مثل ارسال درخواست همکاری)  

### دوشنبه
- تنظیم نسخه‌های Responsive (Desktop/Mobile) در Prototype برای سناریوهای اصلی  

### سه‌شنبه
- **Internal UX Review**
  - تست دستی Prototype توسط UX/PM/Dev  
  - ثبت باگ‌های UX/Flow (Dead ends, Confusing steps, Missing states)

### چهارشنبه
- اعمال اصلاحات روی Prototype  

### پنج‌شنبه – مستندسازی Prototype
- به‌روزرسانی بخش Prototype Specifications در `Phase2-Design-UX.md` با:
  - دامنه تعاملات  
  - سناریوهای قابل تست  
  - لینک نسخه‌های Desktop/Mobile  

### جمعه – برنامه‌ریزی Usability Testing
- نهایی‌سازی سناریوهای تست (از بخش Usability Testing Scenarios)  
- آماده‌کردن Script و فرم ثبت مشاهدات  

---

## هفته ۷ – Usability Testing با کاربران واقعی

### شنبه
- انتخاب ۵–۷ کاربر تست (بر اساس Personas: علی، سارا، محمد و …)  
- زمان‌بندی Sessionها (Online/حضوری)

### یکشنبه
- اجرای ۲–۳ تست اول (Senario 1 و 2: ثبت‌نام/پروفایل و پیدا کردن هم‌بنیان‌گذار)  
- ثبت ویدیو/اسکرین و Noteها

### دوشنبه
- اجرای ۲–۳ تست بعدی (Scenario 3 و 4: جستجو و پیام‌رسانی)  
- ثبت مشکلات UX و نقاط قوت

### سه‌شنبه
- تحلیل نتایج:
  - دسته‌بندی مشکلات به: Critical / Major / Minor / Nice-to-have  
  - استخراج Metrics: زمان تکمیل Task، نرخ موفقیت، خطاها، رضایت ذهنی  

### چهارشنبه
- جلسه جمع‌بندی نتایج تست:
  - تصمیم روی این‌که کدام مشکلات قبل از توسعه MVP باید حتماً حل شوند  
  - ثبت Improvementهای لازم در Backlog UX  

### پنج‌شنبه – به‌روزرسانی Design
- اعمال اصلاحات روی Mockups و Prototype طبق نتایج تست  
- به‌روزرسانی بخش «Usability Test Report» در `Phase2-Design-UX.md`

### جمعه – هم‌ترازی با Dev و Product
- جلسه Hand-off آماده‌سازی برای ورود به Phase3/Phase4:
  - مرور همه Flows و Screens  
  - پاسخ به سوالات فنی/بیزینسی  

---

## هفته ۸ تا ۱۰ – تثبیت Design System، آماده‌سازی Assetها و پشتیبانی توسعه

### شنبه تا چهارشنبه (الگوی ثابت هر هفته)
- **UX/UI**
  - تمیز کردن فایل Figma:
    - استفاده از Components و Variants  
    - نام‌گذاری استاندارد لایه‌ها و Frames (برای Dev)  
  - آماده‌سازی Design Tokens (رنگ‌ها، Spacing، Typography) مطابق بخش Design Tokens در Phase2  
  - Export Iconها، تصاویر و Styleها برای تیم فنی  
- **همکاری با Dev**
  - پاسخ روزانه به سوالات Implementation  
  - در صورت نیاز طراحی States/Empty/Error که در حین توسعه مشخص می‌شود  

### پنج‌شنبه – ریویو هفتگی UX/Dev
- مرور پیشرفت توسعه در مقابل Design  
- ثبت جاهای Discrepancy (جایی که توسعه با دیزاین تفاوت دارد)  
- تصمیم‌گیری: تغییر دیزاین یا تغییر توسعه؟ (به‌صورت موردی)

### جمعه – مدیریت
- بررسی این‌که:
  - آیا Design برای تمام Flows MVP «کامل و منجمد» (Design Freeze) هست؟  
  - آیا چیزی در Design باقی مانده که Blocker برای توسعه باشد؟  
  - اگر بله، تعیین Plan سریع برای بستن آن در هفته بعد  

---

## الگوی ثابت هفتگی در فاز ۲

- **شنبه**: Deep Work طراحی/تحقیق (Wireframe, Mockup, Flows, System)  
- **یکشنبه**: تکمیل کارهای طراحی + هماهنگی با Product  
- **دوشنبه**: Design System / Components / Tokens  
- **سه‌شنبه**: Prototype / Testing / Align با Dev  
- **چهارشنبه**: Design Review چندجانبه (UX + UI + Product + Dev)  
- **پنج‌شنبه**: مستندسازی (`Phase2-Design-UX.md`، Style Guide، Hand-off Notes)  
- **جمعه**: تصمیم‌گیری مدیریتی، Design Freezeهای مرحله‌ای، برنامه هفته بعد  

این برنامه کمک می‌کند تا **قبل از شروع توسعه سنگین فاز ۴، کل UX/UI MVP کاملاً مشخص، تست‌شده و مستند** باشد و تیم فنی بدون ابهام وارد پیاده‌سازی شود.


