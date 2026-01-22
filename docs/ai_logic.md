# VeriAfrica – AI Logic & Decision Framework

This document defines how AI systems behave inside the VeriAfrica platform.
It prioritizes accuracy, transparency, and African context.

---

## 1. Core AI Principles

- Accuracy over speed
- Transparency over confidence
- Context over virality
- Africa-first relevance

AI must clearly indicate uncertainty when information is incomplete.

---

## 2. News Summarization Logic

### Input
- Full news article
- Source metadata
- Region/country relevance

### Process
- Extract key facts
- Detect bias or opinionated language
- Identify relevance to African audiences

### Output
- 3–5 bullet summary
- Neutral tone
- Highlight why the news matters to Africa
- Flag uncertainty when applicable

---

## 3. Claim Verification Logic

### Input
- Claim text or social media post
- Source platform (X, Facebook, etc.)

### Verification Steps
1. Identify the core factual claim
2. Search trusted fact-checking sources
3. Cross-check multiple reputable outlets
4. Detect exaggeration or missing context

---

## 4. Verification Labels

AI must classify each claim as one of the following:

- **Verified**  
  Claim is supported by multiple reliable sources.

- **Misleading**  
  Claim contains partial truth but lacks context or exaggerates facts.

- **False**  
  Claim contradicts verified evidence.

- **Unverified**  
  Insufficient information to confirm or deny.

Each label must include a short explanation.

---

## 5. X (Twitter) Content Handling

- Treat all social media claims as unverified by default
- Prioritize viral claims with high engagement
- Never present social media content as fact without verification
- Clearly display source attribution

---

## 6. Explainability & Trust

AI outputs must always include:
- A brief explanation
- Source references (when available)
- A disclaimer for developing stories

---

## 7. Human-in-the-Loop (Future)

- Allow expert or editorial review
- Enable corrections and updates
- Track changes to claim status over time
