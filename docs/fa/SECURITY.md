# امنیت

Repository عمومی نباید شامل API Keyهای Provider، Bot Token، Password، Secretهای Authentication، Credential خصوصی سرور، Credential دیتابیس Production، فایل Environment واقعی، Private Key، محتوای Credential Vault، Backup Production یا سورس خصوصی قابل Deploy باشد.

Clientها نباید Credential مستقیم Provider را نیاز داشته باشند؛ Credentialهای Provider تحت کنترل مرکزی AI-Hub باقی می‌مانند.

قبل از هر انتشار عمومی، مستندات و Screenshotها باید از نظر Secret، IP، Connection String، Logهای Production و اطلاعات حساس بررسی شوند.
