# OSS Scout

An AI agent for discovering emerging open-source projects worth investigating.

## Goal

Identify small, fast-growing GitHub projects with opportunities to:

- Contribute code
- Connect with maintainers and teams
- Gain experience with interesting technologies
- Potentially join an early-stage team

The goal isn't simply to find popular repositories. It's to **surface promising projects early**, before they become widely known.

## Sources

Initial discovery sources:

- [GitHub Trending](https://github.com/trending)
- [Trendshift](https://trendshift.io/)
- [Ageshio](https://ageshio.dev/)
- [Star History](https://star-history.com/)

Additional sources can be added as needed.

## Discovery Criteria

Prioritize projects exhibiting some combination of:

- **Early momentum:** Rapid recent growth relative to project size
- **Small teams:** Individual maintainers or small teams where contributions could matter
- **Active development:** Recent commits, releases, and community activity
- **Contributor accessibility:** Open issues, responsive maintainers, accepted external PRs
- **Interesting technology:** Especially AI agents, developer tooling, infrastructure, and crypto
- **Real traction:** Evidence of actual usage, adoption, or developer interest

These are guidelines, not hard filters. Avoid prematurely narrowing discovery.

## Reports

Generate concise, actionable reports that help decide which projects deserve deeper investigation.

For each promising project, include:

| Field | Description |
|---|---|
| Project | Name and GitHub URL |
| What it does | Plain-English explanation |
| Momentum | Stars, recent growth, trend |
| Team | Maintainers, contributors, project maturity |
| Opportunity | Why it might be worth investigating |
| Next step | Specific suggested action |

Prioritize signal over volume. Explain **why a project matters**, not just its metrics.

## Workflow

1. **Discover** emerging repositories from available sources.
2. **Filter** for momentum, relevance, and potential opportunities.
3. **Investigate** promising candidates using GitHub activity and project documentation.
4. **Report** a short, ranked shortlist with actionable next steps.
5. **Track** interesting projects over time to identify meaningful developments.

## Principles

- Start simple; avoid unnecessary infrastructure.
- Prefer actionable discoveries over exhaustive coverage.
- Distinguish genuine adoption from temporary hype.
- Don't assume popularity means contributor friendliness.
- Avoid repeatedly surfacing the same projects without new information.
- Keep recommendations evidence-based, with links to sources.
- Treat discovery criteria and reporting formats as experimental.

## Status

**Exploratory / MVP**

No fixed architecture, schedule, scoring system, or automation strategy yet.

Start with manual agent runs and concise reports. Refine the workflow based on which discoveries prove useful.