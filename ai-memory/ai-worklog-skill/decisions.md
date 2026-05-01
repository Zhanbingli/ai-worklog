# AI Project Decisions - ai-worklog-skill

## 2026-05-01 - Switch AI worklog to project scoped directories

Context: Avoid reading unrelated project logs and reduce clone size when bootstrapping memory
Project: ai-worklog-skill
Decision: Use project directories as the primary partition for worklogs and memory; keep project fields as redundant metadata and legacy fallback support.
Evidence: remote worklog entry `2026-05-01 - Switch AI worklog to project scoped directories`.

## 2026-05-01 - Harden AI worklog publishing and bootstrap

Context: Improve security stability engineering maintainability and bootstrap performance for the AI worklog skill
Project: ai-worklog-skill
Decision: Use YAML frontmatter plus ai-index/<project>.json to make records both human-readable and machine-efficient for future Codex bootstrap.
Evidence: remote worklog entry `2026-05-01 - Harden AI worklog publishing and bootstrap`.

## 2026-05-01 - Fix GitHub Actions git identity failure

Context: Make publish_worklog.py work in CI and fresh environments without global git user configuration
Project: ai-worklog-skill
Decision: Set git user.name and user.email locally inside temporary publishing repositories so CI and first-time users do not need global git identity configuration.
Evidence: remote worklog entry `2026-05-01 - Fix GitHub Actions git identity failure`.

## 2026-05-01 - Add project config and legacy migration to AI worklog skill

Context: Make the skill easier for teams to configure and migrate older worklogs into project-scoped storage
Project: ai-worklog-skill
Decision: Use .ai-worklog.json as intentional project configuration so users do not need to repeat project and remote arguments on every command.
Evidence: remote worklog entry `2026-05-01 - Add project config and legacy migration to AI worklog skill`.

## 2026-05-01 - Add worklog validation and summary rollups

Context: Make the AI worklog skill more reliable for other users and cheaper for future agents to read
Project: ai-worklog-skill
Decision: Publish should validate structured worklog records and update compact weekly/monthly summaries before pushing, so remote logs stay machine-readable by default.
Evidence: remote worklog entry `2026-05-01 - Add worklog validation and summary rollups`.

