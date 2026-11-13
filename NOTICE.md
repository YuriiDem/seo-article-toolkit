# Third-party notices

This plugin bundles skills and agents written by other authors. Each part keeps its original license and copyright. Full license texts are in [`licenses/`](licenses/).

| Upstream | License | Bundled here | License text |
|---|---|---|---|
| [rampstackco/claude-skills](https://github.com/rampstackco/claude-skills) | MIT, © 2026 RampStack Co. | `skills/content-brief-authoring` | [licenses/rampstackco-claude-skills.txt](licenses/rampstackco-claude-skills.txt) |
| [sshah03/use-citations](https://github.com/sshah03/use-citations) | MIT, © 2026 sshah03 | `skills/use-citations` | [licenses/sshah03-use-citations.txt](licenses/sshah03-use-citations.txt) |
| [TheSmokeDev/geo-skills](https://github.com/TheSmokeDev/geo-skills) | MIT, © 2026 SmokeDev | the `geo*` skills and other skills from that repo, plus agents `geo-ai-visibility`, `geo-content`, `geo-platform-analysis`, `geo-schema`, `geo-technical` | [licenses/TheSmokeDev-geo-skills.txt](licenses/TheSmokeDev-geo-skills.txt) |
| [bartmagera/claude-skills](https://github.com/bartmagera/claude-skills) | Published here with the author's permission | `skills/content-brief`, `semantic-writer`, `content-audit`, `full-site-audit`, `topical-map`, `entity-optimizer`, `internal-linking` | — |
| claude-seo (Bhanu Namikaze, agricidaniel), via bartmagera/claude-skills | MIT, © 2026 Bhanu Namikaze, agricidaniel | code in `skills/full-site-audit` that comes from claude-seo | [licenses/claude-seo-agentic-seo.txt](licenses/claude-seo-agentic-seo.txt) |
| [lyndonkl/claude](https://github.com/lyndonkl/claude) | Published here with the author's permission | `skills/research-claim-map` | — |

Own work by Yuri, under the MIT license in [`LICENSE`](LICENSE): `skills/serp-gap-analysis`, `agents/serp-analyst.md`, and the plugin packaging (manifests, README, path rewrites to `${CLAUDE_PLUGIN_ROOT}`). That license does not cover the bundled third-party parts listed above.

Changes made to bundled skills: hardcoded `~/.claude/skills` paths were rewritten to `${CLAUDE_PLUGIN_ROOT}/skills`.

If you are an upstream author and want your work credited differently or removed, open an issue.
