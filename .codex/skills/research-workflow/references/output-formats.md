# Output Format Specifications

## 1. Executive Summary Format

Use when: User needs a quick decision-support briefing.
Length: 200–400 words.

```markdown
## Executive Summary: [Topic]

**Bottom line:** [Single sentence most important finding]

**Context:** [1–2 sentences on why this matters]

**Key Findings:**
- Finding 1 (🟢 High confidence)
- Finding 2 (🟡 Medium confidence)
- Finding 3 (🔴 Low confidence — needs verification)

**Recommended Action:** [Specific next step]

**Caveats:** [Key limitations of this research]
```

---

## 2. Full Research Report Format

Use when: Comprehensive documentation is required.
Length: 800–2000 words.

Sections (in order):
1. Executive Summary
2. Key Findings (grouped by theme)
3. Consensus Points
4. Areas of Conflict
5. Gaps Identified
6. Recommendations
7. Key Takeaways
8. Sources Reviewed
9. Limitations

See `assets/research-report-template.md` for the full template.

---

## 3. Action Items Format

Use when: User needs practical next steps, not background knowledge.
Length: 100–200 words.

```markdown
## Action Items: [Topic]

**Immediate (this week):**
- [ ] Action 1
- [ ] Action 2

**Short-term (this month):**
- [ ] Action 3

**For further investigation:**
- Open question 1
- Open question 2

**Key insight behind these actions:**
[One sentence explaining the most important finding that drove these recommendations]
```

---

## Formatting Rules (All Formats)

- Use markdown headers for all section titles
- Use tables for comparisons (3+ items)
- Use bullet points for lists of 3+ items
- Confidence emojis: 🟢 High | 🟡 Medium | 🔴 Low
- Always cite sources with `[Source Name](URL)` format
- End every output with at least one actionable recommendation
