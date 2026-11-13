---
name: entity-optimizer
description: >
  Optimize entities, map entity-attribute-value relationships, build lexical coverage, and prepare content for AI citations following Koray Tugberk Gubur's framework. Use this skill whenever the user wants to optimize entities in content, map entity relationships, build lexical coverage, analyze EAV triplets, plan Knowledge Panel strategy, optimize schema markup, or prepare content for LLM/AI citations. Triggers on: "optimize entities", "entity mapping", "lexical coverage", "EAV analysis", "knowledge panel", "schema optimization", "AI citation optimization", "entity analysis", "map entities for", "lexical depth", "entity attributes". Always use this skill when the user mentions entities, lexical relationships, or AI visibility optimization — even if they phrase it casually like "make sure Google understands what this page is about" or "optimize for AI".
---

# Entity Optimizer

Perform comprehensive entity optimization ensuring content has complete Entity-Attribute-Value coverage and deep lexical relationships. This is what separates authority content from generic content — and what makes LLMs cite you as a trusted source.

## Why Entity Optimization Matters

Google and LLMs don't rank pages — they rank **entities they trust on topics**. If Google doesn't understand what you are, who you serve, and what topics you own, you're competing against everyone for everything. Entity optimization builds the semantic signals that establish trust.

---

## Part 1: Entity-Attribute-Value (EAV) Mapping

For the given topic or content, build the complete EAV map:

### Process:
1. **Identify the Central Entity** — the primary subject
2. **Map ALL attributes** of that entity
3. **Prioritize**: Unique → Root → Rare
   - **Unique** = only this entity has this attribute (highest value)
   - **Root** = fundamental, defining characteristics
   - **Rare** = uncommon but differentiating
4. **Score using PPR**: Prominence, Popularity, Relevance
   - **Prominence** = how visible/important is this attribute in the topic space?
   - **Popularity** = how often do users search for or reference it?
   - **Relevance** = how closely does it relate to the central entity?

### Output structure:
```
Central Entity: [Entity Name]
├── Attribute: [name] → Value: [value] | Priority: Unique/Root/Rare | PPR: H/M/L
├── Attribute: [name] → Value: [value] | Priority: Unique/Root/Rare | PPR: H/M/L
├── Attribute: [name] → Value: [value] | Priority: Unique/Root/Rare | PPR: H/M/L
└── ...
```

List EAV triplets exhaustively. Incomplete coverage = incomplete authority signal.

---

## Part 2: Lexical Coverage Analysis (17 Relationship Types)

This is the deepest layer of entity optimization. For every central entity, map ALL 17 lexical relationship types. No lexical depth = no authority signal.

### 1. Synonyms
Alternative terms for the same concept.
> "SEO" → "search engine optimization", "organic search optimization", "search optimization"

### 2. Antonyms
Opposite concepts that define boundaries.
> "organic traffic" → "paid traffic", "ad spend", "PPC"

### 3. Hyponyms
Specific subtypes (narrower terms).
> "SEO" → "technical SEO", "local SEO", "on-page SEO", "off-page SEO", "enterprise SEO"

### 4. Co-hyponyms
Sibling concepts under the same parent category.
> "SEO", "PPC", "content marketing", "social media marketing" → all under "digital marketing"

### 5. Hypernyms
Broader parent categories (wider terms).
> "SEO" → "digital marketing" → "marketing" → "business strategy"

### 6. Meronyms
Part-of relationships (components).
> "SEO" → "keyword research", "link building", "technical audit", "content optimization", "site architecture"

### 7. Holonyms
Whole-of relationships (what this is part of).
> "keyword research" is part of → "SEO"; "SEO" is part of → "digital marketing strategy"

### 8. Troponyms
Manner-specific verbs (how actions are performed).
> "optimize" → "audit", "crawl", "index", "rank", "canonicalize", "render"

### 9. Collocations
Naturally co-occurring word pairs.
> "search volume", "domain authority", "crawl budget", "index coverage", "click-through rate"

### 10. Metonyms
Associated substitutions (using one term to mean another).
> "the algorithm" meaning "Google's ranking system"; "the SERPs" meaning "search results page"

### 11. Polysemy Awareness
Words with multiple meanings requiring disambiguation.
> "authority" = domain authority vs. topical authority vs. brand authority
> "index" = search index vs. database index vs. stock market index
> "bounce" = email bounce vs. website bounce rate

### 12. Taxonomic Siblings
Entities at the same classification level.
> "Google", "Bing", "DuckDuckGo", "Yahoo" → under "search engines"

### 13. Functional Relations
Cause/effect or tool/purpose pairs.
> "link building" → "higher domain authority"; "page speed optimization" → "better Core Web Vitals"

### 14. Gradable Relations
Spectrum/scale terms showing progression.
> "new site" → "established site" → "authority site" → "market leader"

### 15. Derivational Relations
Morphologically related word forms.
> "optimize" → "optimization", "optimized", "optimizer", "optimizing"

### 16. Domain-Specific Jargon Mapping
Technical terms mapped to plain language equivalents.
> "canonical tag" → "URL preference signal"; "hreflang" → "language targeting markup"

### 17. Associative Relations
Contextually linked but not taxonomically related.
> "SEO" associates with "Google Analytics", "Search Console", "CMS", "conversion rate", "content strategy"

---

## Part 3: Named Entity Recognition (NER) Check

Review content for proper entity handling:

1. **Entity completeness** — are all relevant entities mentioned?
2. **Entity qualification** — is each entity mentioned with descriptive context? (Don't just name-drop, qualify)
3. **Entity disambiguation** — are entities specified clearly to avoid confusion?
   - Bad: "Schwartz discusses this" (which Schwartz?)
   - Good: "Barry Schwartz, the search engine optimization journalist, discusses this"
4. **Coreference clarity** — no ambiguous pronouns when multiple entities share gender/type
5. **Entity consistency** — same entity referred to consistently throughout

---

## Part 4: Knowledge Panel & AI Citation Strategy

### Knowledge Panel Establishment
- Is the brand registered on Wikidata?
- Does Organization schema include comprehensive attributes?
- Are SameAs links pointing to ALL official profiles? (LinkedIn, Twitter/X, Crunchbase, Wikipedia, etc.)
- Is there a dedicated About page with full entity markup?
- Are brand searches generating a Knowledge Panel?

### How LLMs Choose Sources to Cite

| Factor | What Matters | How to Optimize |
|--------|-------------|-----------------|
| Entity Recognition | Are you a known entity in training data? | Knowledge Panel, Wikidata, consistent entity signals |
| Semantic Structure | Clear hierarchies, explicit definitions, schema | Question H2s, 40-word answers, structured data |
| Information Uniqueness | Original research > rehashed content | Proprietary data, unique frameworks, case studies |
| Query Vocabulary | Using exact phrases users ask | Match natural query language in headings and answers |

### The Visibility Lag
LLMs are trained on content from 6–18 months ago. What you build now = AI visibility in 2027+. Competitors building authority today will own AI search tomorrow.

### AI Citation Optimization Checklist:
- [ ] Clear, explicit definitions (not buried in paragraphs)
- [ ] Structured hierarchies with question headings
- [ ] Original data, statistics, or frameworks
- [ ] Entity-rich content with EAV triplets
- [ ] FAQ sections with schema markup
- [ ] Consistent brand entity signals across the web

---

## Part 5: Schema Markup Recommendations

For each content piece, specify required schema:

- **Article** schema — every post
- **FAQPage** schema — any Q&A sections (these get extracted by LLMs)
- **HowTo** schema — step-by-step content
- **BreadcrumbList** — topical hierarchy signals
- **Organization** schema — with full entity details and SameAs links
- **Person** schema — for author pages (E-E-A-T signals)

---

## Output Format

When optimizing entities for a piece of content, produce:

1. **Central Entity & Complete EAV Map** — all attributes with priority and PPR scores
2. **Lexical Coverage Map** — all 17 relationship types filled out
3. **NER Checklist** — entity completeness, disambiguation, coreference checks
4. **Knowledge Panel / AI Citation Recommendations** — specific actions to take
5. **Schema Markup Specifications** — exact schema types and key properties
6. **Gap Analysis** — what's missing from current content, prioritized by impact
