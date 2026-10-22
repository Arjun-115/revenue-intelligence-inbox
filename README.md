# Revenue Intelligence Inbox

**Assignment II – Part 1**
**Student:** Arjun V B – 711523BCB009
**Submitted:** October 23, 2026

---

## �� Live Deployed Link
**https://arjun-115.github.io/revenue-intelligence-inbox/**

> Open directly — no login or permission required.

---

## What It Does

A working Revenue Intelligence Inbox for sales managers to:
- Review call and meeting conversation data
- Understand pipeline activity and sentiment at a glance
- Route conversations automatically (Escalate / Close Now / Follow Up / Nurture)
- Export data as JSON, CSV, or Manifest
- Handle duplicate imports, updates, and manual corrections

---

## Features

| Feature | Description |
|---|---|
| **Dashboard** | Pipeline value, critical items, sentiment %, avg deal size, 4 live charts |
| **Inbox** | Search + filter by type/priority/stage/rep, sorted by urgency |
| **Detail View** | Full conversation info, action item checklist, sentiment indicator |
| **Routing** | Auto-routes each conversation with reasoning (ESCALATE/CLOSE/FOLLOW UP/NURTURE) |
| **Analytics** | Win/loss by rep, competitive intelligence, closing forecast |
| **Export** | JSON, CSV, Manifest, Priority filter, At-risk filter, Action items by rep |
| **Import** | Duplicate detection (exact + soft match), update merging, 3 simulation tests |
| **Manual Entry** | Add new conversations via modal form |
| **Findings** | 3 key findings with source evidence + 1 rejected decision |

---

## How to Run Locally

```bash
# Option 1: Python server
cd revenue-intelligence-inbox
python -m http.server 8000
# Open http://localhost:8000

# Option 2: Just open the file
start index.html
```

No dependencies. Pure HTML/CSS/JavaScript. Works offline after first load.

---

## Project Structure

```
revenue-intelligence-inbox/
├── index.html              ← Complete single-page application
├── data/
│   └── conversations.json  ← Sample dataset (10 conversations)
├── exports/
│   ├── conversations.json  ← Full export
│   ├── conversations.csv   ← CSV export
│   └── manifest.json       ← Export manifest
└── README.md
```

---

## Key Findings (Summary)

1. **GlobalRetail Ltd ($95k) is at critical risk** — competitor offering 2-week deployment vs 6-week. Needs VP escalation immediately.
2. **$225k closing within 2 weeks** — RetailMax ($78k) + Acme Corp ($52k) both in final negotiation with positive sentiment.
3. **HealthCo Systems ($130k) unblocked** — Technical review passed, HIPAA confirmed, ready for commercial proposal.

**Decision Rejected:** Auto-hiding Closed Lost deals — rejected because loss reasons contain competitive intelligence needed for coaching and re-engagement.

---

## Duplicate/Update Handling

- **Exact duplicate** (same ID, same content): skipped with log entry
- **Update** (same ID, different content): merged with `updated_at` timestamp
- **Soft duplicate** (same account/rep/date, different ID): flagged with `duplicate_of` reference, shown with warning banner in inbox
- Test using the 3 simulation buttons on the Import page
