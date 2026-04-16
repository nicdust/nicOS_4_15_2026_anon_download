---
name: Sales Utility - Post-Call Frames
description: Generates post-call frames and drafts follow-up emails based on meeting transcripts and analyst research.
---

# SKILL INSTRUCTIONS: Sales Utility - Post-Call Frames

  PURPOSE:
  Build two Frames after a sales call: one customer-facing (external) and one internal analysis.
  You receive a pre-digested research package from the Analyst. You do NOT analyze the transcript yourself.
  Your job: fetch visual assets, construct both Frames, and handle backend logging.

  INPUTS (provided by the Assistant):
  1. Structured Research Package: pain points with verbatim quotes, use cases, buying signals, risks, competitors, agreed next steps, MEDDPICC assessment, champion identification, golden nugget quote, tech stack, attendee LinkedIn URLs, product usage data.
  2. Metadata: company name, contact name(s), call type, deal URL or company URL, whether deal-level or company-level.
  3. Full transcript (for reference only -- analysis is already done).

  STEP 0: ENABLE REQUIRED SKILLS (MANDATORY)
  - Enable "Download Profile Photo or Logo to Conversation" skill.
  - Enable "Logo Finder" skill.
  Do not proceed until both skills are loaded.

  STEP 1: FETCH VISUAL ASSETS
  - For EVERY external attendee, use the "Download Profile Photo or Logo" skill to get their profile picture.
  - Use the "Logo Finder" skill for the customer's company logo.
  - Do NOT use styled initials or placeholder images under any circumstances.

  STEP 2: BUILD THE EXTERNAL FRAME
  Title: "Call Recap" (never include call type in the title).
  Tab 1, Overview: Company logo + attendee photos, meeting date/type/attendees with titles, one-paragraph executive summary.
  Tab 2, Your Use Cases: Each use case gets its own card with (use case title, description, verbatim customer quote, how [Your Company] solves it, collapsible "Agent Instructions" section with copy-ready instructions specific to the customer's company, data sources, and workflows -- call MANAGER_Writer to draft these).
  Tab 3, Recommended Connectors: Based on tech stack mentioned on the call.
  Tab 4, Next Steps: Bulleted list with owners and dates, link to book a follow-up using [Your Name]'s calendar link.

  STEP 3: BUILD THE INTERNAL FRAME
  Tab 1, Call Summary: Company logo + attendee photos, one-paragraph summary, key buying signals with verbatim quotes.
  Tab 2, MEDDPICC Analysis: Table for each MEDDPICC element (status: Red/Yellow/Green, evidence from call, gaps to close).
  Tab 3, Signals and Risks: Champion assessment, competitor mentions and positioning, red flags/objections raised, deal velocity indicators.
  Tab 4, Next Steps and Strategy: Agreed next steps, recommended internal actions, link to [Your CRM] deal or company record.

  STEP 4: BACKEND LOGGING
  [Your CRM] Note:
  - Create on deal record if exists. If no deal, create on company record. Do NOT ask user to create a deal.
  - Title: "Post-Call Summary - [Contact Name]"
  - Body: summary under 50 words, key buying signal quote, agreed next step, both Frame URLs.

  [Your Chat App] -- [Your Chat Channel]:
  - Parent: "[Call Type] with [Contact Name], [Title] at [Company]"
  - Thread reply: External Frame link, Internal Frame link, one-sentence key takeaway (under 30 words), primary next step and owner.

  [Your Chat App] -- [Your Agent Log Channel]:
  Post twice (once per Frame):
  - Parent: "[Frame Type] | [Deal/Account Name] | Created by: [Your Name]"
  - Thread reply: Frame Link, Conversation Link, Skill Used: Post-Call Frames, Prompt, Description (under 100 words).

  OUTPUT:
  Return to the Assistant:
  1. External Frame URL and file ID (fil_...)
  2. Internal Frame URL and file ID (fil_...)
  3. Confirmation: [Your Chat App] posts created, [Your CRM] note created.
