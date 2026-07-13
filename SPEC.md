One Place — Spec & MVP Plan

Overview

One Place is a calm, visual platform for children and families (and schools with permission) to centralize schedules, travel, wellbeing support and occurrences.

Primary users:
- Child (age ~6–12) — simple, visual app
- Parent — management, logging, sharing
- School staff (with permission) — view Support Passport and observations

Core Goals
- Reduce overwhelm with simple, predictable UI
- Centralize school/home schedules and travel
- Provide quick wellbeing support and structured logging
- Allow parents control over sharing with schools

Screens (child-facing)

1) Today (already prototyped)
- Purpose: At-a-glance Now / Next / Later timeline, micro-checklist, transport ETA, quick Help Me.
- Key components: NowCard (micro-tasks), TransportCard (ETA), EventCard list, Help Me button, bottom nav.
- States: Normal, empty, overdue, offline.

2) My Week (prototype page created)
- Purpose: Week view with colored blocks per day and quick drill-down to day details.
- Key components: Week grid, Day details list, Add routine.

3) Help Me (prototype page created)
- Purpose: Quick emotional support choices, immediate calming suggestions, log occurrence for parent.
- Key components: Preset feeling buttons, suggestions list, optional parent notification.

4) Travel / My Bus (prototype created)
- Purpose: Show next bus, map, status, leave-home guidance.
- Key components: NextBus card, status, simple map placeholder.

Screens (parent-facing) — spec highlights

1) Parent Dashboard
- Purpose: Manage child profile, add/edit activities, view Today/My Week, see occurrences and patterns.
- Key actions: Add Activity, Record Occurrence, View Patterns, Download Support Passport (PDF), share controls.

2) Add/Edit Activity
- Fields: title, date/time, recurrence, location, notes, reminder, createdBy.

3) Record Occurrence
- Guided fields: What happened before? What happened? What helped? Anything different? Attachments, timestamp.

4) Patterns & Insights
- Aggregated view (last 30/90 days): top triggers, helpful strategies, charts, exportable CSV/PDF.

5) Support Passport
- Shareable summary: things that help, difficulties, strategies, visual timetable. Download PDF and control recipients.

School View (permissioned)
- Student overview, Observations, Strategies, Files. Can add observations; parents control what is shared.

MVP Priorities (recommended order)

MVP-1 (Core):
- Accounts: Parent account + child record and basic pairing.
- Child Today screen (static + checklist) — already prototyped.
- Parent Add Activity (create/edit events) and flow to sync to child.
- Local persistence + one-way sync (child reads parent events).

MVP-2 (Wellbeing & Logging):
- Help Me quick flow (child-side) + occurrence logging (child & parent inputs).
- Record Occurrence form for parents.
- Notifications (event reminders, Help Me logs).

MVP-3 (Sharing & Insights):
- Support Passport export (PDF) and basic sharing to school via invite/permission.
- Simple Patterns & Insights dashboard (counts, top triggers).
- Transport card with ETA (basic manual input or integration).

MVP-4 (Polish & Scale):
- Offline-first syncing and conflict resolution.
- Accessibility modes, high-contrast, reduced motion.
- Analytics (privacy aware) and opt-ins; map integration; school portal improvements.

Estimated Effort (rough)
- Small prototype (static screens): 1–2 developer-days per screen.
- Working MVP-1 (accounts, sync, Today, parent add/edit): 2–4 developer-weeks.
- Full MVP (MVP-1 + 2 + basic sharing): 2–3 developer-months.

Suggested Tech Stack
- Mobile-first: React Native + TypeScript.
- Backend: Node.js + Express or Firebase for faster MVP.
- Database: PostgreSQL (server) + SQLite/WatermelonDB on-device for offline.
- Notifications: Firebase Cloud Messaging / APNs.
- Auth: Email/password + parent invite flow; consider OAuth for staff accounts.
- Map/ETA: Mapbox or Google Maps; for bus ETA use transport APIs or manual schedules initially.

Data Model (high-level)
- Child, Event, Occurrence, User (parent/staff), SupportPassport.
- Event fields: id, childId, title, type, startTime, endTime, location, notes, recurrence, reminder, createdBy, completed.
- Occurrence fields: id, childId, eventId?, timestamp, beforeText, happenedText, whatHelpedText, recordedBy.

Privacy & Safety
- Parent controls all sharing to school; explicit consent flows.
- Data encrypted in transit; consider server-side encryption at rest.
- Minimize PII exposure in analytics; require parental opt-in for sharing.

Next Deliverables I can do for you (pick one or let me choose):

A) Create Parent Dashboard prototype (HTML) — so you can see the parent view and how to add events.
B) Scaffold a minimal React Native app with the Child Today screen (working locally with mock data).
C) Export this SPEC as a PDF and produce a one-page investor/funder summary.
D) Walk you through how to run the prototype locally step-by-step (I can provide screenshots and commands).

Clarifying questions (if you want me to build further):
- Which user would you like us to prioritise next: child features, parent dashboard, or school sharing?
- Would you prefer a web-first approach (PWA) or mobile-first React Native app?
- Do you already have hosting or a preferred backend (Firebase, Vercel, AWS)?

How I’ll help next (I’ll take care of the tech):
- I can build the Parent Dashboard prototype now if you want a simple web view to show parents what they’d see.
- If you want an installable app later, I can scaffold the RN project and include a small README with run instructions.

---

Files created in this workspace:
- `/workspace/oneplace-prototype/index.html` — Today prototype
- `/workspace/oneplace-prototype/myweek.html` — My Week prototype
- `/workspace/oneplace-prototype/helpme.html` — Help Me prototype
- `/workspace/oneplace-prototype/travel.html` — Travel prototype
- `/workspace/oneplace-prototype/SPEC.md` — this spec

Tell me which next deliverable above you want, or say "You choose" and I'll build the Parent Dashboard prototype now.