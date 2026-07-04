# Contributing to Innovation-Lab

**Principle:** This is a space for battle-tested patterns, not theoretical frameworks. Every contribution should be grounded in lived experience, real projects, and evidence.

---

## What We Accept

### ✅ Contributions We Want

- **Patterns from real projects** — "We built X for Y population; here's what worked"
- **Blindspot analyses** — "We discovered exclusion for Z group; here's how we fixed it"
- **Representative testing reports** — Feedback from people with lived experience
- **Data governance frameworks** — Public sector data sharing patterns
- **Accessibility patterns** — Screen reader testing, keyboard nav, assistive tech insights
- **Neurodiverse design patterns** — ADHD-friendly UX, autism-aware patterns, anxiety-safe flows
- **Agent engineering** — New skills, personas, orchestration patterns
- **Improvements to existing patterns** — Refinements based on new evidence

### ❌ We Don't Accept

- Theoretical frameworks without evidence
- Frameworks that haven't been tested with real users
- Patterns that don't include accessibility/equity by default
- Contributions that don't consider neurodiversity
- "Best practices" without blindspot analysis
- Anything that claims to work for "everyone" without naming exclusions

---

## Before You Contribute

### 1. Check for Interconnections

**Is your work related to:**
- cyberdudeuk's repos (co-cddo, gds-dtx, ndl-pubsec-mcp)?
- Cross-government data standards?
- Public sector citizen-facing systems?
- DEIA, accessibility, or neurodiversity?

If yes: Flag it in your PR. Link to related work. We'll coordinate and avoid duplication.

### 2. Gather Evidence

Every pattern needs:

| Evidence | Required? | Example |
|----------|-----------|---------|
| Real project | Yes | "Built for [system]; served [population]" |
| Blindspot analysis | Yes | "Discovered exclusion for X; why it happened; how we fixed it" |
| Representative testing | Yes (citizen-facing) | "Tested with 3 blind users; 2 ADHD users; 1 Deaf user" |
| Test report | Yes | "X users completed task; Y users encountered barrier; here's the fix" |
| Code/example | Recommended | "Here's the pattern in production" |
| Measurement | Recommended | "Before/after: accessibility defects down 60%; support calls down 40%" |

### 3. Ensure Equity & Inclusion

**Before submitting, ask:**

- [ ] Have I named the served population explicitly (not "users")?
- [ ] Have I conducted a blindspot analysis for at least 2 groups?
- [ ] Have I tested with people from those groups (not just automated checks)?
- [ ] Does this pattern include accessibility by default (not bolted-on)?
- [ ] Have I considered neurodiversity (ADHD, autism, PTSD, anxiety)?
- [ ] Is plain language used (Flesch-Kincaid Grade ≤8)?
- [ ] Could someone neurodiverse understand this without re-reading?
- [ ] Have I flagged what this pattern *doesn't* solve?

If you can't check all boxes, that's okay—open a draft PR and we'll help.

---

## How to Contribute

### For Patterns & Skills

1. **Create a new branch:**
   ```bash
   git checkout -b pattern/your-pattern-name
   ```

2. **Use this template:**

   ```markdown
   # Pattern: [Name]
   
   **Context:** What's the problem you're solving?  
   **Served population:** Who is this for? (Be specific)  
   **Blindspots solved:** What exclusion did you find + fix?
   
   ## The Pattern
   [Step-by-step instructions; code examples; diagrams]
   
   ## Evidence
   - Real project: [X system; Y population]
   - Representative testing: [3 blind users, 2 ADHD users; results]
   - Measurement: [Before/after metrics]
   
   ## What This Doesn't Solve
   [Be honest: what's out of scope?]
   
   ## Testing
   [How to verify this works; automated checks; manual steps]
   ```

3. **Include:**
   - Clear, actionable steps
   - Code examples (if applicable)
   - Blindspot analysis table
   - Representative testing results (summary, not raw data)
   - Links to related work (agent-skills, cyberdudeuk repos, GDS standards)

4. **File structure:**
   ```
   your-pattern/
   ├── PATTERN.md          # Main document
   ├── examples/           # Code/config examples
   ├── testing-report.md   # Summary of rep testing
   └── related-work.md     # Links to interconnected projects
   ```

5. **Submit a PR:**
   - Link to any related issues
   - Mention if this connects to cyberdudeuk's work or cross-gov initiatives
   - Summary: "This pattern serves X population; fixes Y exclusion; tested with Z"

### For Accessibility/Neurodiversity Improvements

1. **If you found a blindspot:**
   - Open an issue: "Pattern X excludes Y population because Z"
   - Include: How you found it, evidence, proposed fix

2. **If you have representative testing data:**
   - Create `testing-reports/` directory in the pattern folder
   - Include: Participant profile (anonymized), task, observation, fix

3. **If you want to add a new neurodiversity pattern:**
   - Use the template above
   - Include ADHD/autism/PTSD/anxiety-specific insights
   - Test with at least 3 people with lived experience

### For Data Architecture / Governance

1. **Document your framework:**
   - Problem: What government/data sharing problem does this solve?
   - Context: Which population/dept does it serve?
   - Schema: Data model, fields, validation rules
   - Governance: Who owns it? How is it maintained?
   - Privacy: What's minimized? Why?

2. **Link to:**
   - NDL (National Data Library) alignment
   - DCAT-UK AP (metadata standard)
   - GDS Way / Service Standard
   - Related cyberdudeuk work (if applicable)

3. **Include:**
   - Example dataset (anonymized)
   - Edge cases (what breaks it?)
   - Audit trail (how is it governed?)

---

## Code of Conduct

### We Require

- **Respect for lived experience.** If someone with lived experience says "this excludes me," listen. Don't argue.
- **No ableism.** Don't use language like "disabled people are expensive" or "edge case." Reframe: "This population has different access needs; here's how we serve them."
- **Nothing About Us Without Us.** If your pattern serves a population, involve people from that population in design + testing.
- **Transparency.** Be honest about limitations, blindspots, and what you don't know.
- **Collaboration over competition.** Link to related work. Flag overlaps with cyberdudeuk's projects. We're building shared infrastructure.

### We Don't Tolerate

- Dismissing accessibility as "nice to have"
- Assumptions that accessibility = higher cost (it doesn't if designed in)
- Language that others or dehumanizes people with disabilities, neurodivergence, or low income
- Patterns that "work for 90%" without naming the 10% you excluded
- Refusing to test with real assistive tech users

---

## Review Process

### Step 1: Automated Checks
- [ ] Markdown is clean (no broken links, headers, formatting)
- [ ] Files follow naming convention (`pattern-name`, `PATTERN.md` or `SKILL.md`)
- [ ] License header included (MIT for code; OGL for docs)

### Step 2: Evidence Review
- [ ] Real project documented (not hypothetical)
- [ ] Blindspot analysis included
- [ ] Representative testing report provided (or rationale for why not yet)
- [ ] Code examples work (if applicable)
- [ ] Links to related work checked

### Step 3: Equity Audit
- [ ] Served population named explicitly
- [ ] Accessibility considered (WCAG 2.2 AA minimum)
- [ ] Neurodiversity patterns included
- [ ] Plain language used
- [ ] No ableist language

### Step 4: Interconnection Check
- [ ] Links to cyberdudeuk's work where relevant
- [ ] Cross-referenced with GDS Service Standard
- [ ] Flagged if it overlaps with existing patterns

### Step 5: Approval
- Minimum 1 core maintainer + 1 community reviewer (person with lived experience from served population, if applicable)

---

## Questions?

- **How do I find representative testers?** See `docs/recruiting-representatives.md`
- **What does "blindspot analysis" look like?** See `docs/blindspot-template.md` + examples in existing patterns
- **How do I measure success?** See `docs/measurement-framework.md`
- **I'm neurodivergent—should I contribute?** YES. Your lived experience is expertise. Patterns you design for yourself serve millions.
- **Can I contribute if I'm not a developer?** YES. We need UX designers, accessibility auditors, people with lived experience, policy experts, community reps.

---

## Maintenance

### Pattern Lifecycle

| Stage | Owner | Action |
|-------|-------|--------|
| **Proposed** | Contributor | Submit PR; pass automated checks |
| **Under Review** | Maintainer + Community | Evidence audit; equity check; interconnection review |
| **Approved** | Maintainer | Merge to main; tag as `v1` |
| **In Use** | Community | Real projects test it; report bugs; suggest improvements |
| **Stable** | Maintainer | Annual review; update if blindspots found |
| **Deprecated** | Maintainer | If better pattern emerges; mark `[DEPRECATED]`; link to replacement |

### Reporting Issues

Found a blindspot in a pattern? Open an issue:

```markdown
**Pattern:** [Name]  
**Exclusion:** [This pattern doesn't work for X population because Y]  
**Evidence:** [How you found it; who told you; test result]  
**Proposed fix:** [What should change]
```

---

## Recognition

Contributors are listed in:
- Pattern README (author + date)
- Annual report (aggregate contribution)
- Alongside their GitHub profile (with permission)

If your pattern is co-designed with community, we list them too (with their consent).

---

## License

By contributing, you agree your work is licensed:
- **Code:** MIT
- **Documentation:** Open Government Licence v3.0

© 2026 — individual contributions; collective impact.
