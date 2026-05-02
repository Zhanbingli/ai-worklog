# AI Project Pitfalls - ai-worklog-skill

## 2026-05-01 - Switch AI worklog to project scoped directories

Symptom: Month-level global files force bootstrap to scan unrelated project logs, wasting tokens and increasing the risk of irrelevant context.
Project: ai-worklog-skill
Cause: Not specified.
Fix: See linked worklog entry.
Evidence: remote worklog entry `2026-05-01 - Switch AI worklog to project scoped directories`.

## 2026-05-01 - Harden AI worklog publishing and bootstrap

Symptom: Regex-only Markdown parsing is fragile over time; stable ids and compact indexes reduce parsing ambiguity and token use.
Project: ai-worklog-skill
Cause: Not specified.
Fix: See linked worklog entry.
Evidence: remote worklog entry `2026-05-01 - Harden AI worklog publishing and bootstrap`.

## 2026-05-01 - Fix GitHub Actions git identity failure

Symptom: GitHub Actions runners may not have git author identity, causing git commit to fail even when worklog generation and scanning succeed.
Project: ai-worklog-skill
Cause: Not specified.
Fix: See linked worklog entry.
Evidence: remote worklog entry `2026-05-01 - Fix GitHub Actions git identity failure`.

## 2026-05-01 - Add project config and legacy migration to AI worklog skill

Symptom: Changing storage layouts without a migration path leaves older logs hard to retrieve; keep migration additive and non-destructive.
Project: ai-worklog-skill
Cause: Not specified.
Fix: See linked worklog entry.
Evidence: remote worklog entry `2026-05-01 - Add project config and legacy migration to AI worklog skill`.

## 2026-05-01 - Add worklog validation and summary rollups

Symptom: Future agents waste context if bootstrap only reads raw monthly logs; read ai-index and ai-summary before detailed entries.
Project: ai-worklog-skill
Cause: Not specified.
Fix: See linked worklog entry.
Evidence: remote worklog entry `2026-05-01 - Add worklog validation and summary rollups`.

## 2026-05-02 - Remove personal default worklog remote

Symptom: A hard-coded maintainer remote in a reusable skill creates privacy and ownership risk because other users may accidentally publish records to the wrong repository.
Project: ai-worklog-skill
Cause: Not specified.
Fix: See linked worklog entry.
Evidence: remote worklog entry `2026-05-02 - Remove personal default worklog remote`.

