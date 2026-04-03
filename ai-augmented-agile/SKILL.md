---
name: AI-Augmented Agile
description: This skill should be used when the user asks about "AI in agile", "using ChatGPT for scrum", "AI-assisted retrospectives", "AI metrics", "AI sprint planning", "AI coaching", "AI ethics in teams", "AI surveillance", "AI performance tracking", "prompt engineering for agile", "AI-generated reports", "deep research for agile", "AI backlog analysis", "AI estimation", "custom GPT for teams", "AI tool selection", "AI transparency", "AI hallucination risk", "AI verification", "AI-augmented coaching", or wants guidance on integrating AI tools into agile practices ethically and effectively.
version: 1.0.0
---

# AI-Augmented Agile Practices

Integrating AI tools (ChatGPT, Claude, Copilot, Gemini, custom GPTs) into agile practice creates significant opportunity and significant risk. The core principle: **AI amplifies human insight; it does not replace it.** When the relationship inverts — humans validating AI outputs rather than AI assisting human judgement — the practice has failed.

This skill links to:
- **`scrum`** — Sprint events where AI may be applied
- **`agile-metrics`** — Metrics AI can generate or misinterpret
- **`agile-coach`** — Coaching stance when AI is involved
- **`facilitation`** — Facilitating sessions with AI-generated inputs
- **`continuous-improvement`** — Using AI in improvement cycles

---

## Core Principles

1. **Human judgement over AI output** — AI produces hypotheses, not conclusions. Every AI output requires human interpretation, contextualisation, and validation before acting on it.

2. **Verify before presenting** — Never present AI-generated data, metrics, or analysis to stakeholders without independent verification. If a calculation cannot be reproduced or explained, do not use it.

3. **Transparency about AI use** — Teams and stakeholders must know when AI was involved in producing analysis, recommendations, or artifacts. Hidden AI use erodes trust.

4. **Consent before processing** — Team data (retrospective notes, Slack messages, code commits) must not be processed by AI without explicit, informed consent from every individual. Company ownership of data does not equal consent for AI analysis.

5. **AI assists the process, not replaces it** — The value of agile ceremonies comes from human dialogue, shared understanding, and collective ownership. AI that pre-digests conclusions eliminates the collaborative sense-making that creates buy-in.

---

## AI in Scrum Ceremonies

### Sprint Planning
- AI-drafted Sprint Goals serve as starting points, not final outputs. The team must refine and commit to the goal together — ownership requires participation, not passive acceptance.
- Time pressure does not justify skipping team refinement of AI-generated goals. A few minutes of collaborative shaping prevents an entire Sprint of misalignment.

### Sprint Review
- Do not automate Sprint Review slide generation from Jira data. If the team spends 2 hours preparing presentations, the underlying problem is treating the Review as presentation theatre rather than stakeholder collaboration. Fix the format (show working software, invite dialogue) before considering AI assistance.
- AI-generated reports showing velocity, story points, and feature delivery statistics address the wrong audience need when stakeholders say Reviews feel "too technical."

### Sprint Retrospective
- AI can identify patterns across multiple retrospectives (recurring themes, word frequency). However, pattern recognition is not causal diagnosis. "Communication breakdown" appearing in 68% of retros is a surface observation — the team must determine the root cause (which may be unclear decision authority, not communication format).
- AI-generated retrospective designs should be reviewed for team-specific context: psychological safety level, recent conflicts, individual learning styles, and actual time capacity. A well-structured generic design may still miss critical team dynamics.
- Retrospective transcripts contain sensitive content (interpersonal conflicts, performance concerns, leadership failures). Processing these through AI requires explicit individual consent, not majority agreement. One objection must be respected.

### Daily Scrum
- AI recommendations to change Daily Scrum format should be presented to the team for discussion, not imposed. Teams are self-managing — process changes require team ownership regardless of how strong the AI's evidence appears.

---

## AI for Metrics and Reporting

### Verification Before Presentation
- Always verify AI-calculated metrics using a spreadsheet or independent method before presenting to leadership. If metric definitions changed across measurement periods, the AI's trend analysis may be meaningless.
- AI-generated "scores" (Release Credibility Score, Team Efficiency Score) must have explainable, reproducible methodology. If the formula cannot be defended under questioning, present the underlying raw metrics instead.

### Contextualising AI-Flagged Trends
- AI reports relative changes ("300% increase in login issues") without absolute context. A 300% increase from 2 to 8 tickets, when user signups grew 8x (50 to 400), means the failure rate actually halved (4% to 2%). Always check absolute numbers and proportional context before acting on AI-flagged trends.

### Activity vs Outcome Metrics
- AI dashboards tracking individual commit frequency, lines of code, pull requests merged, and time in meetings measure **activity, not value**. These create perverse incentives: gaming metrics over collaboration, optimising for the dashboard over customer outcomes.
- When an organisation mandates AI-powered productivity dashboards, the Scrum Master's duty as change agent is to document how these metrics measure activity rather than outcomes, propose alternative outcome-based metrics (cycle time, customer value delivered, defect escape rate), and escalate psychological safety concerns to leadership with specific examples.
- Code metrics used for "contribution scores" reduce Developers to productivity units and violate professional autonomy. The Scrum Master response is not to pilot or improve the scoring — it is to articulate why the approach creates precisely the wrong incentives.

### Automated Status Reports
- AI-generated weekly status reports from Jira data risk replacing genuine stakeholder engagement with "data theatre." The Scrum Master should articulate specific risks (gaming incentives, loss of engagement) and propose the alternative: stakeholders attending Sprint Reviews to see working software directly.

---

## AI for Product Discovery and Backlog

### Validating AI Recommendations
- AI analysis of historical customer feedback identifies past patterns, not current needs. Before committing AI-recommended features to a roadmap, validate with current customers. Use a discovery sprint to test assumptions about actual needs versus historical patterns.

### AI-Generated Test Cards and Hypotheses
- When AI extracts testable hypotheses from PRDs, have a senior Developer review for technical accuracy before sharing with the Product Owner. AI may hallucinate specific technical claims (e.g., inventing a "60% improvement" figure not in the source document).
- The optimal workflow: AI generates initial extraction (fast), human cross-references every claim back to source document (catches hallucinations), senior Developer validates technical accuracy (catches misinterpretation). Reinvest saved time in higher-value experiment design.

### AI Citations and Research
- AI frequently hallucinate plausible-sounding academic citations. Check every citation URL and quoted claim against original sources before distribution. Professional reputation depends on citation accuracy regardless of AI disclosure.

---

## AI Ethics and Team Safety

### Consent and Privacy
- Analysing employee communications (Slack messages, code comments, PR discussions) for performance implications without explicit consent violates privacy expectations, even on company-owned systems. People wrote those messages expecting peer collaboration, not AI surveillance for coaching identification.
- When one team member objects to AI processing of retrospective data, seek explicit individual consent from every member with clear disclosure about data handling and opt-out alternatives. Majority agreement does not override individual consent for sensitive data.

### Psychological Safety
- AI systems that monitor team channels and escalate teams as "resistant to improvement" when adoption metrics are low impose algorithmic judgement over team self-organisation. This replaces servant leadership with surveillance management and violates professional autonomy.
- Individual contribution tracking (even anonymised) destroys psychological safety. In small teams, anonymisation is easily broken. The fundamental problem is using metrics for surveillance rather than team improvement.

### Accountability
- When AI-generated documentation leads to incorrect decisions (e.g., inaccurate architecture docs during incident response), accountability sits with the humans who accepted AI output without verification. AI outputs are hypotheses requiring validation. Humans remain accountable for outcomes regardless of tool assistance.

---

## AI Tool Configuration

### Custom Instructions
- Configure system-level custom instructions defining professional role, expertise level, communication preferences, and output requirements once, so every conversation inherits context automatically.
- For project-specific needs, keep profile instructions unchanged (persistent identity baseline) and provide project-specific requirements in each conversation prompt. Layered approach: profile establishes baseline; prompts add situational context.

### Effective Prompt Design
- Specific trait instructions outperform vague ones. "Treat me as expert; apply radical candor; challenge assumptions; provide citations for non-obvious claims; skip introductory explanations; offer 3 follow-up questions" produces better results than "be helpful, accurate, and professional."
- When output is too high-level, provide specific feedback on what is missing ("Add 3 exercises per module with timing, materials needed, and learning objectives") rather than vague requests ("make it more detailed") or starting over.
- When output constraints matter (slide count, time limit, audience level), specify them upfront. Omitting constraints causes AI to optimise for comprehensiveness rather than actual success criteria.

### Platform Selection
- Evaluate actual workflow needs (memory isolation, project separation, consent model) before selecting an AI platform. Match capabilities to real requirements rather than selecting based on feature checklists.

---

## Iterating on AI Output

### Reflection-Then-Regenerate
- For comprehensive but generic AI reports, use a reflection agent to critique the original output, identify its biggest weaknesses, then create an improved prompt for a second run addressing identified gaps systematically. This is PDCA applied to AI interaction.

### Meta-Prompting
- When a prompt produces acceptable but not excellent results, ask the AI to critique the prompt itself: "What's ambiguous? What's missing? What constraints would sharpen the output?" Use the AI's suggestions to revise and test. This is more effective than random trial-and-error iteration.

---

## Common Anti-Patterns

| Anti-Pattern | Description | Remedy |
|---|---|---|
| AI as oracle | Treating AI output as authoritative conclusion | AI produces hypotheses; validate with human expertise |
| Dependency inversion | Human validates AI rather than AI assisting human | Reset to manual; rebuild direct engagement; reintroduce AI selectively |
| Optimising broken processes | Using AI to automate a dysfunctional ceremony | Fix the ceremony format first; then consider AI assistance |
| Pattern = diagnosis | Treating word frequency as root cause | Use AI patterns as conversation starters; team determines root cause |
| Surveillance coaching | Using AI to monitor and score individual performance | Advocate for outcome metrics; escalate psychological safety concerns |
| Consent bypass | Processing team data because it's on company systems | Explicit individual consent required for AI processing of team data |
| Hollow automation | Professional-looking AI reports that feel formulaic | Rebuild direct data engagement; AI should amplify insight, not replace it |

## Additional Resources

- **`scrum`** skill — Scrum framework, events, artifacts for context on where AI intersects with ceremonies
- **`agile-metrics`** skill — Metrics foundations for understanding what AI should and should not measure
- **`agile-coach`** skill — Coaching stances and psychological safety foundations
