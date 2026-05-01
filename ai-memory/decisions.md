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
