# AI Project Decisions

## 2026-05-01 - Split AI worklog into a reusable skill and a separate record repository

Context: The goal changed from discussing an idea to making a reusable Codex workflow that other people can install and use.

Decision: Keep the reusable workflow in `Zhanbingli/ai-worklog-skill` and keep actual work records in `Zhanbingli/ai-worklog`.

Rejected: Keeping the skill only inside `my_ebooks_YC`, because that made it look like an ebook-project artifact rather than a reusable tool.

Implication: Future work should treat `ai-worklog-skill` as the tool and `ai-worklog` as one possible output repository.

Evidence: `Zhanbingli/ai-worklog-skill` commits `3dbbbc2`, `3db771f`, and `2253ee4`.

## 2026-05-01 - Do not store raw transcripts by default

Context: Worklogs are useful for recall, public learning traces, project memory, and debugging, but raw AI conversations create privacy and noise problems.

Decision: Store concise summaries, decisions, changed files, and repository links. Exclude raw chat transcripts and long verbatim prompts unless explicit private audit logging is requested.

Rejected: Full prompt-plus-diff audit logging as the default mode, because it is too noisy and too risky for public GitHub storage.

Implication: Public records must be sanitized and marked with a privacy level. Private audit material belongs in `.ai-raw/`, which is ignored by git.

Evidence: `ai-worklog-skill` privacy labels: `public`, `project`, `private`, and `never`.
## 2026-05-01 - Add remote worklog publishing to AI worklog skill

Context: Make future AI work records publish to the dedicated ai-worklog repository without leaving local checkout files
Decision: Use https://github.com/Zhanbingli/ai-worklog.git as this installation default remote worklog repository while allowing other users to pass their own remote.
Evidence: remote worklog entry `2026-05-01 - Add remote worklog publishing to AI worklog skill`.

## 2026-05-01 - Add draft generation secret scanning and CI to AI worklog skill

Context: Make the reusable AI worklog skill lower-cost safer and easier to trust
Decision: Prioritize low-cost drafting, pre-publication scanning, and CI before adding more user-facing workflow features.
Evidence: remote worklog entry `2026-05-01 - Add draft generation secret scanning and CI to AI worklog skill`.

## 2026-05-01 - Add project scoped memory bootstrap to AI worklog skill

Context: Let future Codex sessions load only current-project memory from the remote ai-worklog repository without wasting tokens on unrelated logs
Project: ai-worklog-skill
Decision: Use project and tags fields as retrieval keys so bootstrap_memory.py can load only current-project logs and avoid wasting context on unrelated records.
Evidence: remote worklog entry `2026-05-01 - Add project scoped memory bootstrap to AI worklog skill`.

