# معماری

AI-Hub دسترسی به هوش مصنوعی را برای چند برنامه مستقل در یک نقطه متمرکز می‌کند.

## اجزای اصلی

### Central Gateway
Taskهای منطقی AI را دریافت می‌کند، Routing و Configuration مرکزی را اعمال می‌کند، Backend انتخاب‌شده را فراخوانی می‌کند و نتیجه استانداردشده برمی‌گرداند.

### Async Worker
Jobهای پس‌زمینه و Queue-based را از مسیر اصلی درخواست جدا می‌کند.

### Administration Service
مدیریت عملیاتی را مستقل از Gateway اصلی فراهم می‌کند.

## اصول طراحی
1. متمرکزکردن پیچیدگی Providerها
2. خارج نگه‌داشتن Secretهای Provider از Clientها
3. استفاده از قرارداد Task-level
4. جداسازی Background Job از Request handling
5. امکان تغییر مرکزی Provider/Model
6. استقلال Processهای Client از چرخه Start/Stop هاب
