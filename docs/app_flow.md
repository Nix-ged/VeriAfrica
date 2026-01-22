# VeriAfrica – App Flow Blueprint

This document defines the structure and behavior of the VeriAfrica platform.
It serves as a blueprint for future implementation using Windsurf and AI services.

---

## 1. Home Page (Africa First)

### Purpose
Display the most important verified news relevant to African users.

### Inputs
- News articles from trusted African and global sources
- User-selected country or region
- AI summarization engine

### Outputs
- Short AI-generated summaries (3–5 bullets)
- Verification labels:
  - Verified
  - Misleading
  - False
  - Unverified
- Country-based filtering

---

## 2. Viral Claims (X / Twitter)

### Purpose
Track and verify trending claims spreading on social media, especially X.

### Inputs
- Trending posts or claims from X
- Claim text or post link
- AI verification model
- Fact-checking sources

### Outputs
- Claim cards showing:
  - Claim text
  - Source (X)
  - Verification status
- Clickable detail view with:
  - Explanation
  - Sources
  - Confidence level

---

## 3. Fact Check Page

### Purpose
Allow users to submit claims for verification.

### Inputs
- User-submitted text or link
- AI analysis model
- External trusted sources

### Outputs
- Verdict:
  - Verified
  - Misleading
  - False
  - Unverified
- Short explanation
- Source citations

---

## 4. Opportunities Page

### Purpose
Provide users with real opportunities relevant to Africa.

### Inputs
- Curated data on scholarships, jobs, grants, programs
- Regional relevance filters

### Outputs
- Opportunity listings
- Category filtering
- External links to apply

---

## Notes
- AI decisions must be transparent and explainable
- Clear disclaimers for unverified or developing claims
- Local relevance is prioritized over global noise
