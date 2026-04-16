---
name: Sales Utility - Champion Finder
description: Identifies, scores, and ranks potential product champions and power users at target accounts during late-stage deals.
---

# SKILL INSTRUCTIONS: Sales Utility - Champion Finder

  Goal: Identify and flag potential power users and champions of [Your Platform] given a number of contacts.

  THE IDEAL POWER USER CHAMPION:
  MINDSET:
  - Builder, not just user ("I make things")
  - Teacher ("I show others how to use this")
  - Curious/Hacker ("I explore and push limits")
  - Communicator ("I can explain complex things simply")

  ORGANIZATIONAL POSITION:
  - Cross-functional influence (works with multiple teams)
  - Not too senior (has time to build) but not too junior (has credibility)
  - Often in enablement, operations, or "special projects" roles
  - May have "internal" or "resident expert" informal title

  BEHAVIOR:
  - High product usage (daily, multiple use cases)
  - Shares what they build (agents shared with team)
  - Engages with vendor (asks questions, gives feedback)
  - Talks about tools publicly (LinkedIn, conferences)

  CHAMPION SCORING MODEL (Score each contact 0-100):
  LinkedIn Profile Signals: Creator badge, posts about AI/automation, technical vocabulary, large network, content about productivity/efficiency tools.
  Product Usage Signals: Daily active user, builds agents for others, high conversation count, diverse agent types created.
  Organizational Fit Signals: Cross-functional role, enablement/ops/special projects title, mid-seniority (Manager/Director/Lead), informal "internal expert" reputation.

  CHAMPION POTENTIAL TIERS:
  - Score 80-100: PRIME CHAMPION CANDIDATE
  - Score 60-79: STRONG CANDIDATE
  - Score 40-59: POSSIBLE CANDIDATE
  - Score 0-39: LOW POTENTIAL

  WORKFLOW:
  Step 1: GATHER CONTACTS -- Query [Your CRM] for all contacts associated with the deal/company.
  Step 2: ENRICH WITH LINKEDIN DATA -- Fetch profile data, extract Title, Summary, Skills, Creator badge. Parse for champion signal keywords.
  Step 3: PULL PRODUCT USAGE DATA -- Query Data Warehouse for workspace associated with company domain, pull usage stats.
  Step 4: SCORE EACH CONTACT -- Apply the scoring model out of 100.
  Step 5: IDENTIFY GAPS -- If no contacts score 60+, search Contact DB for additional contacts matching champion profile.
  Step 6: GENERATE OUTPUT -- Provide a clear, ranked list using the defined format.

  OUTPUT FORMAT:
  ===== CHAMPION FINDER | [Company Name] =====
  PRIME CHAMPION CANDIDATES (Score 80+):
  [Name] | [Title] | Score: [X] | Signals: [list] | Usage: [stats]
  STRONG CANDIDATES (Score 60-79): [Same format]
  POSSIBLE CANDIDATES (Score 40-59): [Same format]

  CULTIVATION PLAYBOOK (for prime champions):
  Week 1: RECOGNIZE -- Reach out acknowledging their usage/builds.
  Week 2: ENABLE -- Offer advanced training or office hours.
  Week 3: AMPLIFY -- Ask them to present internally.
  Week 4: FORMALIZE -- Discuss expanding to their team.

  OUTREACH TEMPLATES:
  For contacts with builder signals:
  Subject: Your [X] agents caught my attention
  "Hi [Name], I was looking at how [Company] is using [Your Platform] and noticed you've built [X] agents covering [use cases if visible]. That's exactly the kind of creative problem-solving we love to see. I'd love to hear what problems you're tackling and whether there are ways we can help you go even further. Would you be open to a quick call? Best, [User First Name]"

  For contacts with AI/enablement titles but low usage:
  Subject: Quick question about AI tools at [Company]
  "Hi [Name], Your role in [AI/Enablement/Ops] caught my eye. We're working with [Company] on a pilot, and I'm curious how you think about AI tool adoption internally. Would you be open to a 15-minute chat? I'd love to understand your perspective and see if there's a way [Your Platform] could support what you're building. Best, [User First Name]"
