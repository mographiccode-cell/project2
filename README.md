# 🎓 Student Mail Merge — دمج بطاقات الطلاب

تطبيق Flutter لدمج بيانات الطلاب من **Excel** داخل تصميم بطاقات **Word**، مع الحفاظ على القالب وإنتاج ملف **DOCX** نهائي جاهز للطباعة والمشاركة.

**الإصدار الحالي: v1.6.0** — يعمل على Android وWindows 10/11.

## ⬇️ التحميل

- **Android APK:** https://github.com/mographiccode-cell/project2/releases/latest/download/Student-Mail-Merge-v1.6.0.apk
- **Windows Installer EXE:** https://github.com/mographiccode-cell/project2/releases/latest/download/Student-Mail-Merge-Windows-Installer-v1.6.0.exe
- **Windows Portable ZIP:** https://github.com/mographiccode-cell/project2/releases/latest/download/Student-Mail-Merge-Windows-Portable-v1.6.0.zip
- **صفحة Releases:** https://github.com/mographiccode-cell/project2/releases

## المزايا

- استيراد XLSX/XLS مع دعم عدة Sheets.
- اكتشاف الاسم، الصف، اللجنة، ورقم الجلوس.
- دمج البيانات داخل قالب DOCX الموجود بدل إعادة تصميم البطاقة.
- الناتج النهائي **Word DOCX فقط**.
- رقم جلوس متسلسل من الرقم الذي يحدده المستخدم.
- توزيع اللجان **اختياري**:
  - عند إيقافه: تبقى اللجنة الموجودة في Excel كما هي.
  - عند تشغيله: يتم توزيع الطلاب بالتساوي قدر الإمكان.
- كتابة أسماء اللجان بالعربية: **الأولى، الثانية، الثالثة... الحادية عشرة، الحادية والعشرون...** حتى 999 لجنة.
- الفرق بين أكبر وأصغر لجنة لا يتجاوز طالبًا واحدًا.
- قسم **الملفات النهائية** مع فتح ومشاركة وحذف ملفات Word.
- واجهة عربية RTL.
- Android وWindows من نفس Source Code.

## الاستخدام

1. اختر ملف Excel.
2. اختر قالب Word DOCX.
3. أدخل بداية رقم الجلوس، مثل 300.
4. فعّل **توزيع اللجان تلقائيًا** فقط إذا احتجته، ثم أدخل عدد اللجان.
5. اضغط **دمج ملف Word**.
6. افتح أو شارك الملف من قسم **الملفات النهائية**.

## قالب Word

يدعم البطاقات الموجودة داخل جداول Word والتسميات مثل:

```text
اسم الطالبة:
الصف:
اللجنة:
رقم الجلوس:
```

ويدعم كذلك:

```text
{{الاسم}}
{{الصف}}
{{اللجنة}}
{{رقم الجلوس}}
```

أو حقول الدمج `«الاسم»` ونحوها.

يمكن تغيير الألوان والشعار والخطوط والحدود وحجم البطاقة، ويستخدم التطبيق تصميم Word نفسه كأساس للدمج.

## التطوير

المتطلبات:
- Flutter Stable
- Android SDK
- Visual Studio + Desktop development with C++ لبناء Windows

```bash
flutter pub get
flutter analyze
flutter test
flutter run
```

إذا لم تكن ملفات المنصات موجودة:

```bash
flutter create --platforms=android,windows --org com.mographiccode --project-name student_mail_merge .
```

## GitHub Actions

Workflow المشروع يقوم تلقائيًا بـ:
- تجهيز ملفات Android وWindows عند الحاجة.
- Analyze + Tests.
- بناء APK.
- بناء Windows Release وInstaller.
- اختبار تشغيل النسخة المثبتة.
- نشر APK وEXE وPortable تلقائيًا داخل GitHub Releases.

## هيكل المشروع

```text
lib/
test/
installer/
.github/workflows/
pubspec.yaml
README.md
CHANGELOG.md
```

---

**تصميم وبرمجة : م.محمود دغَبس**  
**مبايل: 774813824**
