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

---

## Getting Started

### Prerequisites
- Node.js 22+
- Atlassian Forge CLI (`npm install -g @forge/cli`)
- Atlassian Cloud dev tenant ([get one free](https://go.atlassian.com/cloud-dev))

### Install & Deploy
```bash
cd app
npm install
cd static && npm install --legacy-peer-deps && npm run build && cd ..
forge login
forge register
forge deploy
forge install --site YOUR-SITE.atlassian.net --product jira
forge install --site YOUR-SITE.atlassian.net --product confluence -e development
```

### Development
```bash
cd app/static && npm run build && cd .. && forge deploy
```

For live debugging:
```bash
forge tunnel
```

---

## Permissions

| Scope | Reason |
|-------|--------|
| read:jira-work | Read issues, sprints, versions for reports |
| read:jira-user | Read current user name for report headers |
| read:board-scope:jira-software | Access Scrum/Kanban boards |
| read:project:jira | Access project metadata |
| read:sprint:jira-software | Read sprint data and history |
| read:space:confluence | List Confluence spaces |
| write:page:confluence | Create Confluence pages |
| read:page:confluence | List pages for parent selection |
| read:folder:confluence | List folders for page placement |
| storage:app | Store project settings |

---

## Documentation

- [Technical Documentation](docs/TECHNICAL_DOCUMENTATION.md) — Architecture, APIs, development guide
- [User Guide](docs/USER_GUIDE.md) — How to use each template
- [Pitch Deck](docs/PITCH_DECK.md) — Marketing presentation

---

## Versioning

- **v1.0.0** — MVP with 3 templates (Weekly Status, Release Notes, Project Cockpit)
- **v2.0.0** — 7 templates + enhanced existing + RAID, Steering Committee, Sprint Retro, Team Dashboard

---

## License

Proprietary. All rights reserved.

---

*Built by [Luis Ivars](https://luisivars.pt) — a PM who was tired of building reports manually.*
