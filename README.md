# Endoscope Inspection & Repair Log

> A custom desktop + mobile web application prototype designed to digitize incoming/outgoing hardware inspection logs, active maintenance statuses, and serial number repair histories for medical endoscopes.

**Status:** In Progress — Built in public as my portfolio piece while working full-time in a medical lab.

### 🔗 Live Demo
Coming soon — GitHub Pages

### 🎨 Figma Prototype
[Figma Link - Desktop & Mobile Views]
- Desktop: Dashboard, Incoming Log, Outgoing Log, Serial History, Parts Reference
- Mobile: Incoming Service Report (long form) - Phone-first input

> [PLACEHOLDER: Add Figma screenshots]
> `![Dashboard - Desktop](/docs/figma-screenshots/dashboard.png)`
> `![Incoming Log - Desktop](/docs/figma-screenshots/incoming.png)`
> `![Outgoing Log - Desktop](/docs/figma-screenshots/outgoing.png)`

---

### The Case Story: Why I Built This

In my medical lab, the entire inspection cycle is still manual:

1.  Endoscope arrives with damage → logged on paper service report
2.  Photos/videos taken on phone → manually uploaded to Google Drive (3-4 mins per video, and only if Wifi is stable)
3.  Sheets updated by hand → high risk of error and duplicate Serial Numbers
4.  Repair history is scattered across Drive folders, Google Sheets, Doc files and WhatsApp chats
5.  To find past damage for Serial 2934XXX, we have to search multiple places

**Result:** Verification is slow, history is hard to find, and photo/video evidence is not linked to the report.

I am building this tool to replace paper with a single source of truth.

> [PLACEHOLDER: Photo of current paper report - BLUR sensitive info]
> `![Current paper workflow](/docs/photos/paper-report.jpg)`

### Who Is It For?

**1. Field Service Technician (Primary)**
Works on-site and on the lab floor. Needs to log fast and find history fast.

**2. QA Lab Technician**
Verifies reports and closes the maintenance cycle on desktop.

### User Stories

**For Field Technician — The most useful parts:**

1.  As a technician, I want to fill out the Incoming Service Report digitally on my phone, so I don't have to write on paper and re-type it later in Excel.
2.  As a technician, I want to search a Serial Number (e.g. 2934039) and instantly see its full repair history, so I know what was fixed before.
3.  As a technician, I want easy access to past photos and videos for a specific serial number, so I can compare new damage with previous damage and avoid repeat diagnostics.
4.  As a technician, I want to upload photos directly from my phone camera in the form, so the evidence is immediately linked to the report.

**For QA:**

1.  As QA, I want all incoming and outgoing logs in one searchable table with photo/video/Drive links attached, so I can verify without chasing files on chat.
2.  As QA, I want outgoing reports to automatically link back to the incoming report and serial history, so the entire cycle is traceable.

> [PLACEHOLDER: Mobile form sketch / Figma]
> `![Incoming Service Report - Mobile](/docs/figma-screenshots/mobile-form.png)`

### What I'm Building

**Core Features:**

- **Dashboard:** Overview of Incoming Pending, Outgoing Pending Verification, Active Maintenance, Total Scopes
- **Incoming Log:** Date, Model (TJF-Q180V, GIF-H190, PCF-H190DL), Serial Number, Damage Type, Evidence (Photo/Video/Drive), Status Badge
- **Outgoing Log:** Date Out, Technician, Verification Status, Linked to Incoming Report
- **Serial History View:** Search any SN → Timeline of all repairs + all linked photos/videos
- **Incoming Service Report (Long Form - Mobile First):**
    - Step 1: Scope Identity (Date, Model, Serial Number, Source)
    - Step 2: Damage & Assessment (Damage Type, Description, Leak Test)
    - Step 3: Evidence (Photo Upload with previews, Video Upload, Drive Link)

### Tech Stack & Architecture

Built from scratch on purpose — this is my portfolio piece documenting the full research and build process.

**Current:**
- **Structure:** Semantic HTML5 (header, section, form, fieldset, table)
- **Presentation:** Custom responsive CSS (CSS Grid + Flexbox architecture)

**Planned:**
- **Logic:** JavaScript (Month 3-6) - Search by SN, form validation, draft save, filter
- **Backend:** Cloud database like SQL (Month 10-12) - To store repair histories and file references

**Design Principle:** Clean, clinical, professional. White and soft gray surfaces, blue primary #2563EB for actions, readable tables. Designed for long shifts — spacious on desktop, large touch targets on mobile.

### Project Structure (STILL BUILDING)
/docs
  /figma-screenshots    <- Desktop views + mobile form
  /photos               <- Paper forms (redacted - blur hospital/SN)
  user-stories.md       <- Detailed user stories for tech + QA
  current-workflow.md   <- How it works today: paper → Drive
  research.md           <- Why you chose HTML/CSS from scratch, SQL later
/prototype              <- Your actual HTML/CSS code
  index.html
  /css
  /assets
README.md               <- This file (main portfolio story)
roadmap.md              <- Checklist of what is done / next
