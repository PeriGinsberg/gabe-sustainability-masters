# Gabe Casiello — Sustainability Master's Programs Dashboard

A personal decision-support dashboard for evaluating sustainability master's programs and tracking applications.

## What this is

An interactive single-file HTML dashboard covering 8 sustainability master's programs across three fit tiers, with built-in:
- Candidate profile capture
- Program-by-program ratings (5-star), interest level, and apply/maybe/skip decisions
- Discussion notes per program
- Side-by-side comparison table
- Forced-choice decision questions
- Application tracker (deadlines, recommenders, essays, status)
- Sample timeline for September 2027 start
- Local data persistence (auto-saves to browser)
- JSON export/import for backup and sync

## Quick start

1. Open `index.html` in any browser
2. Walk through the Overview tab to capture Gabe's profile (GPA, preferences, constraints)
3. Use the Programs tab to walk through each option together — capture his rating, interest level, decision, and notes in real-time
4. Use Compare to see all dimensions at once
5. Use Decision Helper to surface his top picks
6. Once narrowed, populate the Application Tracker

Everything auto-saves locally as you go. Use the Data tab to export to JSON for backup.

## Programs included

**Tier 1 — Best fit:**
1. Penn State World Campus — MPS in Renewable Energy & Sustainability Systems (RESS)
2. American University — Kogod MS in Sustainability Management

**Tier 2 — Strong options:**
3. Bard College — MS in Environmental Policy
4. Bard College — MBA in Sustainability
5. Rochester Institute of Technology — MS in Sustainable Systems

**Tier 3 — Stretch options:**
6. University of Miami Herbert — MS in Sustainable Business
7. CU Denver — MS in Sustainable Business
8. Stevens Institute of Technology — MS in Sustainability Management

## Recommended repo structure

```
gabe-sustainability-masters/
├── index.html                    ← this dashboard
├── README.md
├── data/                         ← JSON exports for version history
│   └── dashboard-2026-05-18.json
├── essays/                       ← drafts and revisions of SOPs
│   ├── kogod-sop-v1.md
│   ├── psu-sop-v1.md
│   └── bard-sop-v1.md
├── recommenders/                 ← recommender tracking
│   └── recommender-tracking.md
├── research/                     ← additional program research, alumni interviews, etc.
│   ├── informational-interviews.md
│   └── scholarship-research.md
└── decisions/                    ← record of key decision points and rationale
    └── 2026-05-18-initial-discussion.md
```

## Workflow with Gabe

1. **Initial walkthrough (60–90 min):** Use the dashboard live. Capture his reactions on each program. Don't skip the Decision Helper's forced-choice questions.
2. **Export to JSON** after the meeting. Commit to repo with a descriptive message.
3. **Between meetings:** Add notes to the Programs tab as Gabe does informational interviews, attends webinars, or learns more.
4. **Subsequent meetings:** Re-rate programs as priorities clarify. The dashboard remembers everything.
5. **Application phase:** Use the Application Tracker once target list is finalized (auto-populate from "Apply" status).

## Technical notes

- Self-contained: no build step, no server, no dependencies (except Tabler icons CDN)
- Works fully offline once loaded
- Data lives in browser localStorage — survives refresh but is tied to the specific browser
- For cross-device sync, periodically export JSON and re-import on the other device
- To deploy as a GitHub Pages site, set repo to Pages-enabled with `index.html` at root

## Last updated

May 18, 2026 — Initial build covering 8 programs, candidate profile, decision helper, and tracker.
