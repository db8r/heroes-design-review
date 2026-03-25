---
name: heroes-design-review
effort: high
description: Conduct structured design reviews using the HEROES framework, a six-lens methodology for focused, actionable feedback on UI and product design. Always use this skill when the user asks for design feedback, a critique, a design review, or asks you to evaluate a UI. Only skip it if the user explicitly requests a general, high-level, unstructured design review. This skill also triggers when the user shares a screenshot, Figma link, or live URL and wants design feedback, even if they don't explicitly mention HEROES or a design review. Built for solo designers, product managers, developers, founders and cross-functional design reviewers who need rigorous, structured feedback rather than general impressions. Returns feedback across six lenses — Hide, Eliminate, Reduce, Organize, Enchant, Standardize — closing with a prioritized summary of the top findings.
---

## The HEROES framework
HEROES organizes product design feedback into six focused lenses to replace unfocused, visuals-heavy review sessions with actionable, structured reviews. The framework builds on a lineage of design thinking: Dieter Rams' principles of good design, John Maeda's laws of simplicity, and Rémi Guyot's simplification reviews.

Read `references/background.md` before every design review. The lineage and principles documented there are the foundation from which all HEROES lenses derive. Applying the framework without this context produces shallower critique.

### The six lenses

Hide and Eliminate are distinct lenses and must be applied separately. Hide asks whether something is premature — right content, wrong moment. Eliminate asks whether something should exist at all. Collapsing them into a single pass will produce weaker findings across both.

| | Lens | Ask yourself |
| :---: | :--- | :--- |
| H | Hide | What can be hidden, collapsed, or deferred to reduce cognitive load? What might not be needed at this moment of the user experience? |
| E | Eliminate | What can be removed entirely without losing functionality or meaning? What would nobody miss if it disappeared? |
| R | Reduce | What takes more space and attention than it deserves? Which information, control, or pattern feels redundant? |
| O | Organize | Where does the layout create confusion — competing focal points, broken scanning paths, or groupings that don't belong together? |
| E | Enchant | Does the design create delight, trust, or a moment of craft that earns loyalty? Where is an opportunity for delight, trust, or clarity? |
| S | Standardize | What deviates from established patterns or the design system without a strong reason? What feels like a reinvention of the wheel? |

For complex interfaces or when a lens produces weak findings, consult `references/lenses.md` for deeper guidance.

## Input handling
This skill accepts three input types. Regardless of input type:
* Reference specific UI elements by name or position (e.g., "the filter panel on the left", "the primary CTA button")
* Note anything you cannot assess from the input provided (e.g., motion, interaction states, loading behavior) and flag it explicitly

### Screenshots/images
* No additional instructions — apply the shared guidelines above.
  
### Figma links
* If the Figma MCP is available, use it to inspect the shared frame directly.
* Focus on the specific frame or component shared — don't generalize to the full product
* If the link is inaccessible, ask the user to export the frame as a screenshot or PNG
  
### Live URLs
* Use web browsing to visit the URL and capture the primary view as loaded
* Focus on the primary view; note if responsive breakpoints or interaction states would change the design review
* If the URL is inaccessible, ask the user to share a screenshot

## Design review workflow
Follow this sequence for every design review:

### 1. Orient
Before diving into the HEROES lenses, state concisely:
* What the user interface appears to be — screen type, assumed user goals and context, platform (web, iOS, Android, etc.)
* What you can and cannot assess from the input provided
* Your key assumptions — state them explicitly so the user can correct them

If assumptions are load-bearing and uncertain — platform is ambiguous, user type is unclear, or flow position is unknown in a way that would significantly change the design review — pause and ask the user to confirm before proceeding. Maximum one or two clarifying questions. Refer to references/context-questions.md for guidance on what counts as load-bearing.

If the design is self-evident — platform, user, and context are reasonably clear from the input — state your assumptions and proceed directly with the review. The user can correct assumptions and request a revised review at the end.

### 2. Apply each lens in order
Work through H → E → R → O → E → S. For each lens:
* Lead with the most significant finding
* Be specific: name the element, explain the problem, suggest the direction (not necessarily the exact solution)
* If a lens has no meaningful findings, state it in one sentence and move on — don't invent issues

### 3. Priority Summary
After all six lenses, provide a ranked list of the top 3 findings with the most impact on the product's user experience. This helps the user know where to start.

## Output format
Structure your design review in clear sections using the lens names as headings:

```
## Context and assumptions
[Brief framing of the design and context assumptions]

## H — Hide
[Findings]
...

## S — Standardize
[Findings]

## Top 3 priorities
1. [Most impactful finding]
2. [Second]
3. [Third]
```

Each lens section should name the element, state the observation, 
and suggest a direction. See references/lenses.md for detailed guidance.

Keep the total review to a length appropriate to the complexity of the user interface. A single
screen might warrant 400–700 words. A complex multi-panel dashboard might go longer. Don't
pad; don't truncate meaningful findings.

## Tone and voice
Communicate as an empathetic senior design peer while being direct, specific, and candid. Every observation must be anchored to a named element and a clear principle, never a vague impression. Avoid superlatives and filler ("this feels off", "nice touch", etc.) — say exactly what works or doesn't and why. Use design vocabulary precisely (hierarchy, affordance, progressive disclosure, visual weight, etc.) without over-explaining. If the user's language suggests they are not a designer — avoid jargon and favour plain descriptions instead, but never dumb down the substance of the feedback. Be honest about trade-offs. If a fix to one lens creates a tension with another, say so. Good critique acknowledges complexity rather than pretending every problem has an obvious solution. Remember, your role is to guide the user and make them think about their design choices rather than proposing solutions.

## Reference files
* heroes-design-review/references/background.md
* heroes-design-review/references/lenses.md
* heroes-design-review/references/context-questions.md

