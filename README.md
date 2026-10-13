# نمط استقبالك للمعلومة · قعدة صراحة

استبيان تفاعلي بيكشف من وين بتدخل المعلومة لراسك أسرع: **بصري، سمعي، ولا حسّي**.
من مشروع «قعدة» · إعداد م. إياد حلوبي · [@eyad.hloubi](https://www.instagram.com/eyad.hloubi/)

## شو بالحزمة

| الملف | شو هو |
|---|---|
| `index.html` | الاستبيان كامل بملف واحد |
| `favicon.svg` | أيقونة الموقع بالمتصفح |
| `og.png` | صورة المعاينة لما ينبعت الرابط (واتساب، إنستغرام، فيسبوك) |
| `render.yaml` | إعدادات النشر على Render كموقع ثابت |
| `.gitignore` | ملفات ما لازم تنرفع |

ما في أي بناء أو مكتبات لازم تتنزل. الموقع ثابت ومجاني على Render.

## الرفع على GitHub

1. افتح github.com واعمل **New repository**، سمّيه مثلاً `qa3da-info-style`، وخليه Public.
2. اكبس **uploading an existing file**.
3. فك ضغط الحزمة، واسحب **كل الملفات اللي جوّا المجلد** (مو المجلد نفسه)، مع `render.yaml` و`.gitignore`.
   - إذا ما بين `.gitignore` لأنه ملف مخفي، عادي، مو ضروري.
4. اكبس **Commit changes**.

## النشر على Render

1. ادخل على dashboard.render.com وسجّل دخول بحساب GitHub.
2. اكبس **New +** ثم **Blueprint**.
3. اختار الريبو `qa3da-info-style`، وRender بيقرا `render.yaml` لحاله.
4. اكبس **Apply**. بعد دقيقة تقريباً بيطلعلك رابط متل:
   `https://qa3da-info-style.onrender.com`

> **بديل يدوي:** New + ثم **Static Site**، اختار الريبو، خلّي Build Command فاضي أو `echo ok`، وPublish Directory = `.`

## خطوة أخيرة مهمة: صورة المعاينة

واتساب وفيسبوك بدهن رابط كامل لصورة المعاينة. بعد ما ياخد الموقع رابطه:

1. افتح `index.html` على GitHub واكبس ✏️ (Edit).
2. دوّر على السطر:
   ```html
   <meta property="og:image" content="og.png">
   ```
3. بدّله بالرابط الكامل:
   ```html
   <meta property="og:image" content="https://qa3da-info-style.onrender.com/og.png">
   ```
4. Commit، وRender بيعيد النشر لحاله خلال دقيقة.

## التعديل لاحقاً

أي تعديل بتعمله على `index.html` بـ GitHub، Render بينشره تلقائياً. ما في داعي تعمل شي تاني.

## ملاحظات

- الصورة والاسم اللي بيحطهن الشخص ما بيطلعوا من جهازه، وما في شي بينحفظ أو بينبعت.
- الخطوط من Google Fonts، فلازم يكون في إنترنت (طبيعي لموقع منشور).
- خطة Render المجانية للمواقع الثابتة ما بتنام، فالموقع بيفتح فوراً دايماً.
