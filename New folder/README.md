# SwimFlow — نظام إدارة تدريبات السباحة

موقع بسيط لإدارة الرياضيين، المواعيد، وسجلات الحضور. هذا المشروع جاهز للنشر عبر GitHub Pages.

## ما تمّ إضافته
- `index.html` — صفحة الموقع الرئيسية (واجهات ادمن وزائر، تخزين محلي عبر localStorage).
- `CNAME` — ضع اسم الدومين الخاص بك هنا (مثال: `example.com`).
- `.github/workflows/deploy.yml` — Action لنشر المحتوى تلقائياً إلى فرع `gh-pages` عند الضغط على `main`.
- `.gitignore` — قواعد تجاهل بسيطة.

## خطوات سريعة للرفع إلى GitHub
1. افتح مجلد `Documents` في طرفية Git أو في VS Code.
2. أنشئ مستودع محلي وادفعه إلى GitHub:

```bash
git init
git add .
git commit -m "Initial site: SwimFlow"
# أنشئ مستودعاً جديداً على GitHub ثم اربطه (بدّل URL بالمستودع الخاص بك)
git remote add origin https://github.com/<username>/<repo>.git
git branch -M main
git push -u origin main
```

3. الملف `.github/workflows/deploy.yml` سينشر الملفات تلقائياً إلى فرع `gh-pages` عند كل `push` إلى `main`.

4. لربط دومين مخصص:
 - استبدل محتوى ملف `CNAME` باسم الدومين الخاص بك (مثال: `mysite.com`).
 - في لوحة تحكم مزوّد الدومين، اضبط سجلات DNS: إذا كنت تستخدم GitHub Pages على `gh-pages` أو `username.github.io` اتبع تعليمات GitHub (عادة A-records لِـ GitHub Pages أو CNAME إلى `username.github.io`).

## ملاحظات أمان بسيطة
- كلمة مرور الادمن موجودة في الشيفرة (`2908`) لأغراض تجربة محلية فقط — استبدلها أو أزل واجهة الادمن قبل الاستخدام العام.
- البيانات تُخزّن محلياً في `localStorage`. إن أردت تخزين مركزي، أضيف backend لاحقاً.

إذا تريد، أقدر أهيئ المستودع لك أو أعدّل الإعدادات لينشر باسم الدومين مباشرة. تريد أكمّل؟
