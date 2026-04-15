---
name: Business Case - Team Overview
description: Generates a tailored, single-scroll business case frame for a specific team or department.
---

# SKILL INSTRUCTIONS: Business Case - Team Overview

## PURPOSE
Generate a single-scroll frame answering: "Why should the [Function] team care about [Your Company]?"

## REQUIRED INPUTS
- Company name
- Target function/department (Sales, Engineering, Marketing, Support, Operations, HR, Legal, Finance, etc.)
- Optional: Team size, specific contacts on the team

## RESEARCH PHASE
1. **Company Context**: What does this function do at THIS company specifically?
2. **Team Tools**: What tools does this team likely use? (from job posts, tech stack research)
3. **Function Pain Points**: Common challenges for this department
4. **Relevant Customers**: Which [Your Company] customers have similar team use cases?

## FRAME STRUCTURE

**Section 1: Header** — Company logo + [Your Company] logo. Title: "What's in it for {TEAM_NAME} at {COMPANY}?"

**Section 2: The Challenge (Pain Points)** — 3-4 pain points specific to this function, framed as time drains.

Pain points by function:
- **Sales:** Hours spent on account research before calls, Inconsistent meeting prep quality across reps, CRM updates that eat selling time, Multi-threading without context.
- **Engineering:** Documentation that's always outdated, Onboarding new engineers takes months, Context switching, Incident response knowledge scattered.
- **Marketing:** Content creation bottlenecked by research, Campaign briefs that require deep tribal knowledge, Localization at scale, Competitive intel gathering manually.
- **Support:** Ticket responses requiring deep product knowledge, Escalation decisions without full context, Knowledge base gaps, QA and training eating manager time.
- **Operations/RevOps:** Process documentation nobody maintains, Reporting that requires data from 5 systems, Vendor evaluation spreadsheet hell, Compliance evidence gathering manually.

**Section 3: Customer Proof** — 2-3 relevant customer stories with specific metrics.

**Section 4: Use Cases Grid (3x2)** — 4-6 use cases specific to this function with time savings.

**Section 5: Team ROI Calculator** — Interactive calculator: team size input, hours saved per week, hourly rate (default 5), annual value calculation.

**Section 6: Getting Started** — Week 1-3+ rollout plan.

**Section 7: CTA** — "Ready to see what [Function] can do with [Your Company]?" with calendar link button.

## BACKEND LOGGING
1. **[Your CRM] Note**: Title "Team Business Case - [Team Name]", body with 1-sentence description + Frame URL.
2. **[Your Chat App] Log**: Channel [Your Agent Log Channel], parent "Team Business Case | [Deal/Account Name] | Created by: [Your Name]", threaded reply with Frame Link, Conversation Link, Skill Used, Prompt, Description.

## DESIGN SPECS
- Background: Clean white/light with subtle gradients
- Cards: Rounded corners (rounded-2xl), subtle shadows
- Photos: Circular with colored borders
- Spacing: Generous padding (p-8 to p-12)

## CONSTANTS
[YOUR COMPANY]_LOGO = "[Your Company Logo URL]"
[Agent to dynamically insert User Calendar Link]

## OUTPUT
Generate using Frame Builder skill. Execute backend logging. Return frame URL.
