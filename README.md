# Project Intelligence Hub for Jira

**Stakeholder-ready project reports from Jira. One click.**

An Atlassian Forge app that generates professional project management reports directly from live Jira data. No copy-paste, no manual updates. Open, generate, export.

---

## What It Does

Project Intelligence Hub reads your Jira project data and generates formatted, editable reports ready for stakeholders, steering committees, and team retrospectives.

**7 Report Templates:**

| Template | Purpose | Audience |
|----------|---------|----------|
| Weekly Status Report | Sprint snapshot with metrics, blockers, team summary | Stakeholders, PMs |
| Release Notes | Auto-categorized changelog per version | Clients, documentation |
| Project Cockpit | Executive dashboard with RAG status across 5 dimensions | Leadership, PMO |
| RAID Log | Risks, Actions, Issues, Decisions register | Governance, PMs |
| Steering Committee | Monthly executive report for leadership | Steering committees |
| Sprint Retrospective | Structured retro with velocity and carry-over analysis | Scrum teams |
| Team Performance | Cross-sprint analytics, backlog health, quality metrics | Engineering managers |

**3 Export Formats:**
- **PDF** — Formatted A4 document (generated server-side via jsPDF)
- **Copy to Clipboard** — Rich HTML for pasting into Docs, Outlook, Word
- **Push to Confluence** — Creates a page in any space, with folder support

---

## Tech Stack

- **Platform**: Atlassian Forge (Custom UI)
- **Backend**: TypeScript, Node.js 22, @forge/api, @forge/resolver, @forge/kvs
- **Frontend**: React 18.2, Vite, Atlaskit components
- **PDF**: jsPDF (server-side generation)
- **APIs**: Jira REST API v3 (POST /search/jql), Agile API, Confluence API v2

---

## Project Structure

```
app/
  manifest.yml              # Forge manifest
  shared/types.ts           # Shared TypeScript interfaces
  src/
    index.ts                # Resolver entry point
    resolvers/              # API wrappers, export, storage
    templates/              # 7 report data assembly files
    utils/                  # Pagination, date helpers
  static/                   # React frontend (Vite)
    src/
      App.tsx               # Main shell
      components/           # UI components
      hooks/                # Custom React hooks
      utils/bridge.ts       # Typed invoke() wrappers
docs/
  TECHNICAL_DOCUMENTATION.md
  USER_GUIDE.md
  PITCH_DECK.md
```

*Built by [Luis Ivars](https://luisivars.pt) — a PM who was tired of building reports manually.*
