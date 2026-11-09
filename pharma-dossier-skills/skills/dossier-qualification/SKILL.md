---
name: dossier-qualification
description: Qualifies an inbound pharma manufacturer enquiry or a prospect who has responded — scores deal viability, identifies the right dossier tier, and determines next steps. Use when evaluating whether a lead is worth pursuing and what to sell them.
---

# Dossier Deal Qualification

This skill helps score and qualify a pharmaceutical manufacturer who has shown interest in a dossier licence — so you invest time in real buyers and move fast on hot leads.

## Objective

Determine: (1) Are they a genuine buyer? (2) Which dossier tier fits their need and budget? (3) What is the fastest path to NDA execution?

## The PHARMA Qualification Framework

Adapted from BANT for pharma B2B dossier sales:

| Letter | Stands For | Questions to Ask |
|--------|-----------|-----------------|
| **P** | Product Fit | Does the molecule/dosage form they need exist in the PharmaDossier catalogue? |
| **H** | Horizon (Timeline) | When do they need to file? Is this for a tender deadline, an export market launch, or long-term? |
| **A** | Authority | Are you speaking to the R&D head, MD, or just a junior scientist who can't decide? |
| **R** | Regulatory Market | Which regulatory agency will they file with? (CDSCO, WHO-GMP, ANDA, CTD?) |
| **M** | Money (Budget) | Do they have budget now, next quarter, or never? Can they stretch to Standard/Premium? |
| **A** | Alternatives | Are they considering doing in-house development, buying from a competitor, or just exploring? |

## Qualification Tiers

### 🔴 Hot Lead (move within 24 hours)
- Has a specific molecule in mind that matches catalogue
- Has a regulatory deadline (tender, WHO-PQ application, new market launch)
- Decision-maker is in the conversation
- Budget available immediately
- **Action**: Skip long qualification — send NDA draft and pricing directly

### 🟡 Warm Lead (nurture over 1–4 weeks)
- Molecule need is real but dossier not yet available (custom request)
- Timeline is 2–3 months away
- Junior contact — need to escalate to R&D head
- Budget cycle starts next quarter
- **Action**: Send catalogue and pricing deck, schedule a 20-min intro call

### 🔵 Cold / Nurture
- Just exploring, no specific molecule in mind
- Academic/regulatory advisor (not manufacturer)
- Budget uncertainty or project not approved internally
- **Action**: Add to email nurture list, follow up in 30 days

## Qualification Question Bank

### Product Fit Questions
- "Which molecule and dosage form are you looking for?"
- "What batch size are you targeting — 100 kg, 300 kg, 600 kg?"
- "What type of RMG/granulator do you have — Diosna, Fielder, NMC?"
- "Is this a new product for you or a reformulation of an existing line?"

### Regulatory Questions
- "Which market are you filing for — CDSCO, WHO-GMP, ANDA, or export?"
- "Do you have an in-house RA team or do you work with a CRO?"
- "Have you already received product approval (licence) or is this pre-filing?"
- "Do you need ICH Zone IVb stability data or accelerated only?"

### Authority Questions
- "Are you the person who signs off on formulation development decisions?"
- "Who else would need to be involved in this decision — R&D head, MD?"
- "Who handles regulatory filing at your company?"

### Timeline Questions
- "When do you need the dossier? Do you have a tender deadline or filing date?"
- "How soon could you start the NDA process if we confirm availability?"
- "Is this for an immediate project or planning for next year?"

### Budget Questions
- "Have you allocated a budget for tech-transfer or IP licensing this year?"
- "What range are you comfortable with — are you looking at Starter or a full tech pack?"
- "Have you licensed formulation IP from any source before — what did you pay?"

## Scoring Worksheet

Rate each factor 1–5. Total ≥ 20 = hot, 12–19 = warm, <12 = cold.

```
Product Fit:        ___ / 5  (5 = exact match in catalogue; 1 = no fit)
Decision Authority: ___ / 5  (5 = MD/R&D head; 1 = junior/unknown)
Regulatory Clarity: ___ / 5  (5 = specific filing target known; 1 = vague)
Timeline Urgency:   ___ / 5  (5 = deadline <60 days; 1 = no timeline)
Budget Readiness:   ___ / 5  (5 = budget confirmed; 1 = no budget)

TOTAL:              ___ / 25
```

## Tier Recommendation Logic

| Scenario | Recommended Tier |
|---------|-----------------|
| Need MFR only for CDSCO filing, have in-house RA team | **Starter** |
| Exporting to WHO-GMP markets, need analytical methods + stability | **Standard** |
| New dosage form, no in-house experience, needs SOPs + call support | **Premium** |
| Need 3+ molecules | **Volume discount** — quote per molecule |

## Output Format

```
## Qualification Report: [Company Name] — [Molecule]

**PHARMA Score**: [X/25] — [Hot / Warm / Cold]

**Product Fit**: [Match found / Custom needed]
**Decision-Maker**: [Name, Title — confirmed Y/N]
**Regulatory Market**: [CDSCO / WHO-GMP / ANDA / CTD]
**Timeline**: [Deadline or horizon]
**Budget**: [Confirmed range or unknown]
**Alternative risk**: [In-house development / competitor / none]

**Recommended Tier**: [Starter / Standard / Premium]
**Next Action**: [Send NDA + price / Schedule call / Add to nurture]
**Blockers**: [What needs to be resolved before sale]
```

## Cross-References

- Run `prospect-research` before qualification if this is outbound
- Use `nda-outreach` to draft the outreach message after scoring Hot
- Use `follow-up-emails` for Warm leads that go quiet
