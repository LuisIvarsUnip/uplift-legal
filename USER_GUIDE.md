# Project Intelligence Hub for Jira - User Guide

Welcome to Project Intelligence Hub, your one-click reporting companion for Jira. This guide walks you through every feature so you can generate professional project reports in seconds, not hours.

---

## Getting Started

### How to Access

1. Open any Jira project from your Jira Cloud instance.
2. In the project navigation sidebar, click the **Project Intelligence Hub** tab.
3. You will land on the main dashboard where all report templates are available.

### First-Time Setup

Before generating your first report, take a moment to configure your settings:

1. Click the **Settings** icon (gear) in the top-right corner of the hub.
2. Fill in:
   - **Client Name** -- the name of the client or organization this project belongs to.
   - **Project Manager** -- your name (auto-detected from your Jira profile, but you can override it).
   - **Confluence Space Key** -- the default Confluence space where reports will be published.
3. Click **Save**.

That's it. You are ready to generate reports.

---

## Report Templates

Project Intelligence Hub includes seven ready-to-use report templates. Each one pulls live data from your Jira project and formats it into a polished, shareable document.

---

### 1. Weekly Status Report

**What it does**
Generates a one-click weekly snapshot of your current sprint, including progress metrics, completed work, blockers, and team activity.

**When to use it**
- Weekly stakeholder update emails
- Team standup summaries
- End-of-week project check-ins

**What is auto-populated**
- Sprint progress (percentage complete, story points burned)
- List of completed issues this week
- Open blockers and flagged items
- Team member breakdown (who worked on what)

**What you can edit**
- **RAG status** -- click the colored indicator to cycle through Red, Amber, and Green. Use this to reflect your professional judgment, not just the numbers.
- **Summary** -- add context, highlight wins, or note concerns in your own words.
- **Blocker actions** -- describe what is being done to resolve each blocker.

**Sections explained**
- **Progress** -- sprint burn-down metrics and completion percentage.
- **Highlights** -- key accomplishments and delivered items.
- **Blockers & Risks** -- anything preventing progress, with severity and owner.
- **Next Week Focus** -- upcoming priorities and planned deliverables.
- **Team** -- per-member contribution summary for the reporting period.

---

### 2. Release Notes

**What it does**
Produces an auto-categorized changelog from a specific Jira version (fix version), ready to share with clients, stakeholders, or your documentation team.

**When to use it**
- Before a software release
- When communicating changes to clients or end users
- For internal documentation of what shipped in a version

**How to use it**
1. Click **Generate** on the Release Notes template.
2. Select a **version** from the dropdown (these come from your Jira project's Releases/Versions).
3. Review and edit the generated notes.

**Categories**
Issues are automatically sorted into the following sections based on their issue type:
- **New Features** -- Stories and Epics
- **Improvements** -- Tasks and sub-tasks
- **Bug Fixes** -- Bugs
- **Security** -- Issues labeled or tagged with security
- **Breaking Changes** -- Issues flagged as breaking

**What you can edit**
- **Summary** -- a high-level overview of the release.
- **Highlights** -- the most important changes to call out.
- **Known Issues** -- problems you are aware of but did not fix in this release.
- **Migration Notes** -- steps users need to take when upgrading.
- **Technical Notes** -- details relevant to the development or ops team.

---

### 3. Project Cockpit

**What it does**
Creates an executive one-pager showing overall project health at a glance, with RAG indicators across five dimensions.

**When to use it**
- Monthly executive reviews
- Project health checks
- Portfolio-level status reporting

**Five RAG Dimensions**
Each dimension shows a Red, Amber, or Green indicator. You can click any indicator to override the calculated status.

| Dimension  | How it is calculated                                      |
|------------|-----------------------------------------------------------|
| Scope      | Based on scope change ratio and backlog growth            |
| Timeline   | Based on overdue issues and sprint completion trends      |
| Budget     | Manual entry -- you set this yourself                     |
| Team       | Based on unassigned issues and workload distribution      |
| Risks      | Based on open blockers and high-priority flagged items    |

**Key Metrics**
- Total issues in the project
- Done, In Progress, and To Do counts
- Velocity (average story points per sprint)
- Overdue issues
- Unassigned issues

**Additional Sections**
- **RAID Summary** -- a compact view of top Risks, Actions, Issues, and Decisions.
- **Quality Indicators** -- bug rate, reopen rate, and test coverage signals.
- **Delivery Forecast** -- projected completion based on current velocity.

---

### 4. RAID Log

**What it does**
Compiles a structured log of all Risks, Actions, Issues, and Decisions from your Jira project data.

**When to use it**
- Governance meetings
- Risk review sessions
- Audit and compliance reporting

**How items are identified**

| Category   | How Jira items are mapped                                  |
|------------|------------------------------------------------------------|
| Risks      | High-priority issues that are flagged                      |
| Actions    | Open tasks assigned to team members                        |
| Issues     | Open bugs and impediments                                  |
| Decisions  | Issues with a "decision" label                             |

Each item includes its priority, assignee, status, and due date (if set). Items are sorted by priority so the most critical ones appear first.

---

### 5. Steering Committee Report

**What it does**
Generates a comprehensive monthly leadership report designed for steering committee presentations.

**When to use it**
- Monthly steering committee meetings
- Executive sponsor updates
- Formal project governance reviews

**Sections**
- **Executive Summary** -- a brief overview of project status, key metrics, and overall RAG.
- **Progress** -- what was accomplished during the reporting period.
- **Accomplishments** -- major milestones reached or deliverables completed.
- **Schedule** -- timeline adherence, upcoming milestones, and any date changes.
- **Risks** -- active risks with impact assessment and mitigation plans.
- **Decision Points** -- items that require steering committee input or approval.
- **Budget** -- financial summary (populated from your manual inputs and available data).
- **Next Period** -- planned activities and focus areas for the coming month.

---

### 6. Sprint Retrospective

**What it does**
Creates a structured retrospective report using actual sprint data, giving your team a fact-based starting point for the retro conversation.

**When to use it**
- End-of-sprint retrospective meetings
- Continuous improvement tracking
- Sprint-over-sprint trend analysis

**Metrics (auto-populated)**
- **Committed vs Delivered** -- story points committed at sprint start versus actually completed.
- **Carry-over** -- issues that were not finished and rolled into the next sprint.
- **Velocity trend** -- how this sprint compares to the last several sprints.
- **Bug rate** -- percentage of sprint work that was bug-related.

**What you can edit**
- **What went well** -- add team feedback and positive observations.
- **What didn't go well** -- capture challenges, friction points, and things to improve.
- **Action items** -- specific, assignable follow-ups from the retro discussion.
- **Goal achieved toggle** -- mark whether the sprint goal was met (Yes / Partially / No).

---

### 7. Team Performance Dashboard

**What it does**
Provides cross-sprint analytics on team productivity, workload balance, and delivery health.

**When to use it**
- Quarterly team reviews
- Resource planning discussions
- Team health checks and capacity planning

**Sections**
- **Velocity Trend** -- a chart of story points delivered per sprint over time.
- **Member Performance** -- per-person breakdown of issues completed, story points, and activity.
- **Issue Type Distribution** -- what proportion of work is features vs bugs vs tasks.
- **Cycle Time** -- average time from "In Progress" to "Done" across issue types.
- **Backlog Health** -- age of backlog items, unestimated issues, and stale tickets.
- **Sprint Consistency** -- how predictable your team's delivery is sprint over sprint.

---

## Exporting Reports

Every report can be shared in three ways. Use the export toolbar at the top of any generated report.

### Copy to Clipboard

Click the **Copy** button to copy the full report with formatting preserved. You can paste it directly into:
- Google Docs
- Microsoft Outlook (email body)
- Microsoft Word
- Confluence (manual paste)

Formatting such as tables, headings, bold text, and colored RAG indicators will carry over.

### Export PDF

Click **Export PDF** to download a formatted A4 PDF file. The PDF includes:
- A professional header with project name, date, and client name
- All report sections with proper page breaks
- Your custom footer (if configured in Settings)

The file is saved to your browser's default download location.

### Push to Confluence

Click **Push to Confluence** to publish the report as a new Confluence page.

1. Select the **Confluence space** (defaults to the space you configured in Settings).
2. Optionally select a **parent page or folder** to organize the report under.
3. Click **Publish**.

A new Confluence page is created with the full report content. A link to the page is shown after publishing.

---

## Settings

Access settings from the gear icon in the top-right corner of Project Intelligence Hub.

| Setting              | Description                                                        |
|----------------------|--------------------------------------------------------------------|
| Client Name          | The client or organization name. Appears in Cockpit headers and report footers. |
| Project Manager      | Your name. Auto-detected from your Jira profile, but you can type a different name. |
| Confluence Space Key | The default Confluence space key (e.g., "PM" or "PROJ") used when pushing reports. |
| Custom Footer        | Free-text field. This text appears at the bottom of every exported report. Use it for disclaimers, confidentiality notices, or team branding. |

Settings are saved per project. Each Jira project can have its own configuration.

---

## Tips and Best Practices

- **Generate a Weekly Status Report every Friday** before sending your stakeholder update email. Copy it to clipboard and paste it directly into your email.

- **Run the Steering Committee Report at the start of each month** to prepare for governance meetings. Export it as a PDF for the meeting pack.

- **Push Release Notes to Confluence before every release** so your documentation stays current and stakeholders have a single source of truth.

- **Review the RAID Log weekly** to keep risks visible and ensure nothing falls through the cracks. Share it in your weekly risk review.

- **Use the Team Performance Dashboard quarterly** for resource planning conversations. The velocity trend and cycle time data give you objective inputs for capacity discussions.

- **Override RAG statuses when needed.** The calculated RAG is a starting point based on data, but your judgment as a PM matters. If the data says green but you know a risk is coming, set it to amber.

- **Keep your Settings up to date.** If the client name or PM changes, update it in Settings so all future reports reflect the correct information.

---

## Frequently Asked Questions

**Q: Why are some metrics showing 0?**
A: This usually means one of two things. Either your project does not have a Scrum board with an active sprint, or your issues do not have due dates, story point estimates, or fix versions set. Make sure your team is using these Jira fields consistently for the best results.

**Q: Can I use this with a Kanban project?**
A: Yes. When no sprint is detected, report templates automatically switch to a rolling window approach: 7 days for weekly reports and 30 days for monthly reports. All metrics are calculated based on this time window instead of sprint boundaries.

**Q: Why don't I see any folders when pushing to Confluence?**
A: The Confluence API cannot discover empty folders (pages without child content). If you expect to see a folder but it is missing, add at least one page to it in Confluence first, then try again.

**Q: How is RAG status calculated?**
A: RAG status is determined by a combination of factors including the overdue issue ratio, the number of open blockers, and the sprint completion rate. Green means things are on track, Amber indicates some concerns, and Red signals significant issues. You can always click a RAG indicator to override it with your own assessment.

**Q: Can multiple people on my team use the hub at the same time?**
A: Yes. Each user sees the same project data, and each user can generate their own reports independently. Settings are shared at the project level.

**Q: Do I need special permissions to use Project Intelligence Hub?**
A: You need at least "Browse Project" permission in Jira for the project you want to report on. To push reports to Confluence, you also need "Create Page" permission in the target Confluence space.

**Q: Where does the data come from?**
A: All data is pulled in real time from the Jira and Confluence REST APIs using your currently logged-in user's permissions. No data is stored outside of Jira and Confluence.

---

## Need Help?

If you run into any issues or have feedback, reach out to your Jira administrator or visit the Project Intelligence Hub support page in the Atlassian Marketplace.
