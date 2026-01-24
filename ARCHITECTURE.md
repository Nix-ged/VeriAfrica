# VeriAfrica – System Architecture (Design Phase)

## Overview
The system is designed as an automated content engine that fetches, filters, stores, and serves information without manual publishing.

---

## Update Schedule
- Automated update jobs run every 30–60 minutes
- Frequency can be adjusted based on scale and operational cost

---

## Content Processing Flow
1. Scheduled task initiates (cron job)
2. New content is fetched from APIs and RSS feeds
3. Duplicate articles are removed
4. Content is filtered based on predefined rules
5. Articles are ranked by relevance, freshness, and region
6. Approved content is stored in the database
7. The application serves content directly from the database

---

## Availability Logic
- Updates occur continuously, regardless of user activity
- Content is always available when users open the application
- No dependency on manual uploads

---

## Data Stored
- Title
- Source
- Category
- Region
- Publication time
- Summary
- Original URL

---

## Future Enhancements
- Automated relevance scoring
- Language translation
- Sentiment analysis
