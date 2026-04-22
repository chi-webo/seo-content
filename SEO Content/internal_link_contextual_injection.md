# Skill: internal_link_contextual_injection

## Overview
This skill enables an AI agent to inject internal links into content in a natural, context-aware manner, aligned with Google SEO best practices.

The goal is to ensure links:
- Feel natural to human readers
- Preserve content flow
- Avoid spam patterns
- Improve semantic relevance and crawlability

---

## Objectives

- Insert internal links naturally within content
- Maintain readability and writing flow
- Avoid keyword stuffing and artificial anchors
- Ensure proper link distribution across the article
- Enhance topical authority through contextual linking

---

## Hard Constraints

### 1. Link Quantity
- Minimum: 3 links per article
- Maximum: 5 links per article
- Do not exceed under any condition

---

### 2. Link Spacing
- Each link must be separated by at least 2–3 paragraphs
- Never place:
  - Multiple links in the same paragraph
  - Links in consecutive sentences

---

### 3. Anchor Text Rules

Anchor text must:
- Be naturally integrated into the sentence
- Be semantically relevant to the target page
- Read like normal text (not promotional or forced)

Avoid:
- "click here"
- "xem thêm"
- exact-match keyword stuffing

Preferred style:
- Descriptive, contextual phrases
- Semantic variations instead of exact keywords

---

### 4. Contextual Relevance

Only insert a link if:
- The surrounding content is directly related to the target page
- The link adds value for the reader

If no strong context exists:
→ DO NOT insert link

---

### 5. Content Flow Protection

Avoid placing links in:
- Introduction paragraphs
- Conclusion paragraphs
- Headings (unless necessary)

Preferred placement:
- Body content
- Explanatory sections
- Concept-expansion paragraphs

---

## Processing Logic

### Step 1: Content Segmentation
- Split content into paragraphs
- Identify semantic topics per paragraph

---

### Step 2: Link Opportunity Detection
- Find semantic matches between content and internal pages
- Prioritize:
  - Conceptual relevance
  - Topic alignment
  - Keyword proximity (secondary)

---

### Step 3: Anchor Construction
- Rewrite sentence if needed
- Ensure anchor blends naturally into context
- Avoid forced keyword insertion

---

### Step 4: Link Injection

Use standard HTML format:

<a href="/url">natural anchor text</a>

Ensure:
- Clean structure
- No JavaScript-based links
- Fully crawlable

---

### Step 5: Distribution Validation

Final checklist:

- [ ] Total links between 3–5
- [ ] No links too close together
- [ ] Each link in a separate paragraph
- [ ] No repeated anchors
- [ ] All anchors read naturally
- [ ] No SEO footprint patterns

---

## Output Format

```json
{
  "content": "...optimized content with internal links...",
  "links": [
    {
      "anchor": "...",
      "paragraph": 3,
      "reason": "contextual relevance"
    }
  ]
}