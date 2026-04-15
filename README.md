# NicOS — Dust Agent & Skills Library

A collection of anonymized AI agents and skills built on [Dust](https://dust.tt) for sales professionals using AI-native workflows. This repo is designed to be imported using the [dust-github-action](https://github.com/dust-tt/dust-github-action).

---

## What's Inside

### 🤖 Agents (Multi-Agent System)

The agents form a hierarchical orchestration system:



| Agent | Handle | Description |
|-------|--------|-------------|
| Master Assistant |  | Front door. Orchestrates all workflows. |
| MANAGER_Builder |  | Creates interactive frames, decks, and assets. |
| MANAGER_Writer |  | Writes emails, follow-ups, and agent prompts. |
| MANAGER_Analyst |  | Deep research, contact enrichment, transcript analysis. |
| Writer Agent & Skills Prompt Writer |  | Designs and reviews agent/skill instructions. |
| Analyst Sales Data Miner |  | Queries Snowflake, HubSpot, Lemlist for sales metrics. |
| Builder Comic |  | Creates interactive comic books as React frames. |
| Account Contact Mapping App |  | Builds org charts for target accounts in a database. |
| AUTO Meeting Prep |  | Daily meeting intelligence briefings. |
| AUTO Daily Prep |  | Daily morning digest: pipeline, tasks, agenda. |
| AUTO Task Manager |  | Manages task creation and completion. |
| AUTO New Deal Setup |  | Builds deal intelligence packages for new opportunities. |

---

### 🛠 Skills

| Skill | Handle | Description |
|-------|--------|-------------|
| Logo Finder |  | Finds verified logos from Wikimedia and other trusted sources. |
| Professional Profile Insights |  | Retrieves fresh profile data about contacts and companies. |
| Sales Utility - Deal Stage Validator |  | Validates CRM deal stage progression against exit criteria. |
| Download Profile Photo or Logo |  | Downloads headshots and logos as reusable file IDs. |
| Sales Utility - Post-Call Frames |  | Generates external + internal frames after sales calls. |
| Business Case - Champion Playbook |  | Builds champion enablement dashboards for internal selling. |
| Sales Meeting Prep |  | Multi-source briefing document for upcoming meetings. |
| CRM Backend Sync |  | Read/write operations across CRM, tasks, and chat logging. |
| Business Case - Team Overview |  | Team-specific business case frames (Sales, Eng, Support, etc.). |
| Company Context |  | Reference data: your company info, founders, differentiators. |
| Sales Utility - Champion Finder |  | Identifies and scores champion candidates at target accounts. |
| Personal & Team Context |  | Reference data: your personal info, team members, assets. |
| Outbound - Warm Reference Email |  | Drafts warm outreach emails referencing existing champions. |

---

## How to Use

### Option 1: Import via Sidekick

Each agent and skill in this library includes a **Sidekick Prompt** — a copy-paste instruction that tells Dust's Sidekick to:
1. Review your available workspace tools
2. Attach the right tools for that agent/skill
3. Replace the bracketed placeholders with your actual tool names

Look for the  field in the Notion source doc or the comments in each file.

### Option 2: Import via GitHub Action

1. Fork this repo.
2. Add your Dust API key as a GitHub secret: 
3. Configure the workflow to point at your workspace.
4. Push — the GitHub Action will upsert all agents and skills.

---

## Customizing for Your Setup

All placeholders use  format. Common substitutions:

| Placeholder | Replace with |
|-------------|-------------|
|  | Your company name |
|  | Your first and last name |
|  | HubSpot / Salesforce / Attio |
|  | Fathom / Gong / Granola |
|  | Gmail / Outlook |
|  | Google Calendar / Outlook Calendar |
|  | Slack / Microsoft Teams |
|  | Apollo / Surfe / Fullenrich |
|  | Dust Frames (Create Frames skill) |
|  | Notion / Confluence |
|  | Snowflake / BigQuery |
|  | Your Supabase project ID |

---

## Architecture Notes

- **Agents call agents**: This system uses multi-agent delegation extensively. Master_Assistant delegates to Managers who delegate to Sub-Agents.
- **Skills are composable**: Skills like Logo Finder and Download Profile Photo are called by multiple agents automatically.
- **Backend logging**: Most agents log to a dedicated Slack channel for traceability.
- **Approval handling**: All agents that write to CRM or send emails are designed to pause for user approval.

---

## Source

Originally built by an AE at a B2B SaaS company. Anonymized and shared for the Dust community.
Inspired by the [dust-github-action](https://github.com/dust-tt/dust-github-action) GitOps pattern.
