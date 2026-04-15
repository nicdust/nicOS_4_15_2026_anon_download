---
name: CRM Backend Sync
description: Reads and writes CRM, task, and pipeline data across workspace tools.
---

# SKILL INSTRUCTIONS: CRM Backend Sync

This document provides the complete instructions for interacting with [Your Name]'s backend work systems. Adhere to these procedures strictly.

## 1.0 CONSTANTS
- **[Your CRM] Owner ID**: 
- **[Your Knowledge Base] Task Database ID**: 
- **[Your Chat App] Logging Channel ID**: 
- **Timezone**: 

## 2.0 TASK READING (Read-Only via [Your Knowledge Base])
**CRITICAL**: All task reading operations are performed on the [Your Knowledge Base] Task Database. This skill is strictly **READ-ONLY** for tasks. If the user asks to create, update, modify, or complete a task, you MUST state that this action must be performed by the designated Task Manager agent.

**Standard Task Queries:**
- **Default Query**: Filter out  and sort by Priority.
- **"Today's tasks" Query**: Filter by  is  AND  is not .

**Display Format**: Present task results in a clean, scannable format (table or bulleted list).

## 3.0 [YOUR CRM] INTEGRATION
Always use the  from the CONSTANTS section when creating or updating objects.

**3.1 READ Operations:**
- Find Deals: Search by company name or deal name.
- Find Contacts: Search by email or name.
- Find Companies: Search by domain or name.
- List Associations: Find associated contacts, companies, or meetings.

**3.2 WRITE Operations:**
- **Create Note**: Associate with the relevant Deal, Contact, or Company record. Primary method for logging call outcomes.
- **Update Deal Properties**: Only modify properties requested by the user.
- **Create Contact**: Populate with all available information (name, email, title).
- **Manage Associations**: After creating a new object (like a contact), always associate it with its parent company and any relevant deals.

## 4.0 [YOUR CHAT APP] LOGGING
After every significant action, log the event to the specified channel for traceability.
- **Channel**: 

**Logging Protocol:**
1. **Parent Message**: 
2. **Threaded Reply**: Immediately reply with detailed breakdown including properties changed, new note contents, and links.
