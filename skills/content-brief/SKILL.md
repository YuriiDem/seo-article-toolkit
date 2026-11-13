---
name: content-brief
description: >
  Create semantic content briefs for blog posts and articles following Koray Tugberk Gubur's framework. Use this skill whenever the user wants to create a content brief, plan an article, spec out a blog post, generate writing instructions, or prepare content specifications for a writer. Triggers on: "create a brief", "write a brief for", "plan an article about", "content brief for", "spec out a post", "article plan for", "brief this topic", "prepare a brief". Always use this skill when the user is planning what a specific article should contain, even if they don't say "brief" explicitly — if they're specifying headings, entities, or structure for a single piece of content, this is the right skill.
---

# Semantic Content Brief Generator

Create detailed semantic content briefs that operationalize a topical map into page-level writing instructions. A content brief is NOT a simple outline — it's a precise specification ensuring every article aligns with the semantic content network architecture and satisfies both NLP algorithms and user intent.

## The 67/33 Rule

Every page follows this structure:
- **Macro Context (67–75% of page)** — the core topic and main query. This is what the page is ABOUT.
- **Supplementary Context (25–33%)** — related questions, commercial bridges, FAQ sections. Supports the macro context without diluting the page's Information Retrieval (IR) score.

Stuffing pages with loosely related content dilutes the IR score. Stay disciplined.

---

## The 10 Components of a Semantic Content Brief

### 1. Page Metadata

Define upfront:
- **Target URL** (following the site's topical URL hierarchy)
- **Content type**: Pillar page vs. Cluster page
- **Intent stage**: TOFU / MOFU / BOFU
- **Word count target**: Pillar = 4,000–5,000 words; Cluster = 1,500–3,000 words
- **Central entity** for this page
- **Macro context** — the ONE primary theme (67–75% of content)
- **Supplementary context** — supporting themes (25–33%)

### 2. H1 Framework

The H1 sets the page's primary signal:
- Must contain the central entity or primary query target
- Use attribute prioritization (most important attribute first)
- Signal the main angle of the content clearly

**Example:**
- Weak: "Everything About Email Marketing"
- Strong: "Email Marketing Automation: How to Set Up Triggered Email Sequences That Convert"

### 3. Heading Vector (H2s and H3s)

The order and phrasing of headings determines how search engines understand the passage context under each heading. This comes from Google's "Context scoring adjustments for answer passages" patent.

Rules:
- **All H2s must be formatted as questions** — this is how users search and how NLP parsers identify answer passages
- **H3s** = sub-questions or supporting details under each H2
- **Order matters** — the heading sequence signals the main angle and topic progression
- **Each heading targets a specific query** from the query network

Structure the heading vector to match the frame semantics slots:
1. Identity (What is [topic]?)
2. Mechanism (How does [topic] work?)
3. Users (Who uses/needs [topic]?)
4. Selection (How do you choose [topic]?)
5. Problems (What problems does [topic] solve / what can go wrong?)
6. Outcomes (What results does [topic] deliver?)

Then add supplementary headings for FAQs, commercial bridges, and related queries.

### 4. Extractive Answer Targets

For each Question H2, specify:
- A **40-word extractive answer** that appears immediately after the heading
- Mark **"FS"** next to headings targeted for featured snippets
- Featured snippets: < 340 characters, ~40 words
- The answer must be direct, factual, no hedging — the first sentence after the heading IS the answer

**Example brief notation:**
```
## What Is Email Marketing Automation? [FS]
→ 40-word answer: Email marketing automation is the process of sending targeted email sequences triggered by subscriber actions, time intervals, or behavioral data. Automation platforms execute pre-built workflows that deliver personalized messages without manual intervention, increasing engagement rates by 70–80% compared to batch sends.
```

### 5. Target Entities and Attributes

List every Entity-Attribute-Value (EAV) triplet the article must cover:

```
Entity: Email Marketing Automation
├── Attribute: Definition → Value: automated triggered email sequences
├── Attribute: Primary platforms → Value: Mailchimp, Klaviyo, ActiveCampaign, HubSpot
├── Attribute: Key metrics → Value: open rate, click-through rate, conversion rate
├── Attribute: Common workflows → Value: welcome series, abandoned cart, re-engagement
├── Attribute: Cost range → Value: $0–$500/month for SMB
└── Attribute: Implementation time → Value: 2–4 weeks for basic setup
```

Prioritize: **Unique → Root → Rare** attributes
Score: **PPR (Prominence, Popularity, Relevance)**

### 6. 6-Source Question Generation

Generate the questions this article must answer by analyzing 6 sources:

1. **Competitor content** — what do the top 5 ranking pages cover? What questions do they answer?
2. **Query research** — what do users actually search? (People Also Ask, autocomplete, related searches)
3. **Lexical analysis** — what terms, concepts, and relationships must be covered for lexical completeness?
4. **SERP analysis** — what's in featured snippets, AI overviews, knowledge panels?
5. **Frame semantics** — which of the 6 slots (Identity, Mechanism, Users, Selection, Problems, Outcomes) need filling?
6. **Source context** — what's the brand's unique angle? What can this brand say that competitors can't?

### 7. Macro/Supplementary Structure

Map the full page structure:

```
CENTRAL ENTITY: [Topic]
├── Core Sections (Macro 67-75%):
│   ├── Definition / Identity
│   ├── Mechanism / How it works
│   ├── Benefits / Outcomes
│   ├── Selection criteria / How to choose
│   └── Usage / Implementation
├── Outer Sections (Supplementary 25-33%):
│   ├── FAQ section (FAQPage schema)
│   ├── Commercial bridges (links to product/service pages)
│   └── Related concepts (antonyms, adjacent topics)
└── Contextual Bridges:
    └── Internal link architecture (planned connections)
```

### 8. Internal Link Plan

Specify exact internal linking instructions:
- **Links FROM this page** — anchor text + target URL (max 3–15 in main content)
- **Links TO this page** — which existing pages should link here, with what anchor text
- **Contextual bridge specifications** — how each link connects semantically
- **Anchor text rules**:
  - Never use the same anchor text more than 3x site-wide
  - Never use the first word of a paragraph as anchor text
  - Use synonyms for variety
  - Anchor text must exist in the target page's content

### 9. Schema Requirements

Specify which structured data to implement:
- **Article** schema — for all posts
- **FAQPage** schema — for any Q&A sections
- **HowTo** schema — for step-by-step content
- **BreadcrumbList** schema — for topical hierarchy
- **Organization** schema enhancements — if relevant

### 10. Competitor Pages to Beat

List 3–5 specific competitor URLs that currently rank for the target queries:
- What they cover well
- What they're missing (frame semantic gaps)
- What angle or depth this article will provide that they don't

---

## Output Format

The brief should be a structured, actionable document organized as:

1. **Page Metadata** (URL, type, intent, word count, central entity)
2. **H1**
3. **Full Heading Vector** (all H2s as questions, H3s as sub-questions, with FS markers)
4. **Extractive Answers** (40-word answer for each H2)
5. **EAV Triplet List**
6. **6-Source Questions**
7. **Page Structure** (macro/supplementary split)
8. **Internal Link Map**
9. **Schema Specifications**
10. **Competitor Analysis**

When research tools are available (Ahrefs, GSC, web search), use them to build evidence-based briefs. When they're not, clearly mark assumptions and recommend validation.
