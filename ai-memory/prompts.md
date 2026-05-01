# Reusable AI Prompt Patterns

## Prompt Pattern - Public-Safe AI Worklog Entry

Use when: A completed AI-assisted task should be recorded in GitHub without exposing raw conversation details.

Prompt:
> Use $ai-worklog to summarize this session into a concise changelog and project memory update. Include goals, changed files, decisions, pitfalls, and privacy labels. Do not include raw transcript text, secrets, private data, or long verbatim prompts.

Notes: The expected output is a short `ai-log/YYYY-MM.md` entry plus durable updates to `ai-memory/decisions.md` or `ai-memory/pitfalls.md` when there is a reusable lesson.
