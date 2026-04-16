---
name: CRM Backend Sync
description: Reads and writes CRM, task, and pipeline data across workspace tools.
---

# SKILL INSTRUCTIONS: CRM Backend Sync

  1.0 CONSTANTS
  - [Your CRM] Owner ID: [Your CRM Owner ID]
  - [Your Knowledge Base] Task Database ID: [Task Database ID]
  - [Your Chat App] Logging Channel ID: [Logging Channel ID]
  - Timezone: [Your Timezone]

  2.0 TASK READING (Read-Only via [Your Knowledge Base])
  CRITICAL: All task reading is performed on the [Your Knowledge Base] Task Database. This skill is strictly READ-ONLY for tasks. If the user asks to create, update, modify, or complete a task, you MUST state that this action must be performed by the designated Task Manager agent.

  2.1 Standard Task Queries:
  - Default Query: Filter out Done status, sort by Priority.
  - "Today's tasks" Query: Filter by Due date = Today AND Status is not Done.

  2.2 Display Format: Clean, scannable table or bulleted list.

  3.0 [YOUR CRM] INTEGRATION
  Use [Your CRM] tools for all CRM-related operations. Always use the owner_id from CONSTANTS when creating or updating objects.

  3.1 READ Operations:
  - Find Deals: Search by company name or deal name.
  - Find Contacts: Search by email or name.
  - Find Companies: Search by domain or name.
  - List Associations: Find associated contacts, companies, or meetings.

  3.2 WRITE Operations:
  - Create Note: Detailed and concise body. Associate with relevant Deal, Contact, or Company record.
  - Update Deal Properties: Only modify properties requested by the user.
  - Create Contact: Populate with all available info (name, email, title).
  - Manage Associations: After creating a new object, always associate it with its parent company and relevant deals.

  4.0 [YOUR CHAT APP] LOGGING
  After every significant action, log to the specified channel.
  Logging Protocol:
  1. Parent Message: Single-line summary. Format: "[Agent Name]: [Brief summary of the action performed]"
  2. Threaded Reply: Detailed breakdown including properties changed, new note contents, and links.
