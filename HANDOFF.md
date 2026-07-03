# HANDOFF — كامن KAMEN™ Website

**التاريخ:** 2026-06-30  
**الحالة:** جاهز للمراجعة — لم يُرفع إلى GitHub بعد

---

## هيكل الملفات

```
/repo
├── index.html              ← الصفحة الرئيسية للموقع التسويقي
├── growth-map.html         ← خارطة كامن للنمو (تشخيص تفاعلي — 4 خطوات)
├── demo.html               ← صفحة بريدج للنموذج الحي (تشرح قبل الإرسال)
├── HANDOFF.md              ← هذا الملف
├── docs/
│   ├── DECISIONS_LOG.md
│   ├── BACKLOG.md
│   ├── PROJECT_CONTEXT.md
│   ├── MASTER_ROADMAP.md
│   └── BRAND_USAGE.md
└── project/                ← ملفات الأنيميشن (كامن موشن)
    ├── index.html          ← نسخة الأنيميشن العمودية 9:16
    ├── index-landscape.html← نسخة الأنيميشن الأفقية 16:9
    ├── kamen.jsx
    ├── animations.jsx
    ├── support.js
    ├── Kamen Motion.dc.html
    └── assets/
        ├── logo-full.png
        ├── logo-mark.png
        └── logo-text.png
```

---

## مسار الزائر المُنجز

```
index.html
  ↓ (ابدأ خارطة كامن للنمو)
growth-map.html
  ↓ (بعد إرسال الخارطة أو طلب التواصل)
واتساب ← فقط كخطوة أخيرة

index.html
  ↓ (شاهد نموذجًا حيًا)
demo.html
  ↓ (افتح النموذج الحي)
https://aseeaa0e-png.github.io/ardiyat-aldiyar/ (تبويب جديد)

demo.html أيضاً يحتوي:
  → ابدأ خارطة كامن للنمو → growth-map.html
  → تحدث مع كامن → واتساب
```

---

## رقم واتساب — يجب تحديثه قبل الرفع

**الرقم الحالي مؤقت:** `966500000000`

ابحث عن هذه النصوص في الملفات الثلاثة وعدّل الرقم:
```
https://wa.me/966500000000
```

الملفات التي تحتوي عليه:
- `index.html` (موضعان: nav mobile + CTA banner + footer)
- `growth-map.html` (في شاشة النتيجة)
- `demo.html` (في زر التواصل)

---

## فيديو كامن موشن — يُضاف لاحقاً

الفيديو **غير متوفر بعد** كملف MP4. الصفحة الرئيسية تعرض placeholder في القسم "كيف تعمل كامن؟".

لإضافة الفيديو:
1. صدّر `project/index.html` كـ MP4 (عبر Share → Export → Video أو تسجيل شاشة)
2. ضع الملف في: `assets/kamen-motion.mp4`
3. ضع صورة الـ poster (الإطار الأخير) في: `assets/kamen-motion-poster.png`
4. في `index.html`، اقرأ التعليق داخل `.video-frame` وأزل الـ `<!--` لتفعيل الـ `<video>` tag وأحذف `div.video-placeholder`

---

## نموذج التقييم — يحتاج backend

`growth-map.html` يعرض نموذجاً تفاعلياً بـ 4 خطوات.
عند الإرسال، يعرض شاشة نجاح فقط — **لا يُرسل البيانات حالياً**.

خيارات الربط:
- [Formspree](https://formspree.io) — أسهل خيار، لا يحتاج backend
- Google Forms + iframe
- Airtable + API
- أي backend مخصص

---

## Dropdown في الهيدر

الـ Dropdown مُنجز بـ CSS `:hover` للـ desktop — يعمل بدون JavaScript.
على الجوال: القائمة المتنقلة تعرض نفس الخيارات كقائمة مسطحة بدون dropdown.

**ملاحظة للمرحلة التالية:** يمكن تحسين الـ dropdown بـ JavaScript لدعم click-based بدل hover-based (أفضل للـ accessibility).

---

## الأصول

| الملف | المسار | الحالة |
|-------|--------|--------|
| الشعار الكامل | `project/assets/logo-full.png` | ✓ موجود |
| رمز الشعار | `project/assets/logo-mark.png` | ✓ موجود |
| نص الشعار | `project/assets/logo-text.png` | ✓ موجود |
| فيديو موشن | `assets/kamen-motion.mp4` | ✗ يُضاف لاحقاً |
| صورة الفيديو | `assets/kamen-motion-poster.png` | ✗ يُضاف لاحقاً |

---

## قرارات تصميمية مهمة

1. **لا أسعار مغلقة** — جميع الأسعار بصيغة "تبدأ من" مع توضيح أن السعر النهائي بعد الخارطة
2. **لا إرسال مباشر لواتساب** من أزرار التقييم — كل أزرار التشخيص تذهب لـ `growth-map.html`
3. **كامن ليست محصورة في الأرضيات** — ذُكر صراحةً في `demo.html` مرتين وفي `index.html`
4. **لا إنجليزية** — KAMEN™ كعنصر هوية فقط، بقية الموقع عربي بالكامل
5. **منهجية نهائية** — نضج ونتائج (لا نضج ونمو)، مواءمة وتمكين = حل عملي ذكي

---

## ما يحتاج مراجعة يدوية قبل الرفع

- [ ] تحديث رقم واتساب في جميع الملفات
- [ ] إضافة فيديو كامن موشن أو إبقاء الـ placeholder
- [ ] ربط نموذج growth-map.html بـ backend (Formspree أو غيره)
- [ ] مراجعة محتوى النصوص والتأكد من التوافق مع المنهجية النهائية
- [ ] اختبار الموقع على الجوال (iPhone + Android)
- [ ] مراجعة روابط الـ anchor (#methodology, #paths, الخ) للتأكد من عملها
