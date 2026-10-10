# اتصال پروژه‌ها

AI-Hub زیرساخت مشترک است. Clientها از طریق Taskهای منطقی AI متصل می‌شوند و مستقیماً به Provider خارجی وابسته نیستند.

## Integration تأییدشده: Tel-News

Tel-News یک پلتفرم چندمنبعی پردازش و انتشار خبر است که پردازش Local را با Stageهای منتخب AI در AI-Hub ترکیب می‌کند.

```text
News Sources
  -> Local normalization/filtering
  -> Deduplication where applicable
  -> AI-Hub task
  -> Centrally selected provider/model
  -> Structured result
  -> Publishing pipeline
```

طراحی گسترده‌تر از Stageهایی مانند relevance filtering، event extraction، semantic processing، writing/rewriting، quality review و translation پشتیبانی می‌کند.
