# ROLES.md
Project: VeriAfrica  
Purpose: Define access levels and permissions

---

## 1. Overview

Clear role separation prevents abuse, errors, and platform instability.

---

## 2. Roles Defined

### 1. User
Permissions:
- Read public content
- Filter by category and region

Restrictions:
- No content creation
- No moderation access

---

### 2. Premium User
Permissions:
- All User permissions
- Access to premium or early content
- Reduced ads (if applicable)

Restrictions:
- No moderation or system access

---

### 3. Admin
Permissions:
- Approve or remove content
- Pin important news
- Flag unreliable sources
- View system logs

Restrictions:
- Cannot modify system automation logic

---

### 4. System (Automated Jobs)
Permissions:
- Fetch external data
- Process and store content
- Update content status automatically

Restrictions:
- No manual decision-making
- No user interaction

---

## 3. Role Enforcement

- Each API endpoint checks role permissions
- Unauthorized actions are blocked and logged

---

## 4. Principle

No role has unnecessary access.
Automation and human control are strictly separated.
