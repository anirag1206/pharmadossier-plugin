---
name: dossier-orchestrator
description: Orchestrates the full PharmaDossier sales process from prospect to paid — research, qualify, outreach, follow-up, NDA, payment. Use when you want to run a complete end-to-end dossier sale for a specific prospect or when managing a pipeline of leads.
---

# PharmaDossier Sales Orchestrator

This orchestrator coordinates all pharma-dossier-skills into a complete, structured sales process — from first research to signed NDA and payment received.

## Objective

Run the full tech-transfer dossier sale in the most efficient sequence possible, using the right skill at each stage and always knowing what the next action is.

## The PharmaDossier Sales Process

```
STAGE 1: PROSPECT        → prospect-research
STAGE 2: QUALIFY         → dossier-qualification  
STAGE 3: OUTREACH        → nda-outreach
STAGE 4: FOLLOW-UP       → follow-up-emails
STAGE 5: NDA EXECUTE     → (this skill)
STAGE 6: PAYMENT         → (this skill)
STAGE 7: DELIVERY        → (this skill)
```

## Stage Gate Logic

### STAGE 1: Prospect Research
**Trigger**: New company name or LinkedIn profile to evaluate.

**Action**: Run `prospect-research` to build a full company and decision-maker brief.

**Gate to advance**: Product fit is at least 3/5 — they manufacture a dosage form for which a dossier exists in catalogue.

**Output needed**: Prospect brief with molecule fit and decision-maker contact.

---

### STAGE 2: Qualification
**Trigger**: Prospect brief complete, OR inbound enquiry received.

**Action**: Run `dossier-qualification` to score the lead.

**Gate to advance**:
- Hot (20–25): Advance immediately to outreach
- Warm (12–19): Advance to outreach with longer nurture window
- Cold (<12): Add to 90-day nurture, do not pursue actively

**Output needed**: Qualification report with PHARMA score and tier recommendation.

---

### STAGE 3: First Contact Outreach
**Trigger**: Lead scored Hot or Warm.

**Action**: Run `nda-outreach` to draft personalized message.

**Channel priority** (India):
1. WhatsApp (if mobile number available)
2. LinkedIn DM (if no number)
3. Email (supplement to above)

**Channel priority** (Export):
1. LinkedIn DM
2. Email
3. WhatsApp (if available)

**Gate to advance**: They respond OR 48 hours pass.

**If response**: Move to qualification conversation (ask PHARMA questions).  
**If no response**: Move to Stage 4.

---

### STAGE 4: Follow-Up Sequence
**Trigger**: No response after 48h, or conversation stalled.

**Action**: Run `follow-up-emails` to generate the right touch for the situation.

**Follow-up map**:
| Situation | Touch Type |
|-----------|-----------|
| 48h no response | Touch 1 — same channel reminder |
| 1 week no response | Touch 2 — new channel + contents list |
| 2 weeks no response | Touch 3 — urgency / exclusivity nudge |
| 4 weeks no response | Touch 4 — break-up message |
| Read receipt but no reply | Specific WhatsApp seen-no-reply message |
| "Send more info" then went silent | Specific follow-up template |

**Gate to advance**: They respond and want to know pricing / NDA.

**Stop condition**: Touch 4 sent with no response → move to 90-day nurture.

---

### STAGE 5: NDA Execution
**Trigger**: Prospect confirms interest and asks for pricing or NDA.

**What to send:**
1. Final pricing confirmation based on tier (Starter / Standard / Premium)
2. NDA draft (bilateral, single-site license)
3. Company details form (registered company name, GST/TAN for India, country and company registration for export)

**Standard NDA turnaround**: Same business day if received before 5pm IST.

**Checklist before sending NDA:**
- [ ] Molecule confirmed and in catalogue
- [ ] Tier confirmed (Starter / Standard / Premium)
- [ ] Regulatory market confirmed
- [ ] Company legal name and address collected
- [ ] Single-site address confirmed (manufacturing location that gets licensed)

**Common NDA questions and answers:**
- "Can we modify the agreement?" — Minor edits acceptable; core IP protection clauses are non-negotiable
- "Can we get site exclusivity?" — Premium tier includes 12-month regional exclusivity option (quote separately)
- "Is GST included?" — No, GST at 18% applicable to Indian buyers; show the base price and GST separately on proforma

---

### STAGE 6: Payment Collection

**India payment methods:**
- UPI (GPay / PhonePe / Paytm) for amounts up to ₹1,00,000
- NEFT / RTGS for all amounts (send bank details with proforma invoice)
- Cheque: not preferred, adds 3–5 day delay

**Export payment methods:**
- Wise (bank transfer, fastest and lowest fee)
- SWIFT / Wire transfer to Indian account
- Do not accept PayPal (high fees, not suitable for B2B)

**Proforma invoice checklist:**
- [ ] Company name and address (buyer)
- [ ] GST/GSTIN (Indian buyers)
- [ ] HSN code for IP licensing services (998314)
- [ ] Price in INR (India) or USD (export)
- [ ] "Subject to Single-Site License Agreement dated [date]"
- [ ] Payment terms: Advance (100% before delivery)

**Gate to advance**: Payment confirmed in bank account.

---

### STAGE 7: Document Delivery

**Delivery process:**
1. Generate watermarked PDF with licensee company name + date on each page
2. Send via email to the registered contact email
3. Send delivery confirmation on WhatsApp
4. Log delivery in customer record

**Starter delivery (MFR)**: Within 24 hours of payment confirmation.  
**Standard delivery (Full Tech Pack)**: Within 48 hours.  
**Premium delivery (Dossier-Ready Pack)**: Within 48 hours for documents; schedule 1-hour call within 5 business days.

**What to include in delivery email:**
- Subject: "PharmaDossier: [Molecule] [Dosage Form] — [Tier] Package Delivered"
- ZIP file or Dropbox link with all modules
- Reference to the executed NDA
- Support instructions (email/WhatsApp for queries)
- Reminder of single-site license scope

---

## Pipeline Tracking Template

Use this to track active leads:

```
| Company | Molecule | Stage | Last Touch | Next Action | Due |
|---------|---------|-------|-----------|------------|-----|
| [Co]    | [Mol]   | 3     | WA 09-Nov | Follow-up  | 11-Nov |
```

Stages: 1=Research, 2=Qualified, 3=Outreach, 4=Follow-up, 5=NDA, 6=Payment, 7=Delivered, X=Dead

---

## Weekly Sales Cadence

**Monday**: Review all active leads — what stage, what next action.  
**Tuesday–Thursday**: Outreach and follow-up messages.  
**Friday**: Review responses, qualify new inbounds, update pipeline.

**Monthly review:**
- How many leads entered the pipeline?
- How many reached Stage 5 (NDA)?
- What was the conversion rate?
- Which molecules had the most enquiries?

---

## Quick Reference: Key Numbers

| Metric | Target |
|--------|--------|
| First response time | <4 hours |
| NDA turnaround | Same business day |
| Delivery after payment | 24–48 hours |
| Follow-up touches before stopping | 4 |
| WhatsApp response rate target | >30% |
| Conversion: enquiry → paid | >15% |

---

## How to Use This Orchestrator

When a user says:
- "I have a new lead from [Company]" → Start at Stage 1 (prospect-research)
- "Someone enquired about [molecule]" → Start at Stage 2 (dossier-qualification)
- "They haven't responded in a week" → Stage 4 (follow-up-emails, Touch 2)
- "They're asking for the NDA" → Stage 5 (run NDA checklist above)
- "Payment received" → Stage 7 (run delivery checklist)
- "Run the full process for [Company]" → Run all stages in sequence

Always confirm the current stage before recommending the next action.
