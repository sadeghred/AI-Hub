# AI-Hub

**درگاه مرکزی هوش مصنوعی و لایه هماهنگ‌سازی برای چند پروژه**

[English](README.md) · [معماری](docs/fa/ARCHITECTURE.md) · [امنیت](docs/fa/SECURITY.md) · [اتصال پروژه‌ها](docs/fa/INTEGRATIONS.md) · [نقشه راه](docs/fa/ROADMAP.md)

> **Repository عمومی:** فقط برای معرفی پروژه و مستندات. سورس خصوصی، بسته قابل Deploy، Credentialها، API Keyها، Backupهای Production و فایل دانلود برنامه منتشر نمی‌شوند.

## معرفی

AI-Hub یک سرویس مرکزی هوش مصنوعی است که به چند برنامه مستقل اجازه می‌دهد به‌جای پیاده‌سازی جداگانه SDK، Credential، Routing و Fallback هر Provider، درخواست‌های AI خود را از طریق یک Gateway کنترل‌شده ارسال کنند.

## قابلیت‌های اصلی

- **یک Gateway هوش مصنوعی برای چند پروژه**
- مدیریت مرکزی Provider و Model
- Routing بر اساس Task به‌جای اتصال سخت به Provider
- معماری Fallback بین Provider/Model و Rotation Credential
- جداسازی Credentialهای Provider از پروژه‌های Client
- Async Worker مستقل
- Administration Service مستقل
- State/Configuration مرکزی مبتنی بر PostgreSQL
- کنترل مستقل سرویس‌های Linux

## معماری

```text
Client Projects
      |
      v
AI-Hub Gateway
      |
      +----> Task Routing ----> Provider / Model ----> AI Provider(s)
      |
      +----> Async Worker
      |
      v
Structured Result -> Client Project

Administration Service
```

استقرار تأییدشده از سه سرویس مستقل Gateway، Worker و Administration تشکیل شده است.

## مدل اتصال

`Client Project → AI-Hub → Provider / Model → Structured Result → Client Project`

یکی از Integrationهای عملیاتی تأییدشده **Tel-News** است؛ یک سامانه چندمنبعی پردازش و انتشار خبر که عملیات AI منتخب را به Hub می‌سپارد و مستقیماً به یک Provider خاص وابسته نمی‌شود.

## امنیت در طراحی

پروژه‌های Client نیازی به دسترسی مستقیم به Credentialهای Provider ندارند. مستندات عمومی عمداً API Key، Token، Password، جزئیات خصوصی سرور، Credential دیتابیس، Secretهای داخلی و Implementation خصوصی قابل Deploy را منتشر نمی‌کنند.

## مصرف عملیاتی

در یک اندازه‌گیری عملی پس از پایدارشدن Startup، مجموع RSS سه Process حدود **210 تا 220 MiB** بود. این عدد مشاهده عملی است و Hardware Requirement رسمی نیست.

## وضعیت پروژه

AI-Hub زیرساخت مرکزی عملیاتی و در حال توسعه است و اتصال پروژه‌های دیگر به آن مرحله‌ای انجام می‌شود. این Repository معماری و قابلیت‌ها را معرفی می‌کند و سورس خصوصی را توزیع نمی‌کند.

## تماس

- تلگرام: [@Sadeghred](https://t.me/Sadeghred)
- ایمیل: [sadeghred@gmail.com](mailto:sadeghred@gmail.com)

---
© 2026 AI-Hub Project
