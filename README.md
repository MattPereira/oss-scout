# OSS Scout

Agent skills for finding open-source projects to contribute to, adopt, or learn from. Works in Claude Code and Codex.

## Usage

Run from this repo. Skills only fire when you call them.

| Command                               | Does                                                                  |
| ------------------------------------- | --------------------------------------------------------------------- |
| `/oss-discover-early`                 | Small, rising repos to contribute to → `reports/DATE-early.md`        |
| `/oss-discover-breakout`              | High-momentum projects to adopt or learn → `reports/DATE-breakout.md` |
| `/oss-contribute <repo or issue URL>` | Contribution strategy for a chosen target                             |

Typical loop: run `oss-discover-early`, pick a row from the report, pass its repo or issue to `oss-contribute`.

## Customize

- Interests and stack: [`INTERESTS.md`](INTERESTS.md)
- Sources, criteria, report columns: each skill's `SKILL.md` in `.agents/skills/` (`.claude/skills` symlinks there)
