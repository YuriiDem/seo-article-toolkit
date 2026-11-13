---
name: content-audit
description: >
  Audit existing content for semantic gaps, topical coverage, frame semantics completeness, and AI citation readiness following Koray Tugberk Gubur's Content Configuration methodology. Use this skill whenever the user wants to audit existing content, check topical coverage, measure topical authority, review content for semantic gaps, perform content configuration reviews, check frame semantic completeness, assess intent distribution, or evaluate AI visibility readiness. Triggers on: "audit content", "content audit", "check topical coverage", "review existing content", "semantic audit", "content configuration", "measure authority", "coverage analysis", "what content gaps do I have", "review my blog", "what's missing from my content", "analyze my site content". Always use this skill when the user wants to evaluate their existing content — even if they phrase it as "what should I write next" (that requires understanding current gaps first) or "is my content any good" or "why isn't my content ranking".
---

# Content Audit & Configuration

Audit existing content following Koray Tugberk Gubur's Semantic Audit (Content Configuration) methodology. Content configuration is the continuous process of updating existing pages to maintain topical relevance. Every page should be audited at minimum every 6 months — adjusting headings, anchor texts, internal link priorities, and EAV coverage as search engine NLP models evolve.

---

## Part 1: Content Inventory & Classification

For each existing page or post, assess and categorize:

### Topic Cluster Assignment
Which parent theme does this page belong to? Map every page to a position in the topical map hierarchy. Pages that don't fit anywhere are candidates for removal or restructuring.

### Intent Stage Classification
| Stage | Description | Examples |
|-------|-------------|---------|
| TOFU | Awareness — educational, informational | "What is [topic]", "[topic] guide", "[topic] explained" |
| MOFU | Consideration — comparison, evaluation | "How to choose [topic]", "[A] vs [B]", "best [topic] for [use case]" |
| BOFU | Decision — buyer intent, conversion | "[Brand] vs [Competitor]", "[Competitor] alternatives", "how to [task] with [Brand]" |

### Performance Tier
- **High** — ranking well, generating traffic/conversions
- **Medium** — some impressions but underperforming potential
- **Low** — minimal visibility, few impressions
- **Dead** — zero traffic, not indexed, or cannibalized

### Action Flag
| Flag | Criteria | Action |
|------|----------|--------|
| **Keep** | Good architecture + good performance | Monitor, minor updates |
| **Salvage** | Has potential but poor structure/missing entities | Restructure with semantic writing rules |
| **Consolidate** | Thin, overlapping, or outdated | Merge with a stronger page on the same topic |
| **Remove** | No value, cannibalizing, or irrelevant | 301 redirect to most relevant page or remove |

---

## Part 2: Frame Semantics Gap Analysis

For each topic the site covers, check if ALL six semantic slots are filled. Google has a "semantic frame" for every topic — expected knowledge slots that must be present for a site to be recognized as an authority.

### Coverage Matrix

| Topic | Identity | Mechanism | Users | Selection | Problems | Outcomes | Status |
|-------|----------|-----------|-------|-----------|----------|----------|--------|
| [Topic 1] | ✅/❌/⚠️ | ✅/❌/⚠️ | ✅/❌/⚠️ | ✅/❌/⚠️ | ✅/❌/⚠️ | ✅/❌/⚠️ | Complete/Gaps |
| [Topic 2] | ... | ... | ... | ... | ... | ... | ... |

- ✅ = Covered comprehensively
- ⚠️ = Partially covered (mentioned but not deep)
- ❌ = Missing entirely

**Miss a slot = semantic gap = Google thinks "This site doesn't fully understand this topic."**

The frame semantic slots:
| Slot | Question It Answers |
|------|-------------------|
| Identity | What is it? (Definition, explanation) |
| Mechanism | How does it work? (Process, methodology) |
| Users | Who uses it? (Audience, use cases, personas) |
| Selection | How do you choose? (Comparison criteria, evaluation factors) |
| Problems | What can go wrong? (Troubleshooting, common mistakes, pitfalls) |
| Outcomes | What results does it produce? (Case studies, benchmarks, ROI data) |

---

## Part 3: Topical Coverage Assessment

Evaluate progress toward the Compounding Threshold:

- **Below 60% semantic coverage** → competing with everyone, no authority advantage
- **Above 60%** → Google treats you as default authority. New content indexes faster. Old content ranks higher. You rank for keywords you didn't target. The rich get richer.

### Assessment Questions:
1. How many parent themes in the topical map are covered vs. total needed?
2. How deep is coverage within each theme? (surface-level overview vs. comprehensive pillar + clusters)
3. Does each major theme have a pillar page?
4. Are cluster documents properly connected to their pillars?
5. What percentage of the full topical map is published?
6. What percentage of planned query templates have dedicated content?

### Coverage Score
Estimate an overall topical coverage percentage based on the gap analysis. Be specific about what's missing and what's covered.

---

## Part 4: Per-Page Quality Audit

Check each page against the core authorship rules:

### Quality Checklist (Per Page)

| Check | Question | Pass/Fail |
|-------|----------|-----------|
| Macro Context | Does the page have ONE clear primary theme? (67-75% rule) | |
| Question H2s | Are H2s formatted as questions? | |
| Extractive Answers | Is there a ~40-word answer immediately after each H2? | |
| Sentence Structure | Are sentences subject-first with short dependency trees? | |
| No Hedging | Is hedging language absent? (can, might, should, may) | |
| No Fluff | Are opinions, analogies, and filler removed? | |
| Entity Coverage | Are relevant EAV triplets present? | |
| Lexical Coverage | Are synonyms, antonyms, hyponyms, meronyms present? | |
| Schema Markup | Is appropriate structured data implemented? (Article, FAQ, HowTo, Breadcrumb) | |
| Internal Linking | Does it follow the rules? (3-15 links, anchor diversity, contextual bridges) | |

Score each page: **Strong / Needs Work / Weak / Failing**

---

## Part 5: Intent Distribution Audit

Analyze the overall content mix across the funnel:

| Intent Stage | Ideal Range | Current % | Current Count | Status |
|-------------|-------------|-----------|---------------|--------|
| TOFU | 30-40% | ?% | ? pages | Over/Under/Balanced |
| MOFU | 30-40% | ?% | ? pages | Over/Under/Balanced |
| BOFU | 20-30% | ?% | ? pages | Over/Under/Balanced |

### Common Problem Pattern
80% TOFU / 15% MOFU / 5% BOFU = optimizing for traffic, not pipeline. TOFU attracts browsers. BOFU attracts buyers. BOFU content converts at 10x the rate.

### Missing BOFU Content Types
Check for these high-converting content types:
- [ ] Competitor comparison pages ("[Brand] vs [Competitor]")
- [ ] Alternative pages ("Best [Competitor] alternatives for [use case]")
- [ ] Product-led/service-led content ("How to [task] with [Brand]")
- [ ] Integration guides
- [ ] Feature deep-dives
- [ ] Case studies with results data
- [ ] Migration guides for switchers

---

## Part 6: AI Visibility Readiness

Evaluate whether the site is positioned for AI/LLM citations:

### Entity Recognition
- [ ] Brand appears as a recognized entity (Knowledge Panel exists)
- [ ] Brand registered on Wikidata
- [ ] Consistent brand signals across the web (same name, description, identity)

### Schema & Structure
- [ ] Organization schema is comprehensive (not just basic)
- [ ] SameAs links to ALL official profiles present
- [ ] About page exists with full entity markup
- [ ] BreadcrumbList schema on all pages
- [ ] FAQPage schema on relevant pages

### Content Quality for LLMs
- [ ] Content has clear, explicit definitions (not buried in paragraphs)
- [ ] Structured hierarchies with question headings
- [ ] Original research, data, or unique frameworks present
- [ ] Content uses exact phrases users ask (query vocabulary match)
- [ ] Entity-rich content with complete EAV coverage
- [ ] Information uniqueness score (original vs. rehashed)

### AI Visibility Monitoring
- [ ] Tracking brand mentions in ChatGPT responses
- [ ] Tracking citations in Google AI Overviews
- [ ] Tracking mentions in Perplexity, Gemini, Claude, Copilot
- [ ] Monitoring which pages get cited and for which queries

### The Visibility Lag
LLMs are trained on content from 6–18 months ago. What you build now = AI visibility in 2027+. The audit should flag what needs to be built TODAY to be cited TOMORROW.

---

## Part 7: Configuration Recommendations

For each page audited, provide a prioritized action plan:

### Priority Levels
- **Critical** — page is cannibalized, has major semantic gaps, or is actively hurting the site
- **High** — page has authority potential but needs significant restructuring
- **Medium** — page is functional but missing entity coverage or lexical depth
- **Low** — minor improvements (anchor text updates, schema additions)

### Action Types
| Action | When to Use |
|--------|------------|
| Restructure headings | H2s aren't questions, heading vector is wrong |
| Add entities | Missing EAV triplets, incomplete entity coverage |
| Add schema | No structured data or incomplete implementation |
| Rewrite sentences | Hedging, passive voice, long dependency trees |
| Build contextual bridges | Missing internal link connections |
| Consolidate | Two pages competing for the same query |
| Remove | Dead page with no recovery potential |
| Create new content | Frame semantic slot is completely empty |

---

## Output Format

Produce a comprehensive audit report with:

1. **Content Inventory Table** — all pages classified by cluster, intent, performance, and action flag
2. **Frame Semantics Gap Map** — coverage matrix for all topics
3. **Topical Coverage Score** — estimated percentage with specific gaps identified
4. **Intent Distribution Analysis** — current mix vs. ideal, with specific BOFU gaps
5. **Per-Page Quality Scores** — checklist results for each page
6. **AI Visibility Readiness Score** — checklist results with specific actions
7. **Prioritized Action List** — what to fix first, ordered by impact
8. **Content Calendar Recommendations** — what to create next to fill the biggest gaps

When tools are available (Ahrefs, GSC, web search), use them to pull actual data. When they're not, clearly state which assessments are based on content review vs. data analysis.
