---
name: internal-linking
description: >
  Plan and optimize internal linking using contextual bridges, anchor text strategy, and hub-and-spoke architecture following Koray Tugberk Gubur's methodology. Use this skill whenever the user wants to plan internal links, create contextual bridges between content, optimize anchor text strategy, audit internal link structure, plan hub-and-spoke linking, review link density, or connect articles together. Triggers on: "plan internal links", "internal linking strategy", "contextual bridges", "anchor text plan", "link structure", "hub and spoke links", "link audit", "connect these articles", "how should I link these", "linking strategy", "link these posts". Always use this skill when the user is discussing how pages should connect to each other, even casually — like "should this post link to that one?" or "how do I connect my content?"
---

# Internal Linking Optimizer

Plan and optimize internal linking following Koray Tugberk Gubur's contextual bridge methodology. Internal links pass relevance and topic-sensitive PageRank — but ONLY when properly structured with contextual bridges. Without a proper bridge, links don't pass relevance regardless of how many you add.

---

## Link Classification

Every link on a page falls into one of three categories. Understanding this determines where to invest linking effort.

### S-nodes (Structural/Navigational)
Links repeated across multiple pages for navigation — header menus, footer links, sidebar widgets. These are the LEAST valuable because they appear everywhere and carry minimal contextual signal.

### C-nodes (Content Block)
Block links within the main content area. These carry more contextual relevance because they sit within the page's primary content.

### I-nodes (Individual/Contextual)
Individual links embedded in contextually relevant paragraphs. No similar neighbor links nearby. These carry the HIGHEST contextual relevance and are the most valuable for passing topical authority.

**Strategy:** Maximize I-nodes. Minimize S-nodes. Koray's case studies ranked sites with NO header or footer navigation (logo only in header), pushing ALL link weight to main content I-nodes.

---

## Link Density Rules

Based on tested case studies that achieved rankings without backlinks:

- **3–15 links maximum** per page in main content
- Tested successfully: **3 contextual links** in main content + 5 sidebar links (latest articles) + 1 homepage link in header + 1 homepage link in footer = ~10 total
- **All internal link weight should go to main content links**
- More links = diluted weight per link
- Fewer, higher-quality contextual links outperform many generic links

---

## Anchor Text Rules

These rules prevent over-optimization penalties and ensure natural anchor text distribution:

1. **Never use the same anchor text more than 3 times site-wide.** For the 4th instance, change or add words. Synonyms and variations prevent over-optimization.

2. **Never use the first word of a paragraph as anchor text.** This looks unnatural and can trigger pattern detection.

3. **Never use text from the first paragraph of a page as anchor text linking TO that page.** The first paragraph sets the page's context — using it as anchor text elsewhere creates circular signals.

4. **Supplementary content links go in the last heading's paragraphs.** If linking to a page from a different context or side-topic, place the link in one of the final sections. Google classifies these as "Supplementary Content" links.

5. **Check competitor anchor texts** for the same target page/topic. Understand the anchor text landscape before choosing yours.

6. **Use synonyms** when creating anchor texts. Vary the phrasing across different linking pages.

7. **Anchor text must exist in the target page's content** AND in the linking page's related heading text. This creates a semantic bridge between the two documents.

8. **Anchor text must be descriptive** and match the target page's macro context. Generic anchors like "click here" or "read more" waste linking potential.

---

## Contextual Bridges

This is the most important concept in internal linking. A contextual bridge is the semantic connection between two documents that allows an internal link to actually pass relevance.

### What Makes a Valid Contextual Bridge

For a link to transfer topical relevance, the source and target documents must share:
- **Matching phrase patterns** — similar vocabulary and terminology
- **Shared predicates** — same or related verbs/actions
- **Connected nouns and adjectives** — overlapping entity references
- **Aligned query semantics** — both documents serve queries in the same network

### The Bridge Formula

The contextual bridge between two documents comes from the intersection of:
- **Source context** (the brand's identity and angle)
- **Contextual domain** (the topic area both documents belong to)

If two documents don't share a contextual domain intersection, the link between them won't pass meaningful relevance — no matter how perfect the anchor text is.

### How to Build a Bridge

1. Identify the shared topical territory between the source and target page
2. Write a sentence or paragraph in the source page that naturally introduces the target page's topic
3. The bridge text should use vocabulary that exists on BOTH pages
4. Place the anchor text within this bridge paragraph
5. The bridge should feel like a natural extension of the current section's discussion

**Example:**
- Source page: "Technical SEO Audit Guide"
- Target page: "Core Web Vitals Optimization"
- Bridge: "A comprehensive technical audit evaluates page performance metrics. Core Web Vitals represent three specific performance measurements that Google uses as ranking signals." → anchor on "Core Web Vitals" linking to the target.

### Without a proper contextual bridge, internal links can't pass relevance or PageRank in the context of topic-sensitive PageRank iterations.

---

## Hub-and-Spoke Architecture

The overall internal linking structure follows a hub-and-spoke model:

### Hubs (Pillar Pages)
- Link TO all cluster pages in their topic group
- Receive links FROM all cluster pages
- Act as the central authority document for a parent theme
- Hub pages can also aggregate and summarize cluster topics

### Spokes (Cluster Pages)
- Link BACK to their pillar page
- Link TO relevant sibling cluster pages (within the same topic group)
- May link to cluster pages in adjacent topic groups via contextual bridges

### Architecture Rules
- **Every page connects** to at least one hub — zero orphan pages
- **Implement breadcrumb schema** to signal the topical hierarchy
- **Remove or consolidate orphan pages** — pages with no internal links pointing to them
- **Cross-cluster links** require stronger contextual bridges since they span topic boundaries

---

## Internal Link Audit Process

When auditing existing internal links, check these 7 areas:

### 1. Orphan Pages
Pages with zero internal links pointing to them. These are invisible to the link graph and waste crawl budget. Fix: connect to relevant hub or sibling page.

### 2. Link Density
Flag pages with:
- **>15 main content links** — diluting link weight
- **0–1 links** — not contributing to the semantic network

### 3. Anchor Text Diversity
Flag any anchor text used more than 3 times site-wide. Map all anchor texts to identify over-optimization patterns.

### 4. Contextual Bridge Quality
For each internal link, verify:
- Does the surrounding text create a semantic bridge?
- Does the anchor text exist in the target page's content?
- Is the link in an I-node position (contextual) or S-node position (navigational)?

### 5. S-node Ratio
Pages with too many navigational links relative to contextual links. Header/footer links should be minimal to avoid diluting main content link weight.

### 6. Hub-and-Spoke Gaps
- Are all clusters connected to their pillar?
- Are pillar pages linking to all their clusters?
- Are there broken connections in the hub-and-spoke architecture?

### 7. Supplementary Content Placement
Links to different-context pages should appear in the final sections (supplementary content area), not in the first paragraphs (macro context area).

---

## Output Format

### For PLANNING Internal Links

Produce a link map document with:

1. **Link Map Table**
   | Source Page | Anchor Text | Target Page | Bridge Context | Placement |
   |-----------|-------------|-------------|----------------|-----------|
   | [URL] | [anchor] | [URL] | [bridge justification] | [which section] |

2. **Anchor Text Alternatives** — 2–3 synonym variations per link
3. **Bridge Paragraphs** — draft bridge text for each link
4. **Link Density Check** — total links per page after additions
5. **Hub-and-Spoke Diagram** — visual representation of the connection architecture

### For AUDITING Internal Links

Produce an audit report with:

1. **Orphan Page List** — pages with no incoming internal links
2. **Over-Linked Pages** — pages exceeding 15 main content links
3. **Under-Linked Pages** — pages with 0–1 internal links
4. **Duplicate Anchor Text Violations** — anchors used >3x site-wide
5. **Missing Contextual Bridges** — links without proper bridge context
6. **Hub-and-Spoke Gap Analysis** — missing connections in the architecture
7. **Prioritized Fix List** — ordered by impact (orphan pages first, then bridge gaps, then density issues)
