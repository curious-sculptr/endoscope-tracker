# Research & Decisions

### Problem Observed
Incoming/outgoing inspection logs are still manual. Data lives in 3 places:
Paper report -> Phone photos/videos -> Google Drive -> Excel.

This causes:
- Duplicate serial numbers
- Missing photo evidence (link not pasted)
- No searchable history by Serial Number
- Technicians asking repeatedly for status

### Why Build From Scratch?
Chose to build from HTML/CSS first to:
1. Learn semantic HTML5 and CSS Grid/Flexbox properly
2. Document full journey for portfolio
3. Control the data model for medical hardware (SN is primary key)

Later: SQL database planned. Need table for scopes, repair history, and evidence links.

### Design Decisions
- **Mobile First for Input:** Incoming Service Report must be usable on lab floor with one hand
- **Desktop First for Review:** Dashboard, logs, serial history need wide tables
- **Table to Card:** On mobile, tables convert to cards (avoid horizontal scroll)
- **Color:** White/Gray base (#FFFFFF, #F8FAFC) + Blue action (#2563EB) — clinical, low fatigue for long shifts

### What I Looked At
- Current paper Incoming/Outgoing forms
- Drive upload time: 3-4 min per video, and only if Wifi is stable
- Figma for Ideation and Rapid Testing

### Open Questions
- How to compress video before upload?
- Auto-generate Drive folder structure by SN?
