# AI Project Pitfalls

## 2026-05-01 - A skill is not enough unless the first-use path is obvious

Symptom: The initial skill described the workflow, but a new user still had to infer how to initialize a project, append entries, and create weekly summaries.

Cause: The first version relied too much on Codex interpretation and not enough on deterministic helper scripts.

Fix: Add `init_project.py`, `append_worklog.py`, and `weekly_context.py`, then document the install, initialize, daily log, and weekly review flow in README.

Avoid: Shipping workflow ideas without a one-command first step and a clear maintenance path.

Evidence: `Zhanbingli/ai-worklog-skill` commit `2253ee4`.

## 2026-05-01 - Do not let temporary work become local cache

Symptom: Publishing records can leave cloned repos, generated caches, or raw materials on the local machine.

Cause: Git-based publishing often requires a local working directory unless using an API-only flow.

Fix: Use `/private/tmp` for transient assembly, push the sanitized result, and remove temporary directories after upload.

Avoid: Keeping raw transcript files, local audit folders, or generated caches after the GitHub upload is complete.
