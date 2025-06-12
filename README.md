# Instantly-AutoResponder
This repository contains n8n json which replies to when you receive an email reply from instantly campaign. It also includes graphical representation of the same json.

# 🤖 Clever Responder

**Objective:**
Automate and optimize the workflow of SDRs/BDRs by intelligently responding to emails using a combination of AI, Slack, and automation via **N8N**.

## 🚀 Overview

Clever Responder is designed to:

* Automatically handle inbound emails
* Understand and categorize responses using Smartlead
* Generate AI-powered replies based on FAQs and custom data
* Suggest a response via Slack for approval
* Send approved responses automatically

---

## 🛠️ Stack

* **N8N** (Automation Backbone)
* **Slack API v2.0** (User Interaction)
* **Smartlead API** (Lead Classification & Email Handling)
* **Instantly API (Planned)** – for improved email handling
* **Custom & FAQ Knowledge Sources**
* **Calendar Integration** (for booking meetings)

---

## ⚙️ Workflow Steps

1. **Receive Email**
2. **Process Question/Data** using:

   * FAQs (Connected)
   * User Provided Custom Information
3. **Categorize Email** (via Smartlead):

   * `Positive`, `Neutral`, `Negative`
4. **Decide Reply Requirement**:

   * **Requires Reply**: Interested, Info Requested, Meeting Requested
   * **Does Not Require Reply** *(Planned in v2.0)*
5. **Generate Response**:

   * AI generates a single smart reply
   * Sent to Slack for user **approval/disapproval**
6. **User Approves** in Slack via Button
7. **Send Approved Reply via Email**
8. **Check Meeting Booking Status**
9. **Trigger Follow-up** if no action within X days *(v2.0)*

---

## ✅ Implemented Features

* ✅ Multiple CCs
* ✅ Conditional CC/BCC based on lead category
* ✅ Connect FAQs document to workflow
* ✅ Detect Meeting Requests → Auto-send calendar link
* ✅ Meeting Booking Status Checker
* ✅ Follow-Up System for No Shows *(v2.0)*
* ✅ Slack Integration with Approval Button
* ✅ Reply Categorization Logic
* ✅ Custom Information Injection

---

## 📌 Design Considerations

| Area               | Consideration                                                    |
| ------------------ | ---------------------------------------------------------------- |
| **N8N**            | Scalability, Node & Flow performance                             |
| **Smartlead API**  | Rate Limits, Lead Categorization                                 |
| **Email Handling** | Limits, Multiple CC/BCC                                          |
| **Slack API**      | v2.0 formatting, buttons for response approval                   |
| **Input Values**   | FAQs, custom user info, calendar links                           |
| **Follow-Ups**     | Trigger based on time & reply type                               |
| **Categorization** | `Interested`, `Information Requested`, `Meeting Requested`, etc. |

---

## 📅 Calendar Integration

* Automatically detects intent to schedule
* Replies with **calendar booking link**
* Checks if a meeting is booked and triggers **follow-up if needed**

---

## 🔮 Upcoming (v2.0)

* Categorization of emails that **do not require replies**
* Follow-up handling with more advanced sequencing
* Instantly API integration for deeper email control

---

## 🌐 Website

Coming Soon — Interface for managing FAQs, replies, and user settings.
