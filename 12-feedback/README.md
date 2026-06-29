# Feedback

User feedback about how the tool performed for this project.

Every entry lives in its own folder named `FB-XXX-<slug>/` and contains:

- `feedback.yml` - structured fields (ratings, tags, target area/agent).
  Designed as fine-tuning input - keep the schema stable.
- `description.md` - free-form prose written by the submitter.
- `context.yml` - auto-captured runtime context (current tab, recent agent
  activity, browser info) so triage doesn't need to chase the submitter.
- `attachments/` - screenshots or other files uploaded with the report.

The catalogue lives in `feedback-index.yml` for quick listing without
walking every folder.

## Submitting

Use the floating **Feedback** button in the app, or POST directly to
`/api/feedback`. The service is implemented in `app/feedback_service.py`.

## Statuses

`open` -> `acknowledged` -> `in_progress` -> `resolved` | `wont_fix`

## GitHub issues (optional)

When the submitter ticks "Also file as GitHub issue", a matching issue is
created in the repo configured by `FEEDBACK_GITHUB_REPO` (env var). The
issue URL is recorded back on the entry.
