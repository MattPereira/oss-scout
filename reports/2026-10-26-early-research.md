# Candidate research — 2026-10-26

Supplemental investigation for the ranked shortlist. Counts are GitHub API snapshots; seven-day growth is Ageshio's earlier snapshot, so denominators differ. Stars show attention, not verified adoption. Contributor counts were unavailable through the connected endpoint; named contributors and merged PRs below are evidence, not team-size estimates.

| Candidate | Current stars / language | Seven-day momentum | Contribution signal | Suggested investigation |
|---|---|---|---|---|
| [Beacon](https://github.com/Asymptote-Labs/agent-beacon) | 2,864 / Go | +34%; 56.9× previous week's pace | External contributor fixes merged Oct 26; detailed contribution guide | Try local Codex capture; inspect collector consistency around #973 |
| [DS Harness Remote](https://github.com/liguobao/ds-harness-remote) | 880 / TypeScript | +54%; 6.4× previous week's pace | External mobile and reconnect fixes merged Oct 26 | Reproduce #177 mobile question submission failure |
| [Open Ontologies](https://github.com/fabio-rovai/open-ontologies) | 1,466 / Rust | +21%; 5.9× previous week's pace | Named project lead; multiple external fixes merged Oct 23 | Reproduce #334 custom severity namespace loss |

Momentum source: [Ageshio gaining pace, Oct 26](https://ageshio.dev/). Current metadata: [Beacon API](https://api.github.com/repos/Asymptote-Labs/agent-beacon), [Remote API](https://api.github.com/repos/liguobao/ds-harness-remote), [Open Ontologies API](https://api.github.com/repos/fabio-rovai/open-ontologies).

## Beacon

Captures coding-agent sessions across harnesses and turns useful history into shared memory. Integrates Codex, Cursor and Claude Code; Go core with TypeScript/browser surfaces. Repository created May 12; pushed Oct 26; MIT. [README](https://github.com/Asymptote-Labs/agent-beacon/blob/main/README.md), [metadata](https://api.github.com/repos/Asymptote-Labs/agent-beacon).

Strongest evidence of accessibility: contributor `rudycelekli`'s [#1070](https://github.com/Asymptote-Labs/agent-beacon/pull/1070) (preserve commented Codex config sections) and [#1071](https://github.com/Asymptote-Labs/agent-beacon/pull/1071) (Codex shell telemetry) merged Oct 26. [Closed PR records](https://api.github.com/repos/Asymptote-Labs/agent-beacon/pulls?state=closed&sort=updated&direction=desc&per_page=15).

Open [#973](https://github.com/Asymptote-Labs/agent-beacon/issues/973) documents duplicated sync helpers across 17 collectors and observable behavior differences. Larger refactor: discuss a narrow first slice before implementing. [#974](https://github.com/Asymptote-Labs/agent-beacon/issues/974) offers an alternative correctness investigation: cloned Hermes profiles collide on event IDs, with migration constraints.

The [contribution guide](https://github.com/Asymptote-Labs/agent-beacon/blob/main/CONTRIBUTING.md) welcomes AI-assisted work, gives per-module checks and several contribution surfaces. Best fit inference: agent tooling plus integration debugging, with demonstrated acceptance of small fixes. Caveat: substantial repository and retained session data make real local testing important; team headcount unverified.

## DS Harness Remote

Independent community project for continuing local coding-agent sessions from desktop, browser and mobile; encrypted transport and several agent backends. Created Aug 14; pushed Oct 26. [README](https://github.com/liguobao/ds-harness-remote/blob/main/README.en.md), [metadata](https://api.github.com/repos/liguobao/ds-harness-remote).

GitHub's root license field is null, but the README links an actual [MIT license](https://github.com/liguobao/ds-harness-remote/blob/main/packages/plugin/LICENSE); [package.json](https://github.com/liguobao/ds-harness-remote/blob/main/package.json) also declares MIT.

Owner `liguobao`; external contributors include `dreamfarer-space`, `bluesmilery` and `xiongyuyang`. [#173](https://github.com/liguobao/ds-harness-remote/pull/173), reconnect recovery, and [#174](https://github.com/liguobao/ds-harness-remote/pull/174), Android file attachments, merged Oct 26. [Closed PR records](https://api.github.com/repos/liguobao/ds-harness-remote/pulls?state=closed&sort=updated&direction=desc&per_page=10).

Open [#177](https://github.com/liguobao/ds-harness-remote/issues/177) reports mobile question answers cannot submit and identifies the RPC mismatch. Reproduce against current main, then trace client-to-host response routing. [#178](https://github.com/liguobao/ds-harness-remote/issues/178) concerns excessive foreground reconnections. These user reports provide usage evidence beyond stars; neither is independently reproduced here.

Best fit inference: TypeScript, agent protocols, distributed connection state and mobile UX. Caveat: device/host setup; much issue discussion is Chinese. Do not select old [#97](https://github.com/liguobao/ds-harness-remote/issues/97) as an unimplemented Pi feature: current README already documents experimental Pi support.

## Open Ontologies

Rust CLI/MCP engine that plans and checks knowledge-graph changes, with semantic reports and proof machinery. Created Mar 9; pushed Oct 26; MIT. [Repository](https://github.com/fabio-rovai/open-ontologies), [metadata](https://api.github.com/repos/fabio-rovai/open-ontologies).

[CONTRIBUTORS.md](https://github.com/fabio-rovai/open-ontologies/blob/main/CONTRIBUTORS.md) names Fabio Rovai as project lead and describes outside contributors, including a production user. External [#328](https://github.com/fabio-rovai/open-ontologies/pull/328) and [#297](https://github.com/fabio-rovai/open-ontologies/pull/297) merged Oct 23. [Closed PR records](https://api.github.com/repos/fabio-rovai/open-ontologies/pulls?state=closed&sort=updated&direction=desc&per_page=15).

Owner-opened [#334](https://github.com/fabio-rovai/open-ontologies/issues/334) is a bounded entry point: custom SHACL severity loses its namespace. Reproduce W3C `severity-002`, preserve the declared RDF term through JSON/report comparison, and add a regression. Adjacent [#333](https://github.com/fabio-rovai/open-ontologies/issues/333) concerns datatype false negatives and is more involved.

[Contribution guide](https://github.com/fabio-rovai/open-ontologies/blob/main/CONTRIBUTING.md) supplies architecture, Rust checks, plus no-Rust extension paths through ontology packs, workflow recipes and companion MCP servers. Best fit inference: deeper infrastructure/formal methods learning and direct maintainer interaction. Caveat: specialist RDF/SHACL learning curve; lower direct relevance than agent tooling.
