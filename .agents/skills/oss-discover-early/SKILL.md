---
name: oss-discover-early
description: Find small, fast-growing open-source repos worth contributing to; writes a ranked shortlist report.
disable-model-invocation: true
---

Surface small repos early, before they are widely known, where an outside contribution would matter.

## Sources

- [Ageshio](https://ageshio.dev/) (gaining-pace list)
- [OSS Radar](https://ossradar.net/)
- [Trendar](https://trendar.org/)
- [GitDiscover](https://gitdiscover.org/)

## Criteria

Rank on a combination; guidelines, not filters:

- **Early momentum**: fast recent growth relative to size
- **Small team**: solo or small maintainer group
- **Active**: recent commits, releases, issue activity
- **Contributor access**: open unassigned issues, merged external PRs, responsive maintainers
- **Interest fit**: `INTERESTS.md` at repo root
- **Real traction**: usage evidence beyond stars

## Steps

1. Read prior `reports/*-early.md`; a repo already listed returns only with news (release, growth spike, new contributable issue).
2. Pull candidates from every source.
3. Verify finalists on GitHub: stars, recent merges, open issues.
4. Write `reports/YYYY-MM-DD-early.md`: ranked table, columns Project (name + URL), What it does, Momentum, Team, Opportunity, Next step. Explain why each matters, not just metrics; link evidence.
