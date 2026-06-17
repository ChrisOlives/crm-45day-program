# 45-Day CRM & Automation Career Shift Program
### Complete Curriculum — Google Docs Version
**How to use:** Copy this entire file → Open Google Docs → Paste. Use Format > Paragraph Styles to apply headings. Share the doc with yourself across devices.

---

# SECTION 1: LEARNING STRATEGY

## Why HubSpot 32 Days + n8n 13 Days

90% of CRM job postings require HubSpot. n8n adds differentiation and unlocks higher-paying automation roles. This split maximises employability speed while building a genuinely rare skill combination.

## The 5 Business Scenarios

| # | Company | Type | Days |
|---|---|---|---|
| 1 | BrightClean Services | Local cleaning company | 1–8 |
| 2 | NovaNest Realty | Real estate agency | 9–15 |
| 3 | Stackr SaaS | B2B project management software | 16–24 |
| 4 | PulseCart | E-commerce fitness brand | 25–30 |
| 5 | GrowthBridge Agency | Digital marketing agency | 31–45 |

## Daily Time Investment

| Block | Time |
|---|---|
| Mini Theory | 10 min |
| Hands-On Exercise | 30–45 min |
| Main Project Task | 60–90 min |
| Portfolio Documentation | 15–20 min |
| **Total** | **~2–2.5 hours/day** |

## Certifications Timeline

| Certification | Target Day |
|---|---|
| HubSpot CRM | Day 7 |
| HubSpot Marketing Software | Day 14 |
| HubSpot Sales Software | Day 21 |
| HubSpot Revenue Operations | Day 24 |
| HubSpot Service Hub | Day 28 |
| HubSpot Reporting | Day 30 |

---

# SECTION 2: 45-DAY ROADMAP AT A GLANCE

## Phase 1 — HubSpot Foundations (Days 1–8)
**Company:** BrightClean Services
Account setup → Properties → Pipeline → Import → Lifecycle → Workflows → Dashboards → Documentation

## Phase 2 — Marketing Hub (Days 9–15)
**Company:** NovaNest Realty
Forms → Landing pages → Nurture sequences → Lead scoring → Segmentation → Deal pipelines → Dashboards → Handoff

## Phase 3 — Sales Hub + RevOps (Days 16–24)
**Company:** Stackr SaaS
Lifecycle architecture → SaaS pipelines → Sequences → Onboarding/Churn → Lead scoring → Data cleanup → Migration → RevOps report

## Phase 4 — Service Hub + Operations (Days 25–30)
**Company:** PulseCart
Ticketing → E-commerce segmentation → Operations Hub → Service dashboards → Attribution → Documentation

## Phase 5 — n8n Automation (Days 31–40)
**Company:** GrowthBridge Agency
Foundations → Lead intake → Reporting → AI qualification → Deal automations → Support triage → Enrichment → Onboarding → AI campaigns → Documentation

## Phase 6 — Capstone Project (Days 41–45)
**Company:** GrowthBridge Agency (full system)
Architecture → 8 HubSpot workflows → 5 n8n workflows → 3 executive dashboards → Full documentation

---

# SECTION 3: DAILY BREAKDOWN — PHASE 1 (Days 1–8)
## BrightClean Services

---

## Day 1 — Account Setup & Company Configuration
**Objective:** Configure a production-quality HubSpot account for BrightClean Services.
**Company:** BrightClean Services | **Time:** 2 hours

**Tasks:**
- [ ] Create HubSpot free account at hubspot.com/crm
- [ ] Set company name = "BrightClean Services", upload logo, set timezone
- [ ] Remove all HubSpot demo/sample data
- [ ] Create 3 users: Admin (you), Sarah Kim (Sales Rep), Marcus Johnson (Operations)
- [ ] Create 2 Teams: Sales Team, Operations Team

**Deliverable:** Configured HubSpot account with team structure
**Portfolio:** Screenshot of account settings + users/teams page → `/HubSpot Portfolio/CRM Setup/Day01-Account-Setup/`

---

## Day 2 — Custom Property Schema
**Objective:** Design and build all custom properties for BrightClean.
**Company:** BrightClean Services | **Time:** 2 hours

**Tasks:**
- [ ] Create property group: "BrightClean Service Info"
- [ ] Build 10 custom Contact properties (Service Type, Frequency, Preferred Day, Property Size, Last/Next Service Date, Has Referred, Review Requested, Review Left, Lead Source Detail)
- [ ] Create property group: "BrightClean Deal Info"
- [ ] Build 6 custom Deal properties (Job Type, Duration, Address, Assigned Cleaner, Quote Sent Date, Deposit Collected)
- [ ] Export full property list as CSV

**Deliverable:** 16 custom properties in named groups
**Portfolio:** Property list screenshots + exported CSV → `/HubSpot Portfolio/CRM Setup/Day02-Property-Schema/`

---

## Day 3 — Sales Pipeline + Deal Stages
**Objective:** Build an 8-stage service pipeline with correct probabilities and required fields.
**Company:** BrightClean Services | **Time:** 2.5 hours

**Pipeline Stages:** New Inquiry (10%) → Quote Requested (20%) → Quote Sent (40%) → Follow-Up Sent (50%) → Booked (80%) → Job Completed (90%) → Closed Won (100%) → Closed Lost (0%)

**Tasks:**
- [ ] Rename default pipeline to "BrightClean Service Pipeline"
- [ ] Build all 8 stages with correct probabilities
- [ ] Set required properties for stage transitions (Quote Sent, Booked, Closed Won)
- [ ] Create 8 sample deals across multiple stages

**Deliverable:** Complete pipeline + 8 sample deals
**Portfolio:** Pipeline settings screenshot + deal board screenshot → `/HubSpot Portfolio/CRM Setup/Day03-Pipeline/`

---

## Day 4 — Contact Import & Data Migration
**Objective:** Import 40 contacts from CSV with custom field mapping.
**Company:** BrightClean Services | **Time:** 2.5 hours

**Tasks:**
- [ ] Build 40-contact CSV in Google Sheets with custom columns
- [ ] Import via HubSpot import wizard, map all custom fields
- [ ] Create 10 Company records and associate with contacts
- [ ] Verify import with zero errors

**Deliverable:** 40 contacts + 10 companies in HubSpot
**Portfolio:** Contacts list + import summary screenshot → `/HubSpot Portfolio/CRM Setup/Day04-Data-Import/`

---

## Day 5 — Lifecycle Stages + Segmentation Lists
**Objective:** Assign lifecycle stages to all contacts and build 8 segmentation lists.
**Company:** BrightClean Services | **Time:** 2.5 hours

**Tasks:**
- [ ] Bulk-assign lifecycle stages to all 40 contacts (25 Customer, 7 Lead, 5 Opportunity, 3 Evangelist)
- [ ] Set Lead Status on 7 lead contacts
- [ ] Build 6 Active Lists (All Active Customers, Recurring Clients, Commercial Clients, Referral Sources, Unbooked Leads, Large Properties)
- [ ] Build 2 Static Lists (Q1 New Customers, VIP Commercial Accounts)

**Deliverable:** All contacts staged + 8 lists built
**Portfolio:** Lists view screenshot + lifecycle diagram (Canva) → `/HubSpot Portfolio/CRM Setup/Day05-Lifecycle-Lists/`

---

## Day 6 — Core Automation Workflows (3)
**Objective:** Build BrightClean's 3 core operational workflows.
**Company:** BrightClean Services | **Time:** 3 hours

**Workflow 1:** New Lead Notification → internal email + task + set Lead Status
**Workflow 2:** Post-Service Review Request → 24hr delay + review email + task
**Workflow 3:** Recurring Client Reminder → 7 days before Next Service Date

**Tasks:**
- [ ] Build all 3 workflows with correct triggers and actions
- [ ] Turn all 3 ON
- [ ] Test each with a live contact enrollment
- [ ] Verify task creation and email sending in execution logs

**Deliverable:** 3 live, tested workflows
**Portfolio:** Workflow canvas screenshots + execution logs → `/HubSpot Portfolio/Automations/Day06-Core-Workflows/`

---

## Day 7 — Dashboards + HubSpot CRM Certification ·
**Objective:** Build 2 reporting dashboards and earn HubSpot CRM Certification.
**Company:** BrightClean Services | **Time:** 3 hours

**Dashboard 1 (8 reports):** Pipeline value by stage, deals closed this month, close rate, average deal value, lead-to-customer funnel, contacts by service type, recurring vs. one-time, tasks completed

**Dashboard 2 (3 reports):** Deals created this month, open deals by owner, deals by close date

**Tasks:**
- [ ] Build both dashboards with all reports populated
- [ ] Record Loom video (5–7 min) walking through dashboards
- [ ] Complete HubSpot CRM Certification at academy.hubspot.com
- [ ] Add certification to LinkedIn

**Deliverable:** 2 dashboards + certification earned
**Portfolio:** Dashboard screenshots + Loom link → `/HubSpot Portfolio/Reports/Day07-Dashboards/`

---

## Day 8 — Full Documentation Package
**Objective:** Produce 4 deployment-quality documentation documents.
**Company:** BrightClean Services | **Time:** 2.5 hours

**Documents to produce:**
1. Data Dictionary (Google Sheets) — all 16 properties with descriptions and accepted values
2. Pipeline SOP (Google Docs) — stage definitions, entry/exit criteria, deal naming convention
3. Workflow Documentation — admin reference for all 3 workflows
4. Admin Setup Checklist — full rebuild reference

**Tasks:**
- [ ] Write all 4 documents
- [ ] Export all as PDFs with clean formatting

**Deliverable:** 4 complete documentation documents
**Portfolio:** All 4 PDFs → `/HubSpot Portfolio/Documentation/Day08-BrightClean-CRM-Docs/`

---

# SECTION 3 CONTINUED: PHASE 2 (Days 9–15)
## NovaNest Realty

---

## Day 9 — Landing Pages, Forms & Lead Capture
**Objective:** Build 3 forms and 1 landing page for real estate lead capture.
**Company:** NovaNest Realty | **Time:** 3 hours

**Tasks:**
- [ ] Create 6 NovaNest custom contact properties
- [ ] Build Form 1: Buyer Consultation Request (8 fields)
- [ ] Build Form 2: Free Home Valuation Request (6 fields)
- [ ] Build Form 3: Open House Sign-In Sheet (6 fields)
- [ ] Build landing page: "Get Your Free Home Valuation" with Form 2 embedded

**Deliverable:** 3 live forms + 1 published landing page
**Portfolio:** Form screenshots + landing page preview → `/HubSpot Portfolio/CRM Setup/Day09-NovaNest-Lead-Capture/`

---

## Day 10 — 5-Email Buyer Nurture Sequence
**Objective:** Write, build, and automate a 5-email buyer nurture sequence.
**Company:** NovaNest Realty | **Time:** 3.5 hours

**Email schedule:** Day 0 (Welcome) → Day 3 (Market Update) → Day 7 (Buyer Mistakes) → Day 14 (Social Proof) → Day 30 (Re-engagement)

**Tasks:**
- [ ] Write and build all 5 emails with personalization tokens
- [ ] Build enrollment workflow triggered by Buyer Consultation form
- [ ] Set correct delays between all emails
- [ ] Test by enrolling a contact and verifying Email 1 sends

**Deliverable:** 5 emails + workflow live
**Portfolio:** Email screenshots + workflow canvas → `/HubSpot Portfolio/Automations/Day10-Buyer-Nurture-Sequence/`

---

## Day 11 — Lead Scoring Model + MQL Alert
**Objective:** Build NovaNest's lead scoring model with 11+ attributes and an MQL alert workflow.
**Company:** NovaNest Realty | **Time:** 3 hours

**MQL Threshold:** 40 points | **Key signals:** Form submissions (+20/+25), Timeline urgency (+15/+20), Pre-Approved (+25), Email engagement (+5/+10)

**Tasks:**
- [ ] Configure HubSpot Score with 8+ positive attributes
- [ ] Add 4 negative score attributes
- [ ] Build MQL Alert workflow with 4-hour SLA escalation
- [ ] Verify 5+ contacts reach MQL threshold
- [ ] Write Lead Scoring Model PDF document

**Deliverable:** Functional scoring model + MQL workflow
**Portfolio:** Score editor screenshots + MQL workflow + PDF → `/HubSpot Portfolio/CRM Setup/Day11-Lead-Scoring/`

---

## Day 12 — Advanced Segmentation + Seller Nurture
**Objective:** Build 10 active lists and a 3-email seller nurture sequence.
**Company:** NovaNest Realty | **Time:** 3 hours

**Tasks:**
- [ ] Build 10 active lists using AND/OR logic (Hot Buyer Leads, Seller Leads, Pre-Approved, Budget Over $500K, Urgent Timeline, Cold Leads, MQL Not in Pipeline, Email Engaged, Unengaged, Neighborhood)
- [ ] Write and build 3 seller nurture emails
- [ ] Build Seller Nurture workflow triggered by Home Valuation form
- [ ] Verify all 10 lists have members

**Deliverable:** 10 active lists + seller nurture sequence
**Portfolio:** Lists screenshot + workflow canvas → `/HubSpot Portfolio/Automations/Day12-Segmentation-Seller-Nurture/`

---

## Day 13 — Deal Pipelines + Deal Automation (3 Workflows)
**Objective:** Build 2 NovaNest pipelines and automate deal progression.
**Company:** NovaNest Realty | **Time:** 3 hours

**Pipelines:** Buyer Pipeline (7 stages) + Seller Pipeline (7 stages)
**Workflows:** A) New Inquiry → Deal Creation | B) Consultation Scheduled Checklist | C) Under Contract Closing Checklist (5 tasks)

**Tasks:**
- [ ] Build both pipelines with correct stages and probabilities
- [ ] Build all 3 deal automation workflows
- [ ] Create 10 sample deals across both pipelines

**Deliverable:** 2 pipelines + 3 workflows + 10 sample deals
**Portfolio:** Pipeline settings + workflow canvases → `/HubSpot Portfolio/CRM Setup/Day13-NovaNest-Pipelines/`

---

## Day 14 — Dashboards + Marketing Software Certification ·
**Objective:** Build 2 NovaNest dashboards and earn HubSpot Marketing Software Certification.
**Company:** NovaNest Realty | **Time:** 3 hours

**Dashboard 1 — Lead Intelligence (6 reports):** Source breakdown, form submissions, buyer vs. seller split, MQL rate, score distribution, email performance
**Dashboard 2 — Pipeline Performance (6 reports):** Deals by stage, closed this month, deal velocity, pipeline by agent, stage conversion funnel, lost deal reasons

**Tasks:**
- [ ] Build both dashboards with all reports populated
- [ ] Record Loom walkthrough (5 min)
- [ ] Complete HubSpot Marketing Software Certification

**Deliverable:** 2 dashboards + certification
**Portfolio:** Dashboard screenshots + Loom → `/HubSpot Portfolio/Reports/Day14-NovaNest-Dashboards/`

---

## Day 15 — System Documentation + Client Handoff
**Objective:** Deliver the full NovaNest CRM handoff package.
**Company:** NovaNest Realty | **Time:** 3 hours

**Documents:**
1. CRM System Overview (9 sections) — account structure, all objects, pipelines, workflows, lists, emails, scoring, dashboards
2. Agent Training Guide — non-technical "how to use it" guide
3. CRM Health Audit — verified checklist of system integrity

**Tasks:**
- [ ] Write all 3 documents
- [ ] Fix any health audit issues found
- [ ] Record Loom: "NovaNest CRM Walkthrough" (8 min) — present as if to the broker

**Deliverable:** 3 documents + health audit + Loom video
**Portfolio:** 3 PDFs + Loom link → `/HubSpot Portfolio/Documentation/Day15-NovaNest-Handoff/`

---

# SECTION 3 CONTINUED: PHASE 3 (Days 16–24)
## Stackr SaaS

---

## Day 16 — SaaS Lifecycle Architecture
**Objective:** Build the MQL→SQL→Opportunity lifecycle system for a B2B SaaS company.
**Company:** Stackr SaaS | **Time:** 3 hours
**Tasks:**
- [ ] Create 16 Stackr custom properties (Current Plan, MRR, Usage Score, Churn Risk, etc.)
- [ ] Write Lifecycle Architecture document (entry/exit criteria per stage)
- [ ] Build MQL→SQL workflow with 4-hour SLA escalation
- [ ] Create 30 Stackr contacts with populated custom properties
**Portfolio:** Properties list + workflow canvas + Architecture PDF → `/HubSpot Portfolio/CRM Setup/Day16-Stackr-Lifecycle/`

---

## Day 17 — SaaS Sales Pipelines + 4 Deal Workflows
**Objective:** Build New Business + Expansion pipelines with full deal automation.
**Company:** Stackr SaaS | **Time:** 3 hours
**Pipelines:** New Business (8 stages) + Expansion (6 stages)
**Workflows:** Demo Request → Auto Assignment | Demo Completed Follow-Up | Stalled Deal Alert | Closed Lost Analysis
**Tasks:**
- [ ] Build both pipelines | [ ] Build all 4 workflows | [ ] Create 15 sample deals
**Portfolio:** Pipeline settings + workflow canvases → `/HubSpot Portfolio/CRM Setup/Day17-Stackr-Pipelines/`

---

## Day 18 — Sales Sequences + Outbound Cadences
**Objective:** Build 3 sales sequences covering free-to-pro conversion, cold re-engagement, and post-demo follow-up.
**Company:** Stackr SaaS | **Time:** 3 hours
**Sequences:** Free-to-Pro (5 steps) | Cold Re-engagement (3 steps) | Post-Demo (5 steps)
**Tasks:**
- [ ] Write all email copy | [ ] Build all 3 sequences | [ ] Test with live enrollment | [ ] Write Sequences Playbook
**Portfolio:** Sequence screenshots + Playbook PDF → `/HubSpot Portfolio/Automations/Day18-Sales-Sequences/`

---

## Day 19 — Customer Onboarding + Churn Prevention
**Objective:** Build 5-email onboarding sequence and churn prevention workflow.
**Company:** Stackr SaaS | **Time:** 3.5 hours
**Tasks:**
- [ ] Write & build 5 onboarding emails (Day 0, 1, 3, 7, 14)
- [ ] Build Onboarding workflow with day-based delays
- [ ] Build Churn Prevention workflow with 24-hour escalation
- [ ] Build Re-engagement workflow for low-usage users
- [ ] Create Customer Journey Map in Canva
**Portfolio:** Email screenshots + workflow canvases + Canva map → `/HubSpot Portfolio/Automations/Day19-Onboarding-Churn-Prevention/`

---

## Day 20 — Two-Dimensional Lead Scoring
**Objective:** Build a fit score + engagement score model with tiered routing.
**Company:** Stackr SaaS | **Time:** 3 hours
**Thresholds:** Hot MQL = Fit ≥ 40 + Engagement ≥ 50 | Standard MQL = Fit ≥ 30 + Engagement ≥ 30
**Tasks:**
- [ ] Build 8+ Fit Score attributes | [ ] Build 6+ Engagement Score attributes
- [ ] Build routing workflow (Hot → Senior Rep, Standard → Junior Rep)
- [ ] Create 3 tiered active lists | [ ] Write ICP + Scoring Model PDF
**Portfolio:** Score editor + routing workflow + PDF → `/HubSpot Portfolio/CRM Setup/Day20-Stackr-Lead-Scoring/`

---

## Day 21 — Sales Performance Dashboards + Sales Certification ·
**Objective:** Build revenue forecast and sales coaching dashboards. Earn Sales Software Certification.
**Company:** Stackr SaaS | **Time:** 3.5 hours
**Dashboard 1 (6 reports):** Revenue forecast, pipeline coverage, deals closing, win rate by stage, avg. sales cycle, revenue by deal type
**Dashboard 2 (6 reports):** Activities by rep, deals by rep, close rate by rep, avg. deal value, deals at risk, stage conversion by rep
**Tasks:**
- [ ] Build both dashboards | [ ] Record Loom (6 min) | [ ] Complete HubSpot Sales Software Certification
**Portfolio:** Dashboard screenshots + Loom → `/HubSpot Portfolio/Reports/Day21-Stackr-Sales-Dashboards/`

---

## Day 22 — Data Cleanup + Governance System
**Objective:** Run a full CRM data audit, fix all issues, and build 3 governance workflows.
**Company:** Stackr SaaS | **Time:** 3 hours
**Tasks:**
- [ ] Build Data Audit spreadsheet (3 tabs: Contacts, Deals, Workflows)
- [ ] Find and merge duplicate contacts
- [ ] Fix contacts with missing lifecycle stages
- [ ] Build 3 governance workflows (Auto-Assign Lifecycle, Incomplete Deal Alert, Stale Contact Flag)
- [ ] Write Data Governance SOP v1.0
**Portfolio:** Before/after screenshots + governance workflows + SOP PDF → `/HubSpot Portfolio/Documentation/Day22-Data-Cleanup-Governance/`

---

## Day 23 — CRM Migration Simulation
**Objective:** Simulate a full Pipedrive → HubSpot migration with field mapping.
**Company:** Stackr SaaS | **Time:** 3.5 hours
**Tasks:**
- [ ] Build 50-row Pipedrive export simulation (with dirty data, duplicates, inconsistent formats)
- [ ] Create full Migration Field Mapping document
- [ ] Clean the data (standardize phones, remove duplicates, split names)
- [ ] Import in correct order: Companies → Contacts → Deals
- [ ] Run post-import audit
**Portfolio:** RAW sheet + Field Mapping PDF + import log screenshot → `/HubSpot Portfolio/CRM Setup/Day23-Migration-Simulation/`

---

## Day 24 — RevOps Report + Revenue Operations Certification ·
**Objective:** Build a RevOps Command Center dashboard and write a full optimization report.
**Company:** Stackr SaaS | **Time:** 3.5 hours
**Dashboard (8 reports):** Full funnel conversion, revenue by source, CAC/LTV estimates, MQL volume, SQL rate, time in stage, marketing-sourced revenue
**Report sections:** Executive Summary, Funnel Analysis, Pipeline Performance, Top 3 Bottlenecks, Recommendations, Quick Wins, 90-Day Roadmap
**Tasks:**
- [ ] Build dashboard | [ ] Write 7-section report with real data | [ ] Complete HubSpot Revenue Operations Certification
**Portfolio:** Dashboard screenshot + RevOps Report PDF → `/HubSpot Portfolio/Reports/Day24-RevOps-Report/`

---

# SECTION 3 CONTINUED: PHASE 4 (Days 25–30)
## PulseCart E-Commerce

---

## Day 25 — Service Hub Ticketing System
**Objective:** Build PulseCart's complete support infrastructure.
**Company:** PulseCart | **Time:** 3 hours
**Pipeline:** New Unassigned → Open → Awaiting Reply → Escalated → Resolved → Closed
**Tasks:**
- [ ] Create 9 PulseCart custom contact properties | [ ] Build support ticketing pipeline (6 stages)
- [ ] Create 4 custom ticket properties | [ ] Build 3 support automation workflows
- [ ] Create 20 sample tickets across stages
**Portfolio:** Pipeline settings + ticket board + workflow canvases → `/HubSpot Portfolio/CRM Setup/Day25-PulseCart-Service-Hub/`

---

## Day 26 — E-Commerce Segmentation + Campaigns
**Objective:** Build RFM-based segmentation and 3 targeted email campaigns.
**Company:** PulseCart | **Time:** 3 hours
**Segments:** VIP, At-Risk, One-Time Buyers, High-Value Cardio, Abandoned Cart, Post-Purchase 30-Day, Repeat Buyers, Lapsed VIPs
**Campaigns:** VIP Early Access | 3-Email Win-Back Sequence | One-Time Buyer Re-Order
**Tasks:**
- [ ] Import 40 PulseCart customers | [ ] Build 8 active lists | [ ] Build all 3 campaigns + workflows | [ ] Create Segmentation Map in Canva
**Portfolio:** Lists screenshot + campaign emails + Canva map → `/HubSpot Portfolio/Automations/Day26-PulseCart-Segmentation/`

---

## Day 27 — Operations Hub: Calculated Properties + Data Integrity
**Objective:** Build calculated properties, customer health score, and 3 data integrity workflows.
**Company:** PulseCart | **Time:** 3 hours
**Calculated Properties:** Days Since Last Order | Average Order Value
**Health Score:** Configures HubSpot Score with PulseCart-specific signals
**Tasks:**
- [ ] Build both calculated properties | [ ] Configure Customer Health Score
- [ ] Build Customer Tier Auto-Assignment workflow (Bronze/Silver/Gold/VIP)
- [ ] Build Abandoned Cart workflow | [ ] Build Post-Purchase Tier Upgrade Alert
**Portfolio:** Calculated property screenshots + tier assignment workflow → `/HubSpot Portfolio/CRM Setup/Day27-PulseCart-Operations-Hub/`

---

## Day 28 — Service Dashboards + Service Hub Certification ·
**Objective:** Build PulseCart's customer success dashboard. Earn Service Hub Certification.
**Company:** PulseCart | **Time:** 3 hours
**Dashboard (10 reports):** Ticket volume, issues by category, avg. resolution time, first response rate, tickets by priority, open by assignee, satisfaction by issue type, repeat ticket rate, refund rate, health score distribution
**Tasks:**
- [ ] Build dashboard with all 10 reports | [ ] Record Loom (4 min) | [ ] Complete HubSpot Service Hub Certification
**Portfolio:** Dashboard screenshot + Loom → `/HubSpot Portfolio/Reports/Day28-PulseCart-Service-Dashboard/`

---

## Day 29 — Marketing Attribution Reports
**Objective:** Build 3 attribution models and a full marketing ROI dashboard.
**Company:** PulseCart | **Time:** 3 hours
**Attribution Models:** First Touch | Last Touch | Linear
**Dashboard (6 reports):** New contacts by source, email campaign performance, lead-to-customer rate by source, campaign-attributed revenue, list growth over time, win-back campaign performance
**Tasks:**
- [ ] Build all 3 attribution reports | [ ] Build Marketing ROI Dashboard | [ ] Write Attribution Analysis document with recommendations
**Portfolio:** Attribution screenshots + Marketing ROI dashboard + Analysis PDF → `/HubSpot Portfolio/Reports/Day29-PulseCart-Attribution/`

---

## Day 30 — Final Documentation + Reporting Certification ·
**Objective:** Deliver the PulseCart handoff package. Earn HubSpot Reporting Certification.
**Company:** PulseCart | **Time:** 3 hours
**Documents:** PulseCart System Overview (9 sections) | Admin Playbook | 90-Day Roadmap
**Tasks:**
- [ ] Run and document full CRM health audit | [ ] Write all 3 documents
- [ ] Create PulseCart 1-pager in Canva | [ ] Record Loom: Full PulseCart System Tour (8 min)
- [ ] Complete HubSpot Reporting Certification
**Portfolio:** 3 PDFs + Canva 1-pager + Loom → `/HubSpot Portfolio/Documentation/Day30-PulseCart-Handoff/`

---

# SECTION 3 CONTINUED: PHASE 5 (Days 31–40)
## n8n Automation Engineering — GrowthBridge Agency

---

## Day 31 — n8n Setup + Foundation Workflows
**Objective:** Install n8n. Build 3 workflows covering API requests, webhooks, and scheduled triggers.
**Company:** GrowthBridge Agency | **Time:** 3 hours | **Tool:** n8n (desktop or cloud)
**Tasks:**
- [ ] Install n8n and connect credentials (Gmail, Google Sheets)
- [ ] Workflow 1: HTTP Request → extract fields → add timestamp
- [ ] Workflow 2: Webhook → normalize data → append to Google Sheets
- [ ] Workflow 3: Schedule trigger → send daily summary email
- [ ] Export all 3 as JSON files
**Portfolio:** Workflow canvas screenshots + JSON exports + Sheets screenshot → `/n8n Portfolio/Workflow Exports/Day31-Foundations/`

---

## Day 32 — Lead Intake Automation (7-Node)
**Objective:** Build a complete multi-app lead intake that handles new vs. existing contacts.
**Company:** GrowthBridge Agency | **Time:** 3.5 hours
**Flow:** Webhook → IF (new vs. existing) → HubSpot Contact → HubSpot Deal → Slack #leads → Google Sheets log → Gmail auto-reply
**Tasks:**
- [ ] Set up HubSpot Private App credentials in n8n
- [ ] Build all 7 nodes with correct field mapping
- [ ] Test new contact path AND duplicate/existing contact path
- [ ] Create Automation Map diagram in Canva
**Portfolio:** Workflow canvas + all 6 confirmation screenshots + JSON export + Canva map → `/n8n Portfolio/Workflow Exports/Day32-Lead-Intake/`

---

## Day 33 — Automated Monthly Client Report Generator
**Objective:** Loop over 10 clients, calculate metrics, and email a formatted report to each.
**Company:** GrowthBridge Agency | **Time:** 3.5 hours
**Key nodes:** Schedule trigger → Google Sheets read → Code (group by client) → Loop → Code (format HTML) → Gmail per client → Sheets log
**Tasks:**
- [ ] Build Google Sheet with 30 rows of client metrics data
- [ ] Build full workflow with JavaScript Code nodes
- [ ] Test all 10 clients receive correct separate emails
- [ ] Verify 10 rows in report log after test run
**Portfolio:** Workflow canvas + Code node screenshot + sample email received + log sheet → `/n8n Portfolio/Workflow Exports/Day33-Automated-Reporting/`

---

## Day 34 — AI Lead Qualification Agent
**Objective:** Build an OpenAI-powered agent that scores, categorizes, and routes leads automatically.
**Company:** GrowthBridge Agency | **Time:** 4 hours
**AI Output (JSON):** qualification_score, qualification_tier, fit_reason, red_flags, recommended_action, personalized_opener
**Routing:** Hot/Warm → HubSpot deal + Slack + Gmail | Cold → Sheets nurture queue | Disqualified → Sheets log only
**Tasks:**
- [ ] Configure OpenAI credentials in n8n
- [ ] Build OpenAI node with structured JSON prompt
- [ ] Write Code node to parse AI JSON output
- [ ] Build IF routing node (3 paths)
- [ ] Test with 3 different lead profiles
**Portfolio:** Workflow canvas + AI JSON output screenshot + Slack message + Gmail screenshot → `/n8n Portfolio/Workflow Exports/Day34-AI-Lead-Qualification/`

---

## Day 35 — Deal Stage Change Automations
**Objective:** Build 2 n8n workflows triggered by HubSpot deal stage changes.
**Company:** GrowthBridge Agency | **Time:** 4 hours
**Workflow 1 (Closed Won):** Slack celebration → Gmail welcome → Sheets revenue log → 5 HubSpot onboarding tasks
**Workflow 2 (Closed Lost):** AI loss analysis → Slack to sales team → Sheets log
**Tasks:**
- [ ] Build HubSpot workflow to POST webhook on deal stage change
- [ ] Build both n8n workflows end-to-end
- [ ] Test Closed Won path — verify all 7 nodes fire
- [ ] Test Closed Lost path — verify AI generates unique analysis
**Portfolio:** Both workflow canvases + Slack messages + Sheets logs + JSON exports → `/n8n Portfolio/Workflow Exports/Day35-Deal-Stage-Automations/`

---

## Day 36 — AI Support Triage + 5-Path Routing
**Objective:** Build an AI-powered support ticket triage system routing to 5 different channels.
**Company:** GrowthBridge Agency | **Time:** 4 hours
**AI Output:** category (5 types), priority, summary, suggested_response_time
**Switch Node Paths:** billing → technical → campaign → reporting → general
**Tasks:**
- [ ] Build OpenAI triage node with JSON output
- [ ] Build Switch node with 5 branches
- [ ] Build HubSpot ticket creation + Slack notification + Gmail auto-acknowledgment
- [ ] Test with 5 different support request types
**Portfolio:** Workflow canvas (Switch node visible) + AI outputs + HubSpot ticket record → `/n8n Portfolio/Workflow Exports/Day36-Support-Triage/`

---

## Day 37 — Lead Data Enrichment Pipeline
**Objective:** Process a list of unenriched leads, enrich via API, update HubSpot, log results.
**Company:** GrowthBridge Agency | **Time:** 4 hours
**Key skills:** Loop Over Items, HTTP Request to Clearbit/Abstract API, error handling for failed enrichments
**Tasks:**
- [ ] Build 20-row unenriched leads Google Sheet
- [ ] Write Code node to extract email domain
- [ ] Build Loop + HTTP enrichment + IF (success/failure) branching
- [ ] Update HubSpot contacts with enriched data
- [ ] Log successes and failures to separate sheets
**Portfolio:** Workflow canvas + enriched HubSpot contact + success/failure sheets + JSON export → `/n8n Portfolio/Workflow Exports/Day37-Lead-Enrichment/`

---

## Day 38 — Client Onboarding — 4 Parallel Branches
**Objective:** Build a parallel-branch onboarding workflow — 4 things happen simultaneously.
**Company:** GrowthBridge Agency | **Time:** 4 hours
**Parallel Branches:** A) Gmail welcome | B) HubSpot deal + 8 tasks | C) Slack announcement | D) Google Sheets roster
**Tasks:**
- [ ] Build Webhook trigger + 4 parallel branches + Merge node
- [ ] Test all 4 branches execute simultaneously
- [ ] Test with 3 different service package types
- [ ] Create Onboarding Flow Diagram in Canva
**Portfolio:** Workflow canvas (parallel branches visible) + all 4 confirmation screenshots + Canva diagram → `/n8n Portfolio/Workflow Exports/Day38-Client-Onboarding/`

---

## Day 39 — AI Campaign Assistant
**Objective:** Build a workflow that generates 5 email subject variants using AI and formats them for Slack review.
**Company:** GrowthBridge Agency | **Time:** 3.5 hours
**AI Output:** 5 subject line variants with type tags, recommended variant, A/B test pair
**Slack format:** Rich Block Kit card (not plain text)
**Tasks:**
- [ ] Build AI subject line generator with JSON output
- [ ] Write Code node to format Slack Block Kit message
- [ ] Build Gmail notification to account manager
- [ ] Build second workflow: Weekly Content Ideas (Monday 9am → Slack)
- [ ] Test with 3 different campaign brief types
**Portfolio:** Workflow canvas + Slack Block Kit message screenshot + Gmail notification → `/n8n Portfolio/Workflow Exports/Day39-AI-Campaign-Assistant/`

---

## Day 40 — n8n Documentation Package
**Objective:** Name, export, and document all 10 n8n workflows into a professional package.
**Company:** GrowthBridge Agency | **Time:** 3.5 hours
**Deliverables:** Architecture diagram (Canva) | Workflow Inventory spreadsheet | Admin Runbook | 10 individual workflow docs | 10 JSON exports | Loom video
**Tasks:**
- [ ] Rename all workflows: "[Company] — [Function] — [Trigger Type]"
- [ ] Export all 10 workflows as JSON files
- [ ] Build Architecture Diagram in Canva
- [ ] Write Admin Runbook (6 sections)
- [ ] Write 1-page doc for each workflow
- [ ] Record Loom: n8n System Walkthrough (10 min)
**Portfolio:** All exports + diagrams + docs + Loom → `/n8n Portfolio/` (full structure)

---

# SECTION 3 CONTINUED: PHASE 6 — CAPSTONE (Days 41–45)
## GrowthBridge Agency — Full Revenue System

---

## Day 41 — System Architecture + HubSpot Master Config
**Objective:** Design the full system on paper, then confirm HubSpot matches the architecture.
**Time:** 4 hours
**Tasks:**
- [ ] Write Architecture Document (10 sections: summary, objectives, tech stack, objects, lifecycle, pipelines, automation inventory, integration map, governance, rollout timeline)
- [ ] Create Integration Map diagram in Canva
- [ ] Confirm all 4 HubSpot pipelines exist | [ ] Confirm all 6 active lists are populating
- [ ] Confirm all 15 custom properties are correctly built
**Portfolio:** Architecture PDF + Integration Map + HubSpot confirmation screenshots → `/Capstone Project/Architecture/`

---

## Day 42 — 8 Production HubSpot Workflows
**Objective:** Build or refine all 8 production-quality HubSpot workflows for GrowthBridge.
**Time:** 5 hours

| # | Workflow | Trigger |
|---|---|---|
| 1 | New Lead Intake & Routing | Contact created + Lifecycle = Lead |
| 2 | MQL Alert + SLA Escalation | HubSpot Score ≥ 50 |
| 3 | Deal Created Qualification Checklist | Deal created in pipeline |
| 4 | 5-Email Lead Nurture Sequence | Lifecycle Stage = Lead |
| 5 | Closed Won → Client Onboarding | Deal Stage = Closed Won |
| 6 | Client Health Monitoring | Health Score < 30 OR NPS < 7 |
| 7 | Contract Renewal Alerts (60/30/7 days) | Contract Renewal Date approaching |
| 8 | Upsell Trigger | Customer 90+ days + budget < $2.5K |

**Tasks:**
- [ ] Build/refine all 8 workflows | [ ] Turn all 8 ON | [ ] Test each with a live contact
- [ ] Build Workflow Testing Log spreadsheet (8 rows, all PASS)
**Portfolio:** 8 workflow canvas screenshots + Testing Log → `/Capstone Project/HubSpot Automations/`

---

## Day 43 — 5 Production n8n Workflows + Integration Test
**Objective:** Build/refine all 5 capstone n8n workflows and run a full end-to-end system test.
**Time:** 5 hours

| # | Workflow | Key Feature |
|---|---|---|
| 1 | Master Lead Intake (12 nodes) | AI pre-scoring + priority routing |
| 2 | Closed Won Revenue Event | 4 parallel branches + AI onboarding tip |
| 3 | Monthly Revenue Report Generator | MoM calculations + AI executive summary |
| 4 | Weekly Client Health Monitor | Monday scan + per-client AI suggestions |
| 5 | Weekly AI Leadership Briefing | Friday metrics + AI narrative email |

**Tasks:**
- [ ] Build/refine all 5 workflows | [ ] Export all 5 as JSON
- [ ] Run end-to-end test tracing one lead through all 6 system touchpoints
- [ ] Build End-to-End System Test Log (6 steps, all PASS)
**Portfolio:** 5 workflow canvases + JSON exports + System Test Log → `/Capstone Project/n8n Automations/`

---

## Day 44 — Executive Reporting Suite + Analytics Report
**Objective:** Build 3 executive dashboards (30 reports) and write the Q1 RevOps Analytics Report.
**Time:** 5 hours

**Dashboard 1 — Revenue Command Center (10 reports):** MRR, new MRR, churn risk MRR, weighted pipeline, funnel conversion, revenue by service, deals closed, avg. deal value, sales cycle, MoM growth
**Dashboard 2 — Marketing Intelligence (10 reports):** Leads by source, MQL volume, lead-to-MQL rate, MQL-to-demo, email performance, form submissions, score distribution, landing page conversion, campaign revenue
**Dashboard 3 — Client Health & Retention (10 reports):** Health score distribution, at-risk table, NPS average, NPS by package, support tickets by client, renewals in 60 days, retention rate, upsell candidates, avg. tenure, churn this quarter

**Report Sections:** Executive Summary | Revenue Analysis | Lead Gen & Marketing | Sales Performance | Client Health | Automation ROI | Top 3 Recommendations | 90-Day Roadmap

**Tasks:**
- [ ] Build all 3 dashboards with all reports populated
- [ ] Write full 8-section Analytics Report with real data references
- [ ] Record Loom: Executive Dashboard Presentation (10 min)
**Portfolio:** 3 dashboard screenshots + Analytics Report PDF + Loom → `/Capstone Project/Reports/`

---

## Day 45 — Final Documentation + Portfolio Packaging ✓
**Objective:** Package the entire system into a professional, deployment-ready deliverable.
**Time:** 5 hours
**Tasks:**
- [ ] Write Client Handoff Package (12 sections)
- [ ] Run and document full CRM Health Audit (20 checkpoints)
- [ ] Run and document n8n Health Audit (10 checkpoints)
- [ ] Organize complete portfolio folder structure
- [ ] Build 10-slide Capstone Showcase Deck in Canva
- [ ] Record Loom: Full System Walkthrough (15 min)
- [ ] Create Portfolio Index PDF listing all artifacts
**Portfolio:** Everything organized in `/Capstone Project/` folder structure

---

# SECTION 4: PORTFOLIO STRUCTURE

See file: `06-portfolio-and-hiring.md` for the complete file-by-file folder breakdown.

**Quick summary of top portfolio artifacts:**
1. GrowthBridge Revenue System Architecture PDF (Day 41)
2. Q1 RevOps Analytics Report (Day 44)
3. Loom: Full System Walkthrough 15-min (Day 45)
4. n8n AI Lead Qualification Workflow JSON (Day 34)
5. Stackr SaaS RevOps Optimization Report (Day 24)
6. NovaNest Lead Scoring Model PDF (Day 11)
7. Capstone Showcase Deck 10-slides (Day 45)
8. All 6 HubSpot Certification screenshots

---

# SECTION 5: HIRING READINESS

## Readiness Levels

| Level | Definition | Reached After |
|---|---|---|
| Beginner | Can navigate HubSpot but cannot configure independently | Before Day 1 |
| Junior | Can set up properties, pipelines, simple workflows | Day 3 |
| Intermediate | Full CRM build, multi-step workflows, reports independently | Day 8 |
| Employable | Ready for CRM Specialist, Marketing Automation, Junior RevOps | Day 24 |
| Deployment-Ready | Can deliver on Day 1 of any job without handholding | Day 45 |

## Job Titles to Apply For

| Title | Salary Range | Ready After |
|---|---|---|
| HubSpot Administrator | $50K–$70K | Day 30 |
| CRM Specialist | $50K–$72K | Day 30 |
| Marketing Automation Specialist | $55K–$80K | Day 30 |
| Revenue Operations Analyst | $65K–$90K | Day 45 |
| HubSpot Consultant (Freelance) | $60–$95/hr | Day 45 |

## Resume Headline Suggestions
- "HubSpot CRM Specialist | Marketing Automation | RevOps | n8n"
- "CRM Architect & Automation Engineer | HubSpot Certified × 6 | AI Workflows"
- "Revenue Operations Specialist | HubSpot + n8n + AI Automation"
