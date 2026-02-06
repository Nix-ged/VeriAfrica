# Data Model

## Article Object

Each piece of content stored in the system includes:

- id
- title
- summary
- source_name
- source_url
- category (news, entertainment, sports, etc.)
- region (global, Africa, Rwanda)
- language
- published_at
- fetched_at
- credibility_score
- tags

---

## Source Object

- source_id
- name
- type (news, entertainment)
- region
- verified (true/false)

---

## User Interaction (Later Phase)

- views
- clicks
- saves
- shares