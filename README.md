# SEO Article Toolkit

A Claude Code plugin that helps you plan, write, fact-check and audit articles for Google and for AI search (ChatGPT, Perplexity, Gemini, Google AI Overviews).

It bundles about 40 skills and 6 agents. Most come from other authors (credited below). Each skill is a set of instructions Claude follows for one job, such as building a content brief or checking a page's SEO.

## Install

In Claude Code:

```
/plugin marketplace add YuriiDem/seo-article-toolkit
/plugin install seo-article-toolkit@yuriidem
```

Or from a terminal:

```bash
claude plugin marketplace add YuriiDem/seo-article-toolkit
claude plugin install seo-article-toolkit@yuriidem
```

## How to use it

You don't need to remember skill names. Ask Claude in plain words, and it picks the right skill:

> Build a topical map for a blog about home coffee brewing.

> Write a content brief for "how to descale a coffee machine".

> Check the top 10 Google results for this query and tell me what my draft is missing.

To run a specific skill, name it: `use seo-article-toolkit:semantic-writer to rewrite draft.md`. The `use-citations` skill only runs when you type `/use-citations`.

## Writing an article, step by step

Use the steps you need. Each one gives you something concrete to work with.

| Step | Ask for | You get |
|---|---|---|
| 1. Plan the topic | `topical-map` | A map of everything your site should cover on the topic: pillar pages, supporting articles, the questions people search, and what to publish first. |
| 2. Plan the article | `content-brief` or `content-brief-authoring` | A brief for one article: target query, search intent, H1 and all headings, a short answer for each section, key facts to include, internal links and schema to add. |
| 3. Study the competition | `serp-gap-analysis` (or the `serp-analyst` agent) | A `serp-analysis.md` file: what the top results cover, what they miss, what your article must add to beat them, and a list of claims to verify. |
| 4. Check the facts | `research-claim-map` | Each claim rated by evidence quality and source credibility, with a confidence level, so weak or unsupported statements are caught before publishing. |
| 5. Write | `semantic-writer` | The finished article, written to clear rules for search engines and AI, plus a checklist of covered entities and suggested links and schema. |
| 6. Quote sources | `/use-citations` | Answers drawn from a set of documents you give it, with every quote checked against the source, and a report a reviewer can check. |
| 7. Make it citable by AI | `geo-citability`, `geo-content` | A 0–100 score for how likely AI assistants are to quote the page, plus specific passages to rewrite. |
| 8. Link it in | `internal-linking` | A table of which pages should link to the new article and from where, with anchor text options and short bridge paragraphs. |

## Auditing a site or page

| Ask for | You get |
|---|---|
| `seo-audit`, `full-site-audit` | A list of SEO problems on a site or page, ordered by priority, with fixes. |
| `geo-audit` | A full check of how ready a site is for AI search, run by several agents in parallel. |
| `geo-technical`, `geo-crawlers` | Crawling, indexing, speed and AI-crawler access issues (robots.txt, headers). |
| `geo-schema`, `schema-markup` | Missing or broken structured data, and ready-to-paste JSON-LD. |
| `content-audit` | Gaps in topic coverage across your existing articles. |
| `geo-report`, `geo-report-pdf` | A client-ready report (Markdown or PDF) built from the audit results. |

Other skills cover content strategy, site structure, comparison pages, programmatic pages at scale, llms.txt, brand mentions and YouTube.

## Credits and licenses

| Source | Skills |
|---|---|
| [rampstackco/claude-skills](https://github.com/rampstackco/claude-skills) (MIT) | content-brief-authoring |
| [bartmagera/claude-skills](https://github.com/bartmagera/claude-skills) | content-brief, semantic-writer, content-audit, full-site-audit, topical-map, entity-optimizer, internal-linking |
| [lyndonkl/claude](https://github.com/lyndonkl/claude) | research-claim-map |
| [sshah03/use-citations](https://github.com/sshah03/use-citations) (MIT) | use-citations |
| [TheSmokeDev/geo-skills](https://github.com/TheSmokeDev/geo-skills) (MIT) | the other 29 skills and 5 agents |
| Yuri (MIT, see [LICENSE](LICENSE)) | serp-gap-analysis, serp-analyst agent, plugin packaging |

The [LICENSE](LICENSE) file covers only Yuri's own work. Bundled parts keep their original licenses: see [NOTICE.md](NOTICE.md), with full texts in [`licenses/`](licenses/).

## Notes

- Hardcoded `~/.claude/skills` paths in bundled skills were changed to `${CLAUDE_PLUGIN_ROOT}/skills` so they work inside the plugin.
- `token-max-factory` needs an external CLI (Archon) and asks to install it with a shell script. Read the script before running it.
