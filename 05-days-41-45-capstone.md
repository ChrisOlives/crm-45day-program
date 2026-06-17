# Days 41–45: Capstone Project
## Phase 6: Build a Complete Revenue System
## Company: GrowthBridge Agency — Full Deployment

---

# ═══════════════════════════════════════════
# CAPSTONE PROJECT OVERVIEW
# ═══════════════════════════════════════════

## What You Are Building

A production-ready, end-to-end revenue system for GrowthBridge Agency that combines
everything from Days 1–40 into a single, cohesive, deployment-quality deliverable.

This is not a practice exercise. This is the project you show employers.

## What the System Covers

1. Lead capture (HubSpot forms + n8n webhook intake)
2. AI-powered lead qualification and routing (n8n + OpenAI)
3. CRM management (HubSpot contacts, companies, lifecycle stages)
4. Pipeline management (HubSpot deals + automation)
5. Marketing automation (email nurture sequences + workflows)
6. Sales sequences (HubSpot Sales Hub)
7. Client onboarding (HubSpot + n8n parallel workflow)
8. Customer support ticketing (HubSpot Service Hub)
9. Retention and upsell automation (HubSpot workflows)
10. Reporting dashboards (HubSpot + Google Sheets)
11. Deployment-quality documentation (SOPs, runbooks, architecture diagrams)

## Business Context

GrowthBridge Agency is scaling from 30 to 60 clients.
Their current system is held together with spreadsheets and manual effort.
You have been hired as their CRM Architect and Automation Engineer to build a system
that will support 2× client growth without hiring more operations staff.

Your deliverable: a fully deployed, documented, and handed-off revenue system.

## Capstone Structure

| Day | Focus | Output |
|-----|-------|--------|
| Day 41 | System architecture + HubSpot master configuration | Architecture doc + full HubSpot setup |
| Day 42 | Complete automation stack (HubSpot workflows) | 8 production workflows |
| Day 43 | Complete n8n automation stack | 5 production n8n workflows |
| Day 44 | Executive reporting suite | 3 dashboards + analytics report |
| Day 45 | Final documentation + portfolio packaging | Complete deliverable package |

---

# ═══════════════════════════════════════════
# DAY 41: SYSTEM ARCHITECTURE + MASTER HUBSPOT CONFIGURATION
# ═══════════════════════════════════════════

## DAY 41

### Objective
Design the full system architecture on paper first, then configure HubSpot to match the design exactly — properties, pipelines, lifecycle stages, users, and teams.

### Real-World Context
Professional CRM architects design before they build. The architecture document is both a blueprint for the build and a deliverable the client can review before you touch their CRM. It also protects you — if a client changes their mind later, you can point to the signed-off architecture. This "design first" approach is what separates a $40/hr freelancer from a $150/hr consultant.

### Mini Theory (10 min)
Review: System design principles for CRMs — single source of truth, avoid redundant properties, design for the end user (reps), build for scalability (don't create 50 properties no one will fill in). What a "CRM architecture diagram" includes: objects, properties, pipelines, workflows, integrations, and data flows.

### Main Project Task — Part 1: Architecture Document

**Create: "GrowthBridge Revenue System — Architecture v1.0" (Google Docs)**

**Section 1: Executive Summary**
"This document defines the architecture of the GrowthBridge Agency Revenue System, built on HubSpot CRM with n8n automation. The system supports the full revenue lifecycle from lead capture through client retention, and is designed to scale from 30 to 60+ clients without additional operations headcount."

**Section 2: System Objectives**
List 6 measurable objectives:
1. Reduce lead response time from [current] to under 1 hour
2. Automate client onboarding from 3 days to 2 hours
3. Eliminate manual monthly reporting (currently 20+ hours/month)
4. Provide real-time pipeline visibility to leadership
5. Reduce data entry errors by 90% through automation
6. Enable segmented marketing to leads, prospects, and clients separately

**Section 3: Tech Stack**
Table: Tool | Purpose | Plan/Tier | Cost
- HubSpot CRM | CRM, marketing, sales, service | Free/Starter | $0–$50/mo
- n8n | Automation middleware | Self-hosted | $0
- Google Sheets | Data logging, reporting | Free | $0
- Slack | Team notifications | Free | $0
- Gmail | Email sending | Free | $0
- OpenAI API | AI qualification + content | Pay-as-you-go | ~$5/mo

**Section 4: Object Architecture**
For each HubSpot object (Contact, Company, Deal, Ticket):
- Purpose
- Key properties (list custom ones)
- Relationships to other objects

**Section 5: Lifecycle Stage Definitions**
Table: Stage | Entry Criteria | Exit Criteria | Owner (Marketing/Sales/CS)

**Section 6: Pipeline Architecture**
For each pipeline: name, stages, probability, SLAs

**Section 7: Automation Inventory**
Table of ALL workflows (HubSpot + n8n):
Automation Name | Tool | Trigger | Purpose | Status

**Section 8: Integration Map**
Diagram (embed from Canva) showing how HubSpot ↔ n8n ↔ Google Sheets ↔ Slack ↔ Gmail ↔ OpenAI connect

**Section 9: Data Governance Rules**
Key rules: required fields, naming conventions, duplicate handling, ownership rules

**Section 10: Rollout Timeline**
What was built in each phase (Days 1–45) — presented as a client-facing timeline

---

### Main Project Task — Part 2: HubSpot Master Configuration

Using your existing HubSpot account, do a full audit and cleanup. Ensure the following are in place for GrowthBridge:

**Users & Teams (confirm):**
- 3 users: Admin (you), Account Manager (Sarah), Operations (Marcus)
- 2 Teams: Sales/Marketing Team, Operations Team

**Contact Properties — "GrowthBridge Contact Data" group:**
- Contact Type (Dropdown): Lead, Prospect, Client, Partner, Vendor
- Service Interest (Multi-checkbox): SEO, Paid Ads, Social Media, Email Marketing, CRM Management, Full Service
- Monthly Budget (Dropdown): Under $1K, $1K–$2.5K, $2.5K–$5K, $5K+
- Lead Source Detail (Single-line text)
- Assigned Account Manager (Single-line text)
- Client Since (Date)
- Contract Renewal Date (Date)
- NPS Score (Number)
- Client Health Score (HubSpot Score — configure this)

**Deal Properties — "GrowthBridge Deal Data" group:**
- Service Package (Dropdown): SEO Only, Ads Only, Full Service, CRM Management, Custom
- Monthly Retainer Value (Number)
- Annual Contract Value (Number)
- Contract Length (Dropdown): Month-to-Month, 3 months, 6 months, 12 months
- Contract Start Date (Date)
- Contract End Date (Date)

**Pipelines (confirm all exist):**
1. GrowthBridge New Business Pipeline (8 stages)
2. GrowthBridge Client Onboarding Pipeline (6 stages)
3. GrowthBridge Upsell Pipeline (5 stages)
4. GrowthBridge Support Ticketing Pipeline (6 stages)

**Active Lists (confirm or build):**
1. All Active Clients
2. Hot Leads (HubSpot Score ≥ 50)
3. Leads in Nurture
4. Clients Up for Renewal (Contract Renewal Date within 60 days)
5. At-Risk Clients (NPS Score < 7 OR Client Health Score < 30)
6. High-Value Clients (Monthly Retainer ≥ $2,500)

### Deliverable
Architecture document (10 sections) + fully configured HubSpot account with all properties, pipelines, and lists confirmed.

### Portfolio Artifact
- Export Architecture document as a professionally formatted PDF (add a cover page with the GrowthBridge logo)
- Screenshot: HubSpot property list showing all custom properties
- Screenshot: All 4 pipelines in settings
- Screenshot: All 6 active lists with member counts
- Screenshot: Integration Map diagram from Canva (full size)
- Save to: `/Capstone Project/Architecture/`

### Success Criteria
- [ ] Architecture document has all 10 sections complete
- [ ] All custom properties exist in HubSpot with correct types
- [ ] All 4 pipelines exist with correct stage counts
- [ ] All 6 lists are active and have at least 1 member
- [ ] Integration map diagram is visually professional

### Estimated Time: 4 hours

---

# ═══════════════════════════════════════════
# DAY 42: COMPLETE HUBSPOT AUTOMATION STACK
# ═══════════════════════════════════════════

## DAY 42

### Objective
Build or refine all 8 production HubSpot workflows for GrowthBridge — covering the full lifecycle from lead to renewing client. These should be polished, tested, and portfolio-ready.

### Real-World Context
Eight well-built workflows covering the complete customer lifecycle is the kind of system that would take a junior HubSpot specialist months to build and debug. Having it in your portfolio — with documentation and testing evidence — shows an employer you can hit the ground running.

### Main Project Task
**Build / Audit / Polish All 8 Production HubSpot Workflows**

For each workflow: review if it was built in previous days, refine it, ensure it's ON, and re-test it.

---

**Workflow 1: "New Lead — Intake & Routing"**
Trigger: Contact is created AND Lifecycle Stage = Lead (or form submission)
Actions:
1. Set Lead Status = New
2. IF monthly budget ≥ $2,500 → assign to Sarah (Senior AM), ELSE → assign to Marcus
3. Create task for assigned owner: "First contact within 1 hour — {{contact.firstname}}"
4. Set contact property "Assigned Account Manager" = owner name
5. Enroll in Workflow 4 (Nurture Sequence) if not already enrolled

Test: Create 2 leads — one high budget, one low budget — verify different routing.

---

**Workflow 2: "MQL Alert — Sales Handoff"**
Trigger: HubSpot Score ≥ 50
Actions:
1. Set Lifecycle Stage = MQL
2. Send internal email to assigned AM: "🔥 MQL Alert: {{contact.firstname}} scored {{contact.hubspot_score}}"
3. Create urgent task (due: today): "Call MQL immediately"
4. Set Lead Status = Open
5. Delay 1 hour → IF Lead Status still = Open → send escalation to Admin

Test: Manually update a contact's HubSpot Score to 55, verify alert fires.

---

**Workflow 3: "Deal Created — Qualification Checklist"**
Trigger: Deal is created in New Business Pipeline
Actions:
1. Create 3 tasks for deal owner:
   - "Research company: {{company.name}}" (due: today)
   - "Send intro email using [Template Name]" (due: today + 1 day)
   - "Log decision maker name in deal record" (due: today + 2 days)
2. Set Deal Stage = New Inquiry (ensure it defaults correctly)
3. Send internal notification to Sales team

---

**Workflow 4: "Lead Nurture — 5-Email Sequence"**
Trigger: Contact lifecycle stage = Lead AND Contact is NOT a current client
Actions: (build or refine the email sequence)
Email 1 (immediate): "Thanks for reaching out to GrowthBridge"
Email 2 (Day 3): "How agencies like yours are getting more clients"
Email 3 (Day 7): "The #1 mistake small businesses make with digital marketing"
Email 4 (Day 14): "A case study: How [Fake Client] grew 40% in 6 months"
Email 5 (Day 21): "One last thing before I close your file…"
Final action: If no reply/engagement → Set Lead Status = Unqualified

Test: Enroll a test contact and verify email timing.

---

**Workflow 5: "Closed Won — Client Onboarding Trigger"**
Trigger: Deal stage = Closed Won in New Business Pipeline
Actions:
1. Set Contact Lifecycle Stage = Customer
2. Set Contact "Client Since" = today
3. Set Contact "Contract Renewal Date" = today + contract length (use IF branch based on Contract Length property)
4. Create Onboarding Deal in Client Onboarding Pipeline
5. Send welcome email to new client
6. Send Slack-style internal notification: "🎉 NEW CLIENT: {{company.name}} — {{deal.dealname}} — ${{deal.amount}}/mo"
7. Create 5 onboarding tasks for assigned AM (with due dates)
8. Add contact to "All Active Clients" static list

Test: Move a sample deal to Closed Won and verify all 8 actions fire.

---

**Workflow 6: "Client Health Monitoring — At-Risk Alert"**
Trigger: Client Health Score drops below 30 OR NPS Score < 7
Actions:
1. Add contact to "At-Risk Clients" active list
2. Create task for AM: "⚠️ Client health drop — reach out to {{contact.firstname}} at {{company.name}} today"
3. Send internal email to AM: full details + suggested talking points
4. Delay 3 days → IF task still open → escalate to Admin

Test: Manually set a client's NPS Score to 5 and verify task creation.

---

**Workflow 7: "Contract Renewal — 60/30/7 Day Alerts"**
Trigger: Contact property "Contract Renewal Date" = 60 days from today
Actions at Day -60:
1. Create task for AM: "Begin renewal conversation with {{contact.firstname}}"
2. Internal email: "Contract renewal in 60 days: {{company.name}} — ${{contact.monthly_budget}}/mo"

Trigger re-enrollment at Day -30:
1. If no renewal deal created: escalate reminder to AM + Admin
2. Create task: "Send renewal proposal this week"

Trigger at Day -7:
1. URGENT task: "Contract expires in 7 days — confirm renewal or flag as at-risk"
2. If no action: send final escalation to leadership

Test: Set a contact's renewal date to 60 days from today, verify Day -60 task created.

---

**Workflow 8: "Upsell Trigger — Identify Expansion Opportunities"**
Trigger: Contact is Customer AND Monthly Budget < $2,500 AND Client Since > 90 days ago
Actions:
1. Create task for AM: "Review {{company.name}} for upsell opportunity — they've been a client 90+ days"
2. Set contact property "Upsell Candidate" = True
3. Create deal in Upsell Pipeline: "{{company.name}} — Expansion Opportunity"
4. Internal notification to AM with context

Test: Find a contact who qualifies and manually trigger enrollment.

---

**After building all 8 workflows:**

Create a "Workflow Testing Log" in Google Sheets:
Columns: Workflow Name | Test Date | Test Contact Used | Expected Outcome | Actual Outcome | Pass/Fail | Notes

Document every test — this is your quality assurance record.

### Deliverable
8 production HubSpot workflows, all ON, all tested, all documented in testing log.

### Portfolio Artifact
- Screenshot: HubSpot workflow list showing all 8 workflows as "ON"
- Screenshot: Each workflow canvas (8 screenshots)
- Screenshot: Workflow Testing Log showing all pass results
- Export workflow diagrams (screenshot each fully expanded)
- Save to: `/Capstone Project/HubSpot Automations/`

### Success Criteria
- [ ] All 8 workflows are in "ON" status (not draft)
- [ ] Each workflow has been tested with at least 1 test contact
- [ ] Workflow Testing Log shows 8 rows, all Pass
- [ ] Workflow 5 (Closed Won) fires all 8 actions in sequence
- [ ] Workflow 7 (Renewal) has 3 separate time-based triggers

### Estimated Time: 5 hours

---

# ═══════════════════════════════════════════
# DAY 43: COMPLETE n8n AUTOMATION STACK
# ═══════════════════════════════════════════

## DAY 43

### Objective
Build or refine all 5 production n8n workflows for GrowthBridge — these should integrate directly with the HubSpot system built on Day 41–42. Together, HubSpot + n8n form one unified revenue system.

### Real-World Context
The n8n layer handles everything HubSpot can't do natively: AI processing, complex multi-app routing, external API calls, and custom logic. Think of HubSpot as the database and CRM, and n8n as the intelligence layer on top of it. A candidate who can show both working together in a single system is applying for roles at a significantly higher level.

### Main Project Task
**Build / Refine All 5 Production n8n Workflows**

---

**n8n Workflow 1: "Master Lead Intake" (refined from Day 32)**
This is the primary entry point for all inbound leads.

Complete node sequence:
1. Webhook trigger (receives from all form sources)
2. Data normalization (Code node — standardize field names regardless of source form)
3. Domain extraction (Code node)
4. OpenAI: Quick qualification pre-score
   - Prompt: "Score this lead 1-10 on fit for a digital marketing agency. Return JSON: {fit_score: number, reasoning: string}"
5. IF: Fit score ≥ 7 → Priority path; score < 7 → Standard path
6. HubSpot: Create or Update Contact (both paths)
7. Priority path: HubSpot Create Deal + Slack #priority-leads + Gmail personalized outreach
8. Standard path: HubSpot set lifecycle = Lead + add to nurture queue in Google Sheets
9. Both paths: Log to "Lead Intake Master Log" Google Sheet

Refinements from Day 32:
- Add the AI pre-scoring (new)
- Add priority vs. standard branching (new)
- Add error handling: if HubSpot node fails, log to a "Failed Intake" sheet with the raw webhook data so no lead is ever lost

**Final state: 12-node workflow with AI scoring, branching, HubSpot sync, Slack, Gmail, and Sheets.**

---

**n8n Workflow 2: "Closed Won → Full Revenue Event" (refined from Day 35)**
Triggered by HubSpot webhook when a deal reaches Closed Won.

Complete node sequence:
1. Webhook (from HubSpot workflow action)
2. HubSpot: Get full contact + deal data
3. Parallel execution (4 branches using n8n's parallel branching):
   - Branch A: Slack #wins celebration message with full deal details
   - Branch B: Gmail welcome email to new client
   - Branch C: Google Sheets revenue tracker log entry
   - Branch D: HubSpot — create 5 onboarding tasks with date calculations
4. Merge node
5. Google Sheets: Update "Active Client Roster" with new client row
6. OpenAI: Generate a personalized onboarding tip based on the services purchased
7. Gmail: Send onboarding tip to assigned account manager

Refinements:
- Add AI-generated onboarding tip (new)
- Add Active Client Roster update (new)
- Ensure parallel branches run simultaneously (confirm no sequential bottleneck)

---

**n8n Workflow 3: "Monthly Revenue Report Generator" (refined from Day 33)**
Runs on the 1st of every month.

Complete node sequence:
1. Schedule trigger: 1st of month, 9:00 AM
2. Google Sheets: Read "GrowthBridge Revenue Tracker" — last month's data
3. Google Sheets: Read "Active Client Roster" — current client list
4. Code node: Calculate month-over-month metrics
   - Total revenue this month vs. last month
   - New clients added
   - Clients churned
   - Average retainer value
   - Top 3 clients by revenue
5. OpenAI: Generate executive summary paragraph
   - "Based on these metrics, write a 3-sentence executive summary for the GrowthBridge leadership team. Be specific, use the actual numbers."
6. HubSpot: Create a "Report Ready" task for Admin: "Monthly report generated — review and send to leadership"
7. Gmail: Send full report to leadership (formatted HTML email)
   - Revenue summary table
   - AI executive summary
   - Client additions/churn
   - Top clients
   - Month-over-month % change with green/red indicators
8. Slack: Post abbreviated summary to #leadership channel
9. Google Sheets: Archive the report in a "Monthly Reports Archive" tab

Refinements from Day 33:
- Add AI executive summary (new)
- Add HubSpot task creation (new)
- Add MoM % change calculations (new)
- Add archive step (new)

---

**n8n Workflow 4: "Client Health Monitor" (new workflow)**
Runs every Monday morning to flag at-risk clients.

Complete node sequence:
1. Schedule trigger: Every Monday, 8:00 AM
2. HubSpot: Get all contacts where Lifecycle Stage = Customer
3. Code node: Filter contacts where Client Health Score < 40 OR NPS Score < 7 OR Last Activity Date > 30 days
4. IF: At-risk contacts found?
   - Yes → continue
   - No → Slack: "✓ All clients healthy this week. No alerts." → End
5. Loop Over Items (one per at-risk client)
6. OpenAI: Generate personalized re-engagement suggestion
   - "Client: {{name}}, Company: {{company}}, Services: {{services}}, Health Score: {{score}}. Suggest 2 specific actions an account manager could take this week to improve this client's experience."
7. Slack: Post per-client alert to #client-health channel
   - Client name, health score, NPS, last activity, AM name, AI suggestions
8. HubSpot: Create task for assigned AM (one per at-risk client)
9. After loop: Google Sheets log of all at-risk clients this week with AI suggestions

---

**n8n Workflow 5: "AI Weekly Briefing for Leadership" (new workflow)**
Every Friday at 5:00 PM — automated week-in-review.

Complete node sequence:
1. Schedule trigger: Every Friday, 5:00 PM
2. HubSpot: Get week's deal activity (deals created, moved, closed — use HubSpot API filter by date)
3. HubSpot: Get week's lead activity (contacts created this week)
4. Google Sheets: Get week's support tickets (from support log)
5. Code node: Compile all metrics into a single data object
   - Leads this week, MQLs, demos booked, deals closed, revenue, support tickets, resolution rate
6. OpenAI: Generate weekly narrative
   - "Write a professional 4-sentence weekly summary for a digital marketing agency CEO. Include specific numbers. Highlight wins. Flag one concern if metrics warrant it."
7. Gmail: Send "GrowthBridge Weekly Briefing" to leadership
   - Formatted HTML with metrics table + AI narrative + next week's pipeline preview
8. Slack: Post abbreviated version to #leadership

---

**Integration Test — Run the Full System End-to-End:**

Scenario: A new lead comes in for GrowthBridge.

Step by step, trace the lead through the entire system:
1. Submit a test form → n8n Workflow 1 fires → Lead created in HubSpot
2. HubSpot Workflow 1 fires (New Lead Routing) → task created, AM assigned
3. Simulate engagement → HubSpot Score increases → Workflow 2 fires (MQL Alert)
4. Manually create a deal → HubSpot Workflow 3 fires (Deal Checklist)
5. Move deal to Closed Won → HubSpot Workflow 5 fires → n8n Workflow 2 fires simultaneously
6. New client onboarded → Client Health workflow monitors them the next Monday

Document every step in an "End-to-End System Test Log" (Google Sheets).

### Deliverable
5 production n8n workflows + end-to-end system integration test with documented log.

### Portfolio Artifact
- Screenshot: n8n workflow list showing all 5 workflows
- Screenshot: Each workflow canvas (5 full screenshots)
- Screenshot: End-to-End System Test Log (Google Sheets)
- Screenshot: Full parallel branches in Workflow 2
- Export all 5 workflows as JSON files
- Save to: `/Capstone Project/n8n Automations/`

### Success Criteria
- [ ] All 5 n8n workflows execute without errors
- [ ] Workflow 1 correctly routes to priority vs. standard based on AI score
- [ ] Workflow 3 generates a unique AI executive summary each run
- [ ] End-to-end test successfully traces a lead through all 6 touchpoints
- [ ] System Test Log shows all 6 steps as "PASS"

### Estimated Time: 5 hours

---

# ═══════════════════════════════════════════
# DAY 44: EXECUTIVE REPORTING SUITE
# ═══════════════════════════════════════════

## DAY 44

### Objective
Build the complete executive reporting suite — 3 HubSpot dashboards covering revenue, marketing, and client health. Produce a written analytics report that demonstrates strategic thinking, not just data literacy.

### Real-World Context
The CEO of GrowthBridge doesn't log into HubSpot to check reports. They get a weekly email and check a dashboard on their phone. A RevOps specialist who builds dashboards that give leadership clear answers — not raw data — is the person who gets promoted and rehired. This is what separates "dashboard builders" from "data storytellers."

### Main Project Task — Part 1: Build the 3 Executive Dashboards

**Dashboard 1: GrowthBridge Revenue Command Center**
(Primary dashboard — viewed by CEO and Sales Lead daily)

Reports:
1. Monthly Recurring Revenue (MRR) — sum of Monthly Retainer Value for all active clients
2. New MRR This Month — sum of new clients' retainer values
3. MRR Churn Risk — sum of retainer values for at-risk clients (Health Score < 30)
4. Pipeline Value (Weighted) — sum of weighted deal values across all pipelines
5. New Business Pipeline Conversion Funnel — stage-by-stage % conversion
6. Revenue by Service Package — breakdown of MRR by service type
7. Deals Closed This Month (count and value)
8. Average Deal Value — new business pipeline
9. Sales Cycle Length — average days from deal creation to close
10. Month-over-Month Revenue Growth — % change vs. last month

**Dashboard 2: GrowthBridge Marketing Intelligence**
(Viewed by Marketing Manager weekly)

Reports:
1. New Leads Created by Source — this month (bar chart)
2. MQL Volume — contacts reaching MQL threshold this month
3. Lead-to-MQL Rate — % of leads that become MQLs
4. MQL-to-Demo Rate — % of MQLs that get a demo booked
5. Email Nurture Performance — open rate + click rate for all 5 nurture emails
6. Form Submission Volume by Form — which lead magnets are working
7. Lead Quality Distribution — HubSpot Score distribution across all leads
8. Landing Page Conversion Rate — form views vs. submissions
9. Cost Per Lead by Source (manually calculated — add as text note on report)
10. Marketing-Sourced Revenue — Closed Won deals where original source = marketing

**Dashboard 3: GrowthBridge Client Health & Retention**
(Viewed by Account Management team weekly)

Reports:
1. Client Health Score Distribution — all clients segmented by score range
2. At-Risk Clients — table showing clients with Health Score < 40
3. NPS Score Average — across all active clients
4. NPS by Service Package — does Full Service have higher NPS than SEO Only?
5. Support Ticket Volume by Client — which clients are submitting the most tickets?
6. Contract Renewals in Next 60 Days — table showing upcoming renewals + value
7. Client Retention Rate — (clients at end of period / clients at start) × 100
8. Upsell Candidates — clients who are Upsell Candidate = True
9. Average Client Tenure — average months since Client Since date
10. Churned Clients This Quarter — count and lost MRR

---

### Main Project Task — Part 2: Write the Analytics Report

**"GrowthBridge Agency — Q1 Revenue Operations Analysis"**
(Google Docs — 8–10 pages, professionally formatted with a cover page)

**Cover Page:**
- Report Title
- Prepared By: [Your Name]
- Date: [Current Date]
- Prepared For: GrowthBridge Agency Leadership

**Section 1: Executive Summary** (half page)
- 3–4 sentence narrative summary of overall business health
- 3 key findings
- 1 critical recommendation

**Section 2: Revenue Analysis** (1 page)
- Current MRR
- Growth rate
- Pipeline coverage ratio (weighted pipeline / quarterly revenue target)
- Revenue by service type analysis
- What's working, what's at risk

**Section 3: Lead Generation & Marketing** (1 page)
- Lead volume and quality analysis
- Best-performing lead sources
- Nurture sequence performance
- MQL rate and what's driving it
- Recommendation: where to invest more

**Section 4: Sales Performance** (1 page)
- Win rate
- Average deal value
- Sales cycle length
- Stage-by-stage conversion analysis
- Bottleneck identification: which stage has the highest drop-off?

**Section 5: Client Health & Retention** (1 page)
- Overall health score distribution
- At-risk client breakdown
- NPS analysis
- Renewal pipeline value
- Churn risk assessment

**Section 6: Automation ROI** (half page)
Estimate the time saved by each automation:
| Automation | Manual Time | Automated Time | Hours Saved/Month |
|---|---|---|---|
| Lead intake routing | 15 min/lead × 30 leads | 0 | 7.5 hours |
| Monthly reporting | 3 hrs × 10 clients | 0 | 30 hours |
| Client onboarding | 3 days → 2 hours | 2 hours | ~50 hours |
| ... | ... | ... | ... |
Total estimated monthly time savings: ___
At $50/hr operations cost: $___/month saved

**Section 7: Top 3 Strategic Recommendations** (1 page)
For each recommendation:
- What: specific action
- Why: data that supports it
- How: implementation steps in HubSpot/n8n
- Expected impact: measurable outcome

**Section 8: 90-Day Roadmap** (half page)
Month 2 and Month 3 priorities — what to build next to continue scaling the system

### Deliverable
3 HubSpot dashboards (30 reports total) + full Analytics Report document.

### Portfolio Artifact
- Screenshot: All 3 dashboards (full-page screenshots)
- Export Analytics Report as a professionally formatted PDF
- Screenshot: Most complex report (conversion funnel or health score distribution)
- Loom video (10 min): "GrowthBridge Revenue System — Executive Dashboard Presentation"
  Record yourself presenting the dashboards as if you're in a board meeting with the GrowthBridge CEO
  Language: "What this tells us is...", "The risk here is...", "My recommendation is..."
- Save to: `/Capstone Project/Reports/`

### Success Criteria
- [ ] All 3 dashboards have 10 reports each, all populated with data
- [ ] Analytics report has all 8 sections complete with real data references
- [ ] Automation ROI section includes specific time savings per workflow
- [ ] Loom video uses executive/strategic language throughout
- [ ] PDF is formatted professionally (cover page, headers, tables)

### Estimated Time: 5 hours

---

# ═══════════════════════════════════════════
# DAY 45: FINAL DOCUMENTATION + PORTFOLIO PACKAGING
# ═══════════════════════════════════════════

## DAY 45

### Objective
Package the entire capstone project into a deployment-ready deliverable — final documentation, system handoff, portfolio folder organization, and a showcase presentation. This is your graduation day.

### Real-World Context
The difference between a developer who "finishes features" and a consultant who "closes engagements" is documentation and presentation. On Day 45, you're closing the GrowthBridge engagement. You're delivering a system that another professional could maintain without you, expand without breaking things, and trust completely. That professional polish is what turns a portfolio into job offers.

---

### Main Project Task — Part 1: Final System Documentation

**Document 1: GrowthBridge Revenue System — Client Handoff Package**
This is the master delivery document. Professional format, cover page, table of contents.

Table of Contents:
1. Project Overview
2. System Architecture Summary
3. HubSpot Configuration Guide
4. Workflow Reference Guide (HubSpot)
5. n8n Workflow Reference Guide
6. Dashboard Reference Guide
7. Data Governance Policy
8. Admin Playbook
9. Maintenance Schedule
10. Escalation & Support Guide
11. 90-Day Next Steps Roadmap
12. Appendix: Screenshots & Exports

**Section 3: HubSpot Configuration Guide**
For each configured element: what it is, where to find it, what to never change without consulting the admin.

**Section 4: HubSpot Workflow Reference**
For each of the 8 workflows:
| Workflow | Trigger | Actions | Owner | Re-enrollment |
One-paragraph business description of each.

**Section 5: n8n Workflow Reference**
For each of the 5 n8n workflows:
- Name, trigger, apps connected, business purpose, average execution time
- Link to exported .json file
- Troubleshooting tips

**Section 7: Data Governance Policy**
- Required fields checklist for contacts/deals/tickets
- Naming conventions
- Duplicate handling protocol
- Monthly audit checklist
- Who owns data quality

**Section 8: Admin Playbook**
Step-by-step guides for the 10 most common admin tasks:
1. How to add a new team member in HubSpot
2. How to create a new list
3. How to add a new pipeline stage
4. How to check if a workflow is running correctly
5. How to re-activate a paused n8n workflow
6. How to troubleshoot a failed import
7. How to merge duplicate contacts
8. How to run the monthly data audit
9. How to generate the monthly revenue report
10. How to offboard a churned client

**Section 9: Maintenance Schedule**
| Frequency | Task | Owner | Est. Time |
|---|---|---|---|
| Weekly | Review at-risk client alerts | Account Managers | 20 min |
| Weekly | Check workflow execution logs | Admin | 15 min |
| Monthly | Data quality audit | Admin | 1 hour |
| Monthly | Review and archive reports | RevOps | 30 min |
| Quarterly | Audit scoring model (still accurate?) | RevOps | 1 hour |
| Quarterly | Review pipeline stages (still relevant?) | Sales Lead | 30 min |
| Annually | Full system architecture review | Admin | 2 hours |

---

### Main Project Task — Part 2: Final CRM Health Audit

Run through this complete checklist and document every result:

**HubSpot Health Checklist:**
- [ ] All contacts have lifecycle stage assigned
- [ ] All contacts have an assigned owner
- [ ] No contacts with duplicate email addresses
- [ ] All deals have an amount, close date, and associated contact
- [ ] All 8 workflows are ON status
- [ ] No workflows showing error states in execution log
- [ ] All active lists are updating (check "Last updated" timestamp)
- [ ] All dashboards loading with current data
- [ ] All forms have correct redirect/thank-you actions
- [ ] Property groups are organized (no orphaned properties)

**n8n Health Checklist:**
- [ ] All 5 workflows are active (not paused)
- [ ] All credentials are valid (HubSpot, Google Sheets, Gmail, Slack, OpenAI)
- [ ] Last execution of each workflow shows success
- [ ] Webhook URLs are saved in the documentation
- [ ] Workflow exports (.json) are saved and up to date

**Data Quality Checklist:**
- [ ] No contacts in multiple conflicting lifecycle stages
- [ ] All "Client Since" dates are accurate
- [ ] All "Contract Renewal Dates" are set for active clients
- [ ] Monthly Retainer Value populated for all Customer contacts
- [ ] NPS Scores present for at least 80% of Customer contacts

---

### Main Project Task — Part 3: Portfolio Organization

Organize your complete portfolio folder structure:

```
/GrowthBridge Capstone Project/
  /Architecture/
    - GrowthBridge-Revenue-System-Architecture-v1.pdf
    - Integration-Map-Diagram.png
    - System-Overview-1-Pager.pdf (Canva)
  /HubSpot Automations/
    - Workflow-1-Lead-Routing.png (screenshot)
    - Workflow-2-MQL-Alert.png
    - Workflow-3-Deal-Checklist.png
    - Workflow-4-Nurture-Sequence.png
    - Workflow-5-Closed-Won.png
    - Workflow-6-Health-Monitor.png
    - Workflow-7-Renewal-Alerts.png
    - Workflow-8-Upsell-Trigger.png
    - Workflow-Testing-Log.xlsx
  /n8n Automations/
    - n8n-workflow-1-lead-intake.json
    - n8n-workflow-2-closed-won.json
    - n8n-workflow-3-monthly-report.json
    - n8n-workflow-4-health-monitor.json
    - n8n-workflow-5-weekly-briefing.json
    - All workflow canvas screenshots (5 .png files)
    - n8n-architecture-diagram.png
  /Reports/
    - Revenue-Command-Center-Screenshot.png
    - Marketing-Intelligence-Screenshot.png
    - Client-Health-Dashboard-Screenshot.png
    - GrowthBridge-Q1-RevOps-Analysis.pdf
  /Documentation/
    - GrowthBridge-Client-Handoff-Package.pdf
    - Data-Governance-Policy.pdf
    - Admin-Playbook.pdf
    - Maintenance-Schedule.pdf
  /System-Test-Evidence/
    - End-to-End-Test-Log.xlsx
    - CRM-Health-Audit-Checklist.pdf
    - Workflow-Testing-Log.xlsx
  /Videos/
    - README.md (links to all Loom videos)
    - Loom: Executive Dashboard Presentation (10 min)
    - Loom: System Architecture Walkthrough (8 min)
    - Loom: n8n Automation Demo (8 min)
    - Loom: Full System Tour (15 min)
```

---

### Main Project Task — Part 4: Capstone Showcase Presentation

**Create a "Capstone Showcase Deck" in Canva (8–10 slides)**

Slide 1: Cover
"GrowthBridge Revenue System"
Your Name | CRM Architect & Automation Engineer | [Date]

Slide 2: The Problem
What GrowthBridge was dealing with before: manual work, slow onboarding, no visibility, inconsistent follow-up.
Use before/after comparison.

Slide 3: The Solution — System Overview
One-page architecture diagram. Brief bullets on what was built.

Slide 4: HubSpot Configuration
Key stats: X contacts, X custom properties, X pipelines, X workflows, X certifications earned

Slide 5: Automation Highlights
Top 3 most impactful workflows — what they do, what they automate, time saved

Slide 6: AI Integration
The 2 AI-powered workflows — lead qualification agent and content assistant. What GPT-4 does inside each.

Slide 7: Reporting Suite
Dashboard screenshots (3 side by side). "Leadership now has real-time visibility into revenue, marketing, and client health."

Slide 8: Results & ROI
Estimated time saved per month, manual processes eliminated, what this enables at 2× scale.

Slide 9: Certifications Earned
List all 6 HubSpot certifications with dates. Logo bar.

Slide 10: What I Can Build For You
"If you're a company that needs [this], I can build [this]."
Clear call to action: LinkedIn / Email / Portfolio link

**Record a final Loom Video (15 min): "Full GrowthBridge System Walkthrough"**
Cover:
- Open the Capstone Showcase deck and narrate slides 1–3 (3 min)
- Live HubSpot demo: show pipelines, active workflows, dashboards (5 min)
- Live n8n demo: show 2 workflows executing (4 min)
- Close: "This is what I'm capable of building — here's what I'd do for your company" (3 min)

### Deliverable
Complete portfolio folder + Client Handoff Package + CRM Health Audit + Showcase Deck + Loom walkthrough.

### Portfolio Artifact
Everything in the folder structure above, fully organized and ready to share.

**FINAL ARTIFACT: Create a single PDF "Portfolio Index"**
One-page document listing every artifact in your portfolio with:
- File name
- What it is
- Which project it's from
- Location in folder structure

This is the document you attach to job applications alongside your resume.

### Success Criteria
- [ ] Client Handoff Package has all 12 sections complete
- [ ] CRM Health Audit checklist shows 100% pass (fix anything that fails)
- [ ] n8n Health Audit shows all 5 workflows active with valid credentials
- [ ] Portfolio folder has at least 30 distinct artifacts
- [ ] Capstone Showcase Deck has all 10 slides complete
- [ ] Final Loom video is 12–18 minutes and covers all 4 sections
- [ ] Portfolio Index PDF lists all artifacts
- [ ] You feel genuinely proud of what you built

### Estimated Time: 5 hours

---

# ═══════════════════════════════════════════
# CAPSTONE COMPLETION SUMMARY
# ═══════════════════════════════════════════

## What You Built in 5 Days

| Deliverable | Count |
|---|---|
| HubSpot production workflows | 8 |
| n8n production workflows | 5 |
| HubSpot dashboards | 3 |
| Dashboard reports | 30 |
| Documentation documents | 10+ |
| System test evidence files | 3 |
| Loom videos (total program) | 8+ |
| Canva diagrams | 4+ |
| Architecture sections | 12 |
| Portfolio artifacts | 30+ |

## What You Can Now Say in an Interview

- "I built a complete lead-to-renewal automation system for a marketing agency using HubSpot and n8n"
- "I designed the CRM architecture before building it and delivered deployment-ready documentation"
- "I integrated OpenAI into 2 production workflows for lead qualification and content generation"
- "I built a parallel-branch client onboarding system that reduces onboarding time from 3 days to 2 hours"
- "I produced executive reporting dashboards that give leadership real-time revenue, marketing, and retention visibility"
- "I hold 6 HubSpot certifications including CRM, Marketing, Sales, Service, Revenue Operations, and Reporting"

## The Capstone as a Job Application Asset

When applying for roles, you can say:
- "My portfolio demonstrates an end-to-end revenue system built on HubSpot + n8n for a digital marketing agency"
- Attach: Architecture PDF + Loom walkthrough link
- Reference: Specific workflows by name to answer technical interview questions
