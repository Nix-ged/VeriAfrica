# API_FLOW.md
Project: VeriAfrica  
Purpose: Define how data moves through the system via APIs

---

## 1. Objective

This document explains how data is:
- Created
- Processed
- Stored
- Served to users
- Moderated by admins
- Updated automatically by the system

It focuses on behavior, not implementation.

---

## 2. Core API Actors

The system interacts with four main actors:

1. External Content Sources  
2. System (Automated Jobs)  
3. Users  
4. Admins  

---

## 3. Data Creation Flow

1. External sources (news APIs, RSS feeds) expose new content
2. The system fetches raw content through scheduled API requests
3. Raw content is normalized into a standard internal format
4. Each item is assigned:
   - Source
   - Category
   - Region
   - Timestamp
   - Trust score (initial)

Content is not shown to users at this stage.

---

## 4. Data Processing & Storage

After creation:
1. Duplicate detection runs (based on title, URL, and content hash)
2. Content is filtered using predefined rules
3. Valid content is saved to the database with status = "active"
4. Flagged content is saved with status = "review"

---

## 5. User Data Fetch Flow

1. User opens the app
2. App requests content via public read APIs
3. API returns only:
   - Active content
   - Allowed categories
   - User-appropriate access level
4. Content is ordered by relevance and recency

Users never interact directly with raw sources.

---

## 6. Admin Moderation Flow

Admins can:
- Approve content
- Remove content
- Pin high-priority content
- Flag sources for review

Admin actions update content status in real time.

---

## 7. Automated System Actions

The system:
- Triggers scheduled fetch jobs
- Re-evaluates existing content
- Deactivates outdated or unreliable items
- Logs all automated actions for audit

---

## 8. Failure Handling

If an external API fails:
- The system logs the failure
- Continues using cached content
- Skips the source until the next cycle

No downtime is exposed to users.

---

## 9. Security Notes

- Read and write access are strictly separated
- Admin actions require elevated permissions
- Automated jobs operate under system-level access only
