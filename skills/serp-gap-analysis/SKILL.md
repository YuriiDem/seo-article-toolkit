---
name: serp-gap-analysis
description: Analyze the top-ranking articles for a query, build a coverage matrix, and turn gaps into concrete improvements for the user's brief, outline, or draft. Use when the user says "analyze the top results", "check the SERP", "what do competitors cover", "make my article better than the top 10", "competitor gap for this article", "SERP analysis", "проверь топ выдачи", "сравни с конкурентами", or before finalizing a brief or after a first draft.
---

# SERP Gap Analysis

Study what currently ranks for a query and make the user's article more useful than every result — by covering what readers need, adding information the top results lack, and presenting it better. Never by copying.

## Inputs

Collect (ask only for what is missing and cannot be defaulted):
- Target query (+ 2–4 close variants). Default: derive variants from the query.
- Language and market. Default: English, global/US.
- The user's material: nothing, a brief, an outline, or a draft (file path or pasted text).
- Number of results to analyze. Default: top 10 organic, minimum 5 that load.
- If a brand `*-editorial-standard` skill is installed and the topic falls within its scope, its rules override this skill.

## Hard rules

1. **Observed, not invented.** Record every SERP observation with tool, query, date, and market: "Observed via web search on YYYY-MM-DD, query '…'". A web-search tool result is not an exact personalized Google SERP — say so. Never invent rankings, search volume, difficulty, traffic, or backlink numbers.
2. **Read pages, not snippets.** Fetch each result. If a page cannot be fetched, mark it `NOT_ACCESSED` and move on; never retrieve it by other means and never describe content you did not read.
3. **No copying.** Do not reuse sentences, distinctive phrasing, structure-for-structure outlines, or proprietary checklists. Record *topics covered*, not wording. Short quotes (≤15 words) only inside the analysis to justify an observation, never in the user's article.
4. **Competitors are not sources.** A fact found in a competitor article is a lead. Trace it to the primary source; add it to the claim ledger as `UNVERIFIED` until checked.
5. **Consensus ≠ truth.** If most top results repeat a claim, that is a coverage signal, not evidence. Flag popular advice that is unsupported or potentially harmful.
6. **Beat on usefulness.** Prioritize information gain, accuracy, clarity, and safety over length. Do not recommend padding to match competitor word counts.

## Workflow

### Step 1 — Collect the SERP
- Run web searches for the main query and variants. Note features visible in results (AI answer, People Also Ask–style questions, videos, forums) only if actually observed.
- Pick the top organic articles. Skip ads, pure product pages, and duplicates; keep forums (Reddit, Quora) in a separate "community" bucket — they reveal real reader questions.
- Classify the dominant intent (informational / commercial / navigational / mixed) and format (checklist, guide, listicle, tool) from what ranks.

### Step 2 — Dissect each result
For every accessed URL record (one row per page in `serp-analysis.md`):
| Field | What to capture |
|---|---|
| URL, publisher, publisher type | gov / nonprofit / media / brand / forum |
| Title, H1 | as published |
| Outline | H2/H3 list, paraphrased topic labels |
| Answer-first? | does it answer in the first ~100 words |
| Formats | checklist, table, steps, printable, video, tool, images |
| Approx. length | rough word count; informational only |
| Entities & subtopics | key concepts covered |
| Questions answered | explicit and implicit |
| Evidence | sources cited, primary or not, dates |
| E-E-A-T signals | author, credentials, expert review, last updated |
| Unique value | what only this page offers |
| Weaknesses | outdated, vague, unsafe, unsourced, buried answer, guarantees safety, victim-blaming |

### Step 3 — Build the coverage matrix
Rows = subtopics/questions; columns = each competitor + "Ours". Mark ✔ / partial / ✘.
Then classify every row:
- **Table stakes** — covered by ≥50% of results. Missing it is a gap.
- **Differentiators** — covered by 1–2 results, clearly valuable to readers.
- **Open gaps** — reader needs (from forums, questions, fan-out, primary sources) no top result serves well.
- **Avoid** — covered by competitors but inaccurate, unsafe, outdated, or off-intent.

### Step 4 — Compare the user's material
- No material yet → produce a brief/outline addendum: required sections, differentiators to add, open gaps to own, questions for FAQ.
- Brief/outline → mark each section keep / expand / add / cut, with reason tied to the matrix.
- Draft → score it against the matrix and return section-level edits (what to add, where, why, which evidence is needed). Do not rewrite the whole article unless asked.

### Step 5 — Information-gain plan
Propose 3–7 additions that would make the article the best result, ranked by reader value and effort, e.g.:
- original assets (printable checklist, template message, decision table, "warning sign → action" matrix);
- clearer structure (answer under each heading, comparison tables, scannable steps);
- stronger evidence (primary sources competitors skip, dated and linked);
- expertise (real reviewer, first-hand operational experience — only if genuine);
- freshness (current app features, updated guidance, "Last verified" date);
- missing audience segments or scenarios.
Each item: what, why (which gap), where in the article, evidence needed, effort (S/M/L).

## Output — `serp-analysis.md`
1. Header: query, variants, market, date, tool, number of results accessed / not accessed, caveats.
2. SERP summary: dominant intent, format, typical structure, observed features.
3. Competitor table (Step 2), compact.
4. Coverage matrix with table stakes / differentiators / open gaps / avoid.
5. Assessment of the user's material (Step 4).
6. Information-gain plan (Step 5).
7. New claims to verify → list for the claim ledger, all `UNVERIFIED`.
8. One-line verdict: what the article must do to deserve to outrank the current top results.

## Re-check loop
After the user's article is revised, re-run Step 4 against the same matrix and report remaining gaps. Re-run the full analysis if the SERP is older than ~3 months.
