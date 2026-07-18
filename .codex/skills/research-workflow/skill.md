---
name: research-workflow
description: >
  Guide agents through structured research including planning, multi-query
  execution, source analysis, and synthesis. Use for comprehensive topic
  research, deep investigation, or creating research reports.
  Keywords: research, investigate, deep dive, comprehensive, analysis,
  synthesis, report.
license: MIT
compatibility: Designed for Claude Code and similar products. Web search capability required.
author: sakshamonwork-gif
version: "1.1"
---

# Research Workflow Skill

A structured methodology for conducting **comprehensive, multi-phase research**.
This skill transforms Claude from a single-shot search tool into a disciplined
research analyst that plans, executes, critiques, and synthesises.

---

## When to Use

**Use this skill when:**
- The user needs comprehensive research on a topic
- Multiple search queries are needed to fully answer a question
- Source credibility and synthesis matter
- A research report or documented findings are expected
- Keywords mentioned: *research, investigate, deep dive, comprehensive analysis*

**Do NOT use this skill when:**
- A single quick search will suffice
- The user wants a simple fact lookup
- No synthesis or analysis is needed

---

## Research Phases Overview

```
┌─────────────────────────────────────────────────────────┐
│                   RESEARCH WORKFLOW                     │
├─────────────────────────────────────────────────────────┤
│                                                         │
│  1. PLANNING          2. EXECUTION                      │
│  ┌────────────┐       ┌────────────┐                    │
│  │ Define     │       │ Run multi- │                    │
│  │ questions  │──────>│ ple queries│                    │
│  │ Plan scope │       │ Eval srcs  │                    │
│  └────────────┘       └────────────┘                    │
│        │                    │                           │
│        v                    v                           │
│  3. ANALYSIS          4. SYNTHESIS                      │
│  ┌────────────┐       ┌────────────┐                    │
│  │ Organise   │       │ Write      │                    │
│  │ findings   │──────>│ coherent   │                    │
│  │ Patterns   │       │ report     │                    │
│  └────────────┘       └────────────┘                    │
└─────────────────────────────────────────────────────────┘
```

---

## Phase 1 — Planning

### Step 1: Define the Research Question
Convert the topic into specific, answerable sub-questions.

> **Example — Topic:** "AI in healthcare"
> - What are the current applications?
> - What are the main benefits and challenges?
> - What regulations govern AI in healthcare?
> - What are the latest developments (last 6 months)?

### Step 2: Identify Sub-Topics
Break the main topic into searchable components:
- Core concepts and definitions
- Current state and applications
- Benefits and advantages
- Challenges and limitations
- Recent developments
- Future trends

### Step 3: Plan Search Strategy
| Round | Query Type | Purpose |
|-------|-----------|--------|
| 1 | Broad overview | Landscape mapping |
| 2 | Specific deep-dive | Detailed evidence |
| 3 | Verification / critic | Challenge assumptions |
| 4 | Recency | Latest news / data |

Minimum **4 queries** per research session.

---

## Phase 2 — Execution

### Step 1: Run Searches in Sequence
```
# Round 1 — Broad
web-search "[topic] overview guide"

# Round 2 — Specific
web-search "[topic] [specific aspect] case study"

# Round 3 — Critic
web-search "[topic] criticism limitations challenges"

# Round 4 — Recency
web-search "[topic] latest news [current year]"
```

### Step 2: Document Each Search
For every query, capture:
- Query used
- # results reviewed
- Key findings (2–3 bullets)
- Notable sources
- New questions raised

### Step 3: Evaluate Sources
For each source, check:

**Credibility Indicators**
- [ ] Author / organisation has domain expertise
- [ ] Published in reputable outlet
- [ ] Date is recent enough for the topic
- [ ] Cites primary sources or data

**Quality Signals**
- [ ] Evidence-based claims
- [ ] Multiple perspectives considered
- [ ] Methodology is clear
- [ ] Peer-reviewed or editorially reviewed

### Step 4: Iterate
Research is non-linear. Based on findings:
- Add queries for gaps discovered
- Verify surprising or counter-intuitive claims
- Explore unexpected connections

---

## Phase 3 — Analysis

### Step 1: Group by Theme
Organise raw notes into:
1. Core concepts
2. Current state
3. Benefits / opportunities
4. Challenges / risks
5. Recent developments
6. Expert opinions

### Step 2: Identify Patterns
| Pattern Type | Question to Answer |
|---|---|
| **Consensus** | Where do multiple authoritative sources agree? |
| **Conflict** | Where do sources disagree? Why? |
| **Gap** | What important questions remain unanswered? |
| **Trend** | What direction is the field moving? |

### Step 3: Assign Confidence
- 🟢 **High** — Multiple authoritative sources agree
- 🟡 **Medium** — Some evidence, limited sources
- 🔴 **Low** — Single source or conflicting information

### Step 4: Note Limitations
- What couldn't be found (paywalled, not yet indexed)
- Areas needing expert consultation
- Potential source bias

---

## Phase 4 — Synthesis

### Step 1: Choose Output Format
| Use Case | Format |
|---|---|
| Executive decision | Executive summary (½–1 page) |
| Full documentation | Research report (structured sections) |
| Next steps focus | Action items + recommendations |

### Step 2: Write the Synthesis
Principles:
1. Lead with the most important finding
2. Connect related concepts explicitly
3. Note confidence levels inline
4. Acknowledge limitations honestly
5. Cite sources for every key claim

### Step 3: Deliver Actionable Elements
Every research output must end with:
- **Key Takeaways** (3–5 bullets)
- **Recommendations** (specific, actionable)
- **Further Research** (open questions)
- **Decision Points** (what this research should inform)

---

## Quality Checklist

Before marking research complete:
- [ ] Clear research questions were defined upfront
- [ ] Minimum 4 queries executed
- [ ] Sources evaluated for credibility
- [ ] Findings organised by theme
- [ ] Consensus, conflicts, and gaps noted
- [ ] Confidence levels assigned
- [ ] Limitations documented
- [ ] Output is actionable

---

## Complete Worked Example

**Topic:** Best practices for API versioning

**Phase 1 — Plan:**
```
Sub-questions:
1. What versioning strategies exist?
2. Pros/cons of each strategy?
3. What do major companies use?
4. Expert recommendations?

Search Plan:
- "API versioning strategies comparison"
- "REST API versioning best practices 2026"
- "API versioning URL vs header vs query parameter"
- "API versioning major companies GitHub Stripe Twilio"
```

**Phase 2 — Execute (summary):**
| Query | Key Finding | Source Quality |
|---|---|---|
| strategies comparison | 3 main types: URL, header, query param | 🟢 High |
| best practices 2026 | Version only on breaking changes | 🟢 High |
| URL vs header | No universal winner; URL more discoverable | 🟡 Medium |
| major companies | Stripe: URL; GitHub: header; Twilio: URL | 🟢 High |

**Phase 3 — Analysis:**
- **Consensus:** Only version on breaking changes; document lifecycle
- **Conflict:** URL vs header versioning (no clear winner)
- **Gap:** Limited data on developer experience UX impact

**Phase 4 — Synthesis:**
> 🟢 **Finding 1:** URL versioning is the most discoverable and widely adopted approach (Stripe, Twilio, AWS).
> 🟡 **Finding 2:** Header versioning is considered architecturally purer but less accessible to new developers.
> 🟢 **Finding 3:** All major providers agree: only introduce a new version for breaking changes.

**Recommendations:**
1. Use URL versioning for public-facing APIs
2. Use semantic versioning principles (MAJOR.MINOR.PATCH)
3. Publish a clear deprecation timeline (minimum 12 months)
4. Automate version detection in CI/CD pipelines

---

## Limitations

- Quality depends on available web search tool
- Cannot access paywalled or restricted content
- Time-intensive — not suitable for quick lookups
- Very recent events may not yet be indexed

---

## Related Skills
- `web-search` — execute individual searches (used inside this workflow)
