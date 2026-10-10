# Integrations

AI-Hub is shared infrastructure. Client projects integrate through logical AI tasks instead of coupling directly to an external AI provider.

## Confirmed Integration: Tel-News

Tel-News is a multi-source news processing and publishing platform. It combines local processing with selected AI stages delegated to AI-Hub.

```text
News Sources
  -> Local normalization/filtering
  -> Deduplication where applicable
  -> AI-Hub task
  -> Centrally selected provider/model
  -> Structured result
  -> Publishing pipeline
```

The wider design supports AI-oriented stages such as relevance filtering, event extraction, semantic processing, writing/rewriting, quality review, and translation.
