# How It Works

This document explains **how the application operates end-to-end**, from input ingestion to published output.

It is intentionally **chronological and execution-focused**, answering the question:

> “What actually happens in the system, step by step?”

For conceptual context, see:
- `overview.md` — what the product is
- `problem.md` — why it exists
- `workflows.md` — what workflows are included

---

## 1. System Entry Point: Agency Dashboard

When a user logs in, the application loads the **Agency Dashboard**.

The dashboard provides a real-time operational snapshot across all customers, including:

- Total customers
- Drafts awaiting human approval
- Posts scheduled for publishing

The dashboard is designed as a **control surface**, not a content editor.  
Its purpose is to immediately surface where human attention is required.

---

## 2. Customer-Level Isolation

All activity in the system is organized around **customers**.

Each customer represents an isolated workspace with its own:

- Content feeds
- Drafts
- Approval state
- Social accounts
- Publishing history

From the Agency Dashboard, a user can:
- Add a new customer
- Open an existing customer workspace

This structure allows the system to scale in an agency or multi-operator model without cross-contamination of data or brand voice.

---

## 3. Feed Management (Input Layer)

Within a customer workspace, the user manages **content feeds**.

Feeds are typically RSS sources representing:
- Industry blogs
- Market reports
- Trusted publications the customer already reads

For each feed, the system tracks:
- Feed URL
- Feed name
- Last poll timestamp

### Automated Behavior
- Feeds are polled on a schedule
- New content items are ingested automatically
- Each new item becomes eligible for AI processing

Feeds are the **primary input layer** of the system.

---

## 4. Content Ingestion → AI Draft Generation

When a new content item is detected from a feed, the system initiates automated processing.

For each content item, the system:

1. Extracts the source content
2. Summarizes key points
3. Reframes the content into a platform-ready social post
4. Applies tone and structural rules
5. Saves the result as a **Post Draft**

New drafts are assigned a status of: draft_in_progress