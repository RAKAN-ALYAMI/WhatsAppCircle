# مميزات نظام WhatsApp Circle

## نظرة عامة
نظام WhatsApp circle هو منصة متكاملة لإدارة أرقام الهواتف وتوزيع النقرات بالتساوي بين الموظفين، مصممة خصيصًا للاستخدام مع تطبيق WhatsApp. النظام مبني بلغة PHP مع واجهة مستخدم عربية سهلة الاستخدام.

## فيديو توضيحي
شاهد الفيديو التوضيحي لنظام WhatsApp Circle:

[![فيديو توضيحي لنظام WhatsApp Circle](https://img.youtube.com/vi/A5dQoXAtHvM/0.jpg)](https://www.youtube.com/watch?v=A5dQoXAtHvM)


## المميزات الرئيسية

### 1. نظام توزيع النقرات الدائري
- **توزيع عادل للعملاء**: يقوم النظام بتوزيع النقرات (العملاء) بالتساوي بين جميع الموظفين باستخدام نظام دائري
- **تتبع آخر موظف**: يحتفظ النظام بسجل لآخر موظف تم توجيه عميل إليه، ليضمن أن الموظف التالي في الدائرة هو من سيستقبل العميل القادم
- **إحصائيات دقيقة**: عرض عدد النقرات لكل موظف بشكل دقيق في لوحة التحكم
- **توجيه تلقائي**: عند النقر على الرابط، يتم توجيه العميل مباشرة إلى رقم الموظف التالي في الدورة

### 2. إدارة الموظفين والأرقام
- **عرض الأرقام**: عرض قائمة بأرقام الهواتف المسجلة مع أسماء أصحابها
- **إضافة أرقام جديدة**: إمكانية إضافة أرقام هواتف جديدة بسهولة
- **حذف الأرقام**: إمكانية حذف الأرقام غير المرغوب فيها
- **تنبيه لإضافة رمز الدولة**: تنبيه واضح يذكر المستخدم بضرورة إضافة رمز الدولة (مثل +966) عند إدخال أرقام الهواتف

### 3. نظام إدارة المستخدمين
- **تسجيل دخول آمن**: واجهة تسجيل دخول مع تشفير كلمات المرور
- **تغيير كلمة المرور**: صفحة مخصصة لتغيير الرقم السري بطريقة آمنة
- **التحقق من صحة كلمة المرور**: نظام للتحقق من كلمة المرور الحالية قبل تغييرها

### 4. واجهة مستخدم متميزة
- **تصميم متجاوب**: واجهة تعمل على جميع أحجام الشاشات
- **ألوان WhatsApp**: استخدام ألوان مستوحاة من تطبيق WhatsApp
- **واجهة عربية كاملة**: دعم كامل للغة العربية مع توجيه من اليمين إلى اليسار
- **أيقونات معبرة**: استخدام أيقونات Font Awesome لتحسين تجربة المستخدم

## كيف يعمل نظام التوزيع الدائري؟

1. عندما يزور العميل رابط النظام، يقوم النظام بتحديد الموظف التالي في الدائرة
2. يتم توجيه العميل مباشرة إلى محادثة WhatsApp مع الموظف المحدد
3. يتم تسجيل النقرة وزيادة عداد النقرات للموظف
4. يتم تحديث سجل آخر موظف تم توجيه عميل إليه
5. في المرة القادمة، سيتم اختيار الموظف التالي في الترتيب

هذه الطريقة تضمن توزيعًا عادلًا للعملاء بين جميع الموظفين، مما يساعد على:
- تحقيق العدالة في توزيع فرص المبيعات
- تخفيف الضغط على موظف واحد
- تحسين وقت الاستجابة للعملاء
- تسهيل متابعة أداء كل موظف من خلال إحصائيات النقرات

## طريقة التركيب

### 1. تثبيت ملفات النظام
1. قم برفع جميع ملفات النظام إلى مجلد باسم `whatsapp` في المسار الرئيسي لموقعك
2. قم برفع صورة أيقونة الواتساب باسم `whatsapp.png` داخل المجلد الرئيسي `www` أو `public_html`

### 2. إعداد قاعدة البيانات
1. قم بإنشاء قاعدة بيانات MySQL جديدة
2. قم باستيراد ملف `whatsapp.sql` إلى قاعدة البيانات:
   - من خلال phpMyAdmin: انتقل إلى قاعدة البيانات التي أنشأتها، ثم انقر على "استيراد" واختر ملف whatsapp.sql
   - أو من خلال سطر الأوامر: `mysql -u username -p database_name < whatsapp.sql`
3. قم بتعديل ملف `config.php` وأدخل بيانات الاتصال بقاعدة البيانات الخاصة بك:
   - اسم المضيف (عادة localhost)
   - اسم المستخدم
   - كلمة المرور
   - اسم قاعدة البيانات

### 3. معلومات تسجيل الدخول
بعد تثبيت النظام، يمكنك تسجيل الدخول باستخدام بيانات الاعتماد الافتراضية:
- **اسم المستخدم:** admin
- **كلمة المرور:** 123456789

> **تنبيه هام**: يجب تغيير كلمة المرور الافتراضية فور تسجيل الدخول لأول مرة من خلال لوحة التحكم للحفاظ على أمان النظام.

### 4. إضافة زر الواتساب إلى موقعك
قم بإضافة الكود التالي في الفوتر أو الهيدر أو أي ملف تريده في موقعك:

```html
<!-- أيقونة WhatsApp -->
<div class="whatsapp-fixed">
    <a href="whatsapp/redirect.php">
        <img src="whatsapp.png" alt="WhatsApp" class="whatsapp-icon">
    </a>
</div>

<style>
    /* تنسيق الأيقونة لتكون ثابتة أسفل يمين الشاشة */
    .whatsapp-fixed {
        position: fixed;
        bottom: 20px; /* المسافة من أسفل الشاشة */
        right: 20px; /* المسافة من يمين الشاشة */
        z-index: 1000;
        background-color: #25d366;
        border-radius: 50%;
        display: flex;
        align-items: center;
        justify-content: center;
        box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    }

    /* حجم الأيقونة يمكن التحكم به هنا */
    .whatsapp-icon {
        width: 60px; /* يمكنك تغيير هذا القيمة للتحكم في العرض */
        height: 60px; /* يمكنك تغيير هذا القيمة للتحكم في الارتفاع */
    }
</style>
<!-- أيقونة WhatsApp -->
```
## متطلبات النظام
- PHP 7.0 أو أحدث
- MySQL 5.6 أو أحدث
- خادم ويب (Apache/Nginx)

## الترخيص
هذا النظام مرخص حصريًا لـ: RAKAN ALYAMI
للتواصل: Telegram: @r7000r | البريد الإلكتروني: rakan7777@gmail.com
