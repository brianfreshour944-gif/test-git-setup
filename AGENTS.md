# AGENTS.md

This repository is a test repository used to verify Git and editor
integration. Keep changes small and easy to review.

## How this repo is set up

OpenHands capabilities are configured as skills in `.agents/skills/`. Skills
load on demand when their trigger words appear, so they do not consume
context until they are needed.

| Skill | Triggers | Purpose |
| - | - | - |
| planning | plan, planning, break this down | Plan before large changes |
| security-review | security, vulnerability, secrets, owasp | Review code for flaws and leaked secrets |
| code-coverage | coverage, untested code | Run tests under coverage and find gaps |
| incident-triage | incident, triage, logs, root cause | Investigate failures and report findings |

## Conventions

- Add new skills under `.agents/skills/<name>/SKILL.md` with YAML frontmatter
  containing `name`, `description`, and `triggers`.
- Write descriptions in the third person and quote the phrases a user would
  say. This drives trigger matching.
- Prefer the existing project tooling. Install a new tool only when needed
  and with agreement.
- Never commit secrets. Never print secret values.
- Keep AGENTS.md concise; move detailed instructions into skills.
