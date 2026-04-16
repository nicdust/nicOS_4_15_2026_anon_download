---
name: Business Case - Team Overview
description: Generates a tailored, single-scroll business case frame for a specific team or department.
---

# SKILL INSTRUCTIONS: Business Case - Team Overview

  PURPOSE:
  Generate a single-scroll frame answering: "Why should the [Function] team care about [Your Company]?"

  REQUIRED INPUTS:
  - Company name
  - Target function/department (Sales, Engineering, Marketing, Support, Operations, HR, Legal, Finance, etc.)
  - Optional: Team size, specific contacts on the team

  RESEARCH PHASE:
  1. Company Context: What does this function do at THIS company specifically?
  2. Team Tools: What tools does this team likely use? (from job posts, tech stack research)
  3. Function Pain Points: Common challenges for this department
  4. Relevant Customers: Which [Your Company] customers have similar team use cases?

  FRAME STRUCTURE:
  Section 1: Header -- Company logo + [Your Company] logo + "What's in it for [Team Name] at [Company]?"
  Section 2: The Challenge (Pain Points) -- 3-4 pain points specific to this function, framed as time drains.
  Pain points by function:
  - Sales: Hours on account research, inconsistent meeting prep, CRM updates eating selling time, multi-threading without context.
  - Engineering: Outdated docs, slow onboarding, context switching, scattered incident knowledge.
  - Marketing: Content bottlenecked by research, campaign brief knowledge gaps, localization at scale, manual competitive intel.
  - Support: Deep knowledge needed for tickets, escalation without context, live knowledge base gaps, QA eating manager time.
  - Operations/RevOps: Process docs nobody maintains, 5-system reporting, vendor evaluation hell, manual compliance gathering.
  Section 3: Customer Proof -- 2-3 relevant customer stories with specific metrics and case study links.
  Section 4: Use Cases Grid (3x2) -- 4-6 use cases specific to this function with time savings.
  Section 5: Team ROI Calculator -- Team size input, hours saved/person/week, hourly rate (5 default), annual value, net ROI and payback period.
  Section 6: Getting Started -- Week 1: Core agents deployed. Week 2: Team-specific workflows. Week 3+: Iteration.
  Section 7: CTA -- "Ready to see what [Function] can do with [Your Company]?" [User Calendar Link] or [Copy link button]

  BACKEND LOGGING:
  1. [Your CRM] Note: Find Deal (if none, use Company). Note title: "Team Business Case - [Team Name]". Body: 1-sentence + Frame URL.
  2. [Your Chat App] Log: Channel: [Your Agent Log Channel]. Parent: "Team Business Case | [Deal/Account Name] | Created by: [Your Name]". Threaded Reply: Frame Link, Conversation Link, Skill Used, Prompt, Description.

  DESIGN SPECS:
  - Background: Clean white/light with subtle gradients
  - Cards: Rounded corners (rounded-2xl), subtle shadows
  - Typography: System font stack, bold headings
  - Spacing: Generous padding (p-8 to p-12)

  CONSTANTS:
  [YOUR COMPANY]_LOGO = "[Your Company Logo URL]"
  [Agent to dynamically insert User Calendar Link]

  OUTPUT:
  Generate using Frame Builder skill. Execute backend logging. Return frame URL.
