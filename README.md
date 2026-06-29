# AEPDEMO

This project was scaffolded by Agentic Engineering.

Every folder below holds a specific class of artifact produced (or consumed)
by the agent pipeline. The structure is the source of truth - replacing the
old SQLite store - so each artifact change is a git commit.

## Folder map

| Folder | Contents |
|---|---|
| `00-project-home/` | Project dashboard, RAID log, pending decisions, customer/PS actions |
| `01-source-documents/` | Raw uploaded documents + classifications + extractions |
| `02-workshop-plan/` | Workshop plans, series, agendas, completed feedback |
| `03-discovery/` | BRD, personas, current-state analysis, integrations |
| `04-requirements/` | Epics + individual requirements (REQ-XXX/) with stories + tests |
| `05-journey-maps/` | Customer/user journey maps |
| `06-design/` | Functional design, data model, wireframes, mockups |
| `07-architecture/` | Integration topology, security, scalability, ADRs |
| `08-build/` | Sprint reports, sandbox prototypes, deployments |
| `09-test/` | Project-wide test plan, UAT strategy, defects |
| `10-change-management/` | Change plan, training plan, rollout plan |
| `11-pipeline-runs/` | History of every agent pipeline run (inputs + outputs) |
| `12-feedback/` | User feedback - one folder per entry, structured for fine-tuning |
| `.agentic/` | Tool-managed metadata (personas, decisions, audit log) |

## Conventions

- **Markdown** for human-readable narrative (`.md`)
- **YAML** for structured data (`.yml`)
- **Attachments** for binaries (images, PDFs) - tracked via Git LFS
- **One file per item** where collaboration is likely (user stories,
  test cases, personas) - keeps merges conflict-free
- **Numbered prefixes** (`00-`, `01-`, ...) preserve order in file listings

## Branching

Each user works on a persona-named branch (e.g. `persona/sa-1-solution-architect`).
Merges to `main` happen only via the auto-merge GitHub Actions workflow.

Project created: 2026-06-29T06:17:35.447220+00:00
Created by: rdhandia@salesforce.com
Git URL: https://github.com/ritikadhandia/AEP-DEMO
