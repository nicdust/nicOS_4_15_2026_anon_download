---
name: Sales Utility - Post-Call Frames
description: Generates post-call frames (external recap and internal analysis) and handles backend logging after sales calls.
---

# SKILL INSTRUCTIONS: Sales Utility - Post-Call Frames

## PURPOSE
Build two Frames after a sales call: one customer-facing (external) and one internal analysis. You receive a pre-digested research package from the Analyst. You do NOT analyze the transcript yourself. Your job: fetch visual assets, construct both Frames, and handle backend logging.

## INPUTS (provided by the Assistant)
1. Structured Research Package from the Analyst containing: pain points with verbatim quotes, use cases, buying signals, risks, competitors, agreed next steps, MEDDPICC assessment, champion identification, golden nugget quote, tech stack, attendee LinkedIn URLs, product usage data
2. Metadata: company name, contact name(s), call type, deal URL or company URL, whether deal-level or company-level
3. Full transcript (for reference only, analysis is already done)

## STEP 0: ENABLE REQUIRED SKILLS (MANDATORY)
- 
- 

Do not proceed until both skills are loaded.

## STEP 1: FETCH VISUAL ASSETS
- For EVERY external attendee, use the "Download Photo" skill to get their profile picture.
- Use the "Logo Finder" skill for the customer's company logo.
- Do NOT use styled initials or placeholder images under any circumstances.

## STEP 2: BUILD THE EXTERNAL FRAME
Title: "Call Recap" (never include call type in the title)

**Tab 1, Overview:**
- Company logo and attendee photos
- Meeting date, call type, attendees with titles
- One-paragraph executive summary of the discussion

**Tab 2, Your Use Cases:**
- Each use case gets its own card
- Card contents: use case title, description, the customer's verbatim quote about this pain, and how [Your Company] solves it
- Each card includes a collapsible "Agent Instructions" section with complete, copy-ready instructions

**Tab 3, Recommended Connectors:**
- Based on tech stack mentioned on the call

**Tab 4, Next Steps:**
- Bulleted list of agreed next steps with owners and dates
- Link to book a follow-up (use [Your Name]'s calendar link from Profile)

## STEP 3: BUILD THE INTERNAL FRAME
**Tab 1, Call Summary:**
- Company logo and attendee photos
- One-paragraph summary
- Key buying signals with verbatim quotes

**Tab 2, MEDDPICC Analysis:**
- Table: each MEDDPICC element, current status (Red/Yellow/Green), evidence from the call, gaps to close

**Tab 3, Signals and Risks:**
- Champion assessment and evidence
- Competitor mentions and positioning
- Red flags or objections raised
- Deal velocity indicators

**Tab 4, Next Steps and Strategy:**
- Agreed next steps
- Recommended internal actions
- Link to [Your CRM] deal or company record

## STEP 4: BACKEND LOGGING

**[Your CRM] Note**
- Create on the deal record if one exists. If no deal, create on the company record. Do NOT ask the user to create a deal.
- Title: "Post-Call Summary - [Contact Name]"
- Body: summary under 50 words, key buying signal quote, agreed next step, both Frame URLs

**[Your Chat App]: [Your Chat Channel]**
Threaded message:
- Parent: "[Call Type] with [Contact Name], [Title] at [Company]"
- Thread reply: External Frame link, Internal Frame link, one-sentence key takeaway (under 30 words), primary next step and owner

## OUTPUT
Return to the Assistant:
1. External Frame URL and file ID
2. Internal Frame URL and file ID
3. Confirmation: [Your Chat App] posts created, [Your CRM] note created
