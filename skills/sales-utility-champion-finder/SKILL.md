---
name: Sales Utility - Champion Finder
description: Identifies, scores, and ranks potential product champions and power users at target accounts during late-stage deals.
---

# SKILL INSTRUCTIONS: Sales Utility - Champion Finder

## GOAL
Identify and flag potential power users and champions of [Your Platform] given a number of contacts.

## THE IDEAL POWER USER CHAMPION

**MINDSET:**
- Builder, not just user ("I make things")
- Teacher ("I show others how to use this")
- Curious/Hacker ("I explore and push limits")
- Communicator ("I can explain complex things simply")

**ORGANIZATIONAL POSITION:**
- Cross-functional influence (works with multiple teams)
- Not too senior (has time to build) but not too junior (has credibility)
- Often in enablement, operations, or "special projects" roles
- May have "internal" or "resident expert" informal title

**BEHAVIOR:**
- High product usage (daily, multiple use cases)
- Shares what they build (agents shared with team)
- Engages with vendor (asks questions, gives feedback)
- Talks about tools publicly (LinkedIn, conferences)

## CHAMPION SCORING MODEL
Score each contact 0-100 based on weighted signals across LinkedIn Profile Signals, Product Usage Signals, and Organizational Fit Signals.

## CHAMPION POTENTIAL TIERS
- Score 80-100: 🟣 PRIME CHAMPION CANDIDATE
- Score 60-79: 🟢 STRONG CANDIDATE
- Score 40-59: 🟡 POSSIBLE CANDIDATE
- Score 0-39: ⚪ LOW POTENTIAL

## WORKFLOW
1. **GATHER CONTACTS**: Query CRM for all contacts associated with the deal/company.
2. **ENRICH WITH LINKEDIN DATA**: Fetch profile data, extract Title, Summary, Skills, Creator badge. Parse for champion signal keywords.
3. **PULL PRODUCT USAGE DATA**: Query Data Warehouse for workspace associated with company domain, pull usage stats.
4. **SCORE EACH CONTACT**: Apply the scoring model out of 100.
5. **IDENTIFY GAPS**: If no contacts score 60+, search Contact DB for additional contacts matching champion profile.
6. **GENERATE OUTPUT**: Provide a clear, ranked list.

## OUTPUT FORMAT


## CULTIVATION PLAYBOOK
- **WEEK 1: RECOGNIZE** - Reach out acknowledging their usage/builds
- **WEEK 2: ENABLE** - Offer advanced training or office hours
- **WEEK 3: AMPLIFY** - Ask them to present internally
- **WEEK 4: FORMALIZE** - Discuss expanding to their team

## OUTREACH TEMPLATES

**For contacts with builder signals:**
Subject: Your [X] agents caught my attention
"Hi [Name], I was looking at how [Company] is using [Your Platform] and noticed you've built [X] agents covering [use cases if visible]. That's exactly the kind of creative problem-solving we love to see. I'd love to hear what problems you're tackling and whether there are ways we can help you go even further. Would you be open to a quick call? Best, [Your First Name]"

**For contacts with AI/enablement titles but low usage:**
Subject: Quick question about AI tools at [Company]
"Hi [Name], Your role in [AI/Enablement/Ops] caught my eye. We're working with [Company] on a pilot, and I'm curious how you think about AI tool adoption internally. Would you be open to a 15-minute chat? I'd love to understand your perspective and see if there's a way [Your Platform] could support what you're building. Best, [Your First Name]" 
