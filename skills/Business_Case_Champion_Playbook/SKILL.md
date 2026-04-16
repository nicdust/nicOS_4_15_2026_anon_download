---
name: Business Case - Champion Playbook
description: Generates a personalized champion enablement dashboard with pitch language, objections, and shareable assets.
---

# SKILL INSTRUCTIONS: Business Case - Champion Playbook

  PURPOSE:
  Generate a high-polish microsite giving your champion everything they need to sell [Your Company] internally.
  This is NOT for the champion to evaluate [Your Company] -- they're already bought in. This helps them convince others.

  REQUIRED INPUTS:
  - Champion name and title
  - Company name
  - Deal context
  - Key stakeholders they need to convince

  FRAME STRUCTURE:
  Section 1: Header (Company logo + [Your Company] logo, "Champion Playbook for [Company]")
  Section 2: The Elevator Pitch (Copy-Paste block for the champion to use)
  Section 3: The Business Case (3 Cards: The Barrier, The Solution, Target Outcomes)
  Section 4: Investment Summary (Timeline, Effort, Investment)
  Section 5: Objection Handling (Expandable accordion for common objections: Security, Budget, IT approval)
  Section 6: Social Proof (Case study card)
  Section 7: Shareable Assets (Links to one-pagers, security docs)
  Section 8: Next Steps (Clear CTA to set up an intro call)

  DESIGN SPECS:
  - Dark mode hero section (premium feel)
  - Glassmorphism effects
  - Copy-to-clipboard functionality on all pitch text

  BACKEND LOGGING ([Your CRM] & [Your Chat App]):
  Log the creation of this frame in two places:
  1. [Your CRM] Note: Find the Deal record (if no deal, use Company record). Create note titled "Champion Enablement Frame - [Champion Name] - Business Case" with 1-sentence description and Frame URL.
  2. [Your Chat App] Log: Channel: [Your Agent Log Channel]. Parent: "Champion Frame | [Deal/Account Name] | Created by: [Your Name]". Threaded Reply MUST contain: Frame Link, Conversation Link, Skill Used, Prompt (exact user prompt), Description (<100 words).

  CONSTANTS:
  [YOUR COMPANY]_LOGO = "[Your Company Logo URL]"
  [Agent to dynamically insert User Calendar Link]

  OUTPUT:
  Generate using your Frame Builder tool. Execute backend logging. Return frame URL.
