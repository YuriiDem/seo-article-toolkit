# SEO Article Toolkit

Bundle of community skills for producing high-quality SEO/GEO articles.

| Source | Skills |
|---|---|
| rampstackco/claude-skills (MIT) | content-brief-authoring |
| bartmagera/claude-skills | content-brief, semantic-writer, content-audit, full-site-audit, topical-map, entity-optimizer, internal-linking |
| lyndonkl/claude | research-claim-map |
| sshah03/use-citations (MIT) | use-citations |
| TheSmokeDev/geo-skills (MIT) | all 29 skills under skills/ + 5 agents |
| Yuri (own) | serp-gap-analysis + serp-analyst agent |

Suggested article pipeline: topical-map → content-brief / content-brief-authoring → research-claim-map → semantic-writer → use-citations → geo-citability / geo-content → internal-linking.

Notes: bartmagera's `agentic-seo` was skipped (duplicate of full-site-audit). Hardcoded `~/.claude/skills` paths were rewritten to `${CLAUDE_PLUGIN_ROOT}/skills`. token-max-factory needs an external CLI (Archon) that it asks to install via a shell script — review before running.
