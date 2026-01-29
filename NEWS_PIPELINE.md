# NEWS_PIPELINE.md
Project: VeriAfrica  
Purpose: Define how news is fetched, verified, and updated

---

## 1. Objective

This document describes the complete lifecycle of news content from source to user.

---

## 2. Content Sources

Primary sources include:
- News APIs (global and African-focused)
- RSS feeds from verified publishers
- Partner organizations (future phase)

No user-generated news is allowed.

---

## 3. Update Frequency

- Content fetch runs every 30–60 minutes
- Critical news sources may run more frequently
- Entertainment content may update less frequently

Schedules are configurable.

---

## 4. Pipeline Stages

### Stage 1: Fetch
- Request latest articles from each source
- Limit fetch to new or updated items only

### Stage 2: Normalize
- Convert all content to a unified structure
- Extract metadata (source, time, region, category)

### Stage 3: Deduplication
- Compare new content with existing records
- Remove duplicates using:
  - URL matching
  - Title similarity
  - Content hashing

### Stage 4: Filtering
- Apply keyword and category filters
- Remove clickbait or misleading headlines
- Flag suspicious content

### Stage 5: Scoring
- Assign relevance score based on:
  - Source trust
  - Recency
  - Regional importance

### Stage 6: Storage
- Store approved content as active
- Store flagged content as review-required

---

## 5. Source Failure Handling

If a source fails:
- Log the error
- Skip the source for that cycle
- Retry in the next scheduled run

The system never depends on a single source.

---

## 6. Misinformation Control

- Only pre-approved sources are allowed
- Keyword-based alerts flag risky content
- Admin review exists as a final safeguard

---

## 7. Output

Only content that passes the pipeline is visible to users.

This ensures accuracy, stability, and trust.
