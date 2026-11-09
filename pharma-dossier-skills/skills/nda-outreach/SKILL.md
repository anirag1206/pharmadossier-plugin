---
name: nda-outreach
description: Drafts personalized first-contact messages for pharma manufacturer prospects — WhatsApp, LinkedIn DM, or email — to initiate dossier enquiry and move toward NDA signing. Use when writing the first message to a new prospect or responding to an inbound enquiry.
---

# NDA Outreach Scripts

This skill creates personalized first-contact messages for pharmaceutical manufacturers — built for how pharma B2B actually closes: WhatsApp, LinkedIn, and phone calls, not automated email campaigns.

## Objective

Get a response that leads to a conversation. The message should feel like it came from someone who understands pharma manufacturing — not a marketing template.

## Channel Strategy

### WhatsApp (Primary for Indian buyers)
- Best response rate for Indian pharma manufacturers
- Keep to 3–5 sentences + a clear question
- Voice note follow-up works well after a text goes unread for 24h
- Never send unsolicited bulk messages — always personalize

### LinkedIn DM (Best for export buyers / R&D heads)
- Use for WHO-GMP export buyers in Africa, SEA, LATAM
- Good for reaching R&D and RA professionals
- Connection request + note, then DM after they accept
- 150–300 characters for the connection note; 300–500 for the DM

### Email (Secondary — for formal follow-ups)
- Use after an initial WhatsApp/LinkedIn contact
- Attach a one-page PharmaDossier product sheet (PDF)
- Good for sending NDA draft and pricing details

### Phone Call (For warm leads or post-no-response)
- Best for mid/large manufacturers where juniors screen calls
- Ask for R&D head or Regulatory head by name when possible
- Short script: introduce, ask one qualifying question, offer to send details

## Outreach Message Framework

### The 4-Part Pharma B2B Message Structure

```
1. HOOK       — Something specific to them (not generic)
2. BRIDGE     — Why you're reaching out to them specifically
3. OFFER      — What they get (the dossier value, not features)
4. CTA        — One simple low-friction next step
```

### Key Principles

**Do:**
- Reference their specific molecule, market, or regulatory situation
- Mention the deliverable (MFR, STP, stability data) concretely
- Keep it under 5 sentences for WhatsApp
- Ask one question, not five
- Use their language (say "RMG" not "granulator", "BOM" not "ingredient list")

**Don't:**
- Start with "I hope this finds you well"
- Explain the whole product in the first message
- Send a PDF unsolicited on first contact
- Use sales buzzwords like "best-in-class" or "game-changing"
- Ask if they're "interested" — assume they might be and find out

## Message Templates

### WhatsApp — Outbound (Cold)

**Template A: Molecule-specific**
```
Hi [Name], I'm Anirag from PharmaDossier. We have a validated 
[Molecule Name] [dosage form] dossier — MFR, HPLC methods, 
stability data, all ready to license. 

Noticed [Company] has [relevant context — e.g., WHO-GMP approval / 
exporting to Africa / new tablet line]. Thought this might be useful 
for your [regulatory market] filing.

Would it help if I sent you the dossier contents list?
```

**Template B: Trigger-based**
```
Hi [Name], I saw [Company] is expanding into [market / new line]. 

We have a ready [Molecule] dossier — commercially validated on 
600L RMG, with WHO-GMP compatible documentation. Saves 18+ months 
of development time.

Can I send you the product sheet — 2 pages?
```

**Template C: Inbound response**
```
Hi [Name], thanks for reaching out about [molecule]. 

Yes, we have a [Starter/Standard/Premium] dossier available — 
[MFR + STP / full tech pack / complete with SOPs and validation]. 

Before I send pricing, quick question: which regulatory market 
are you targeting — CDSCO, WHO-GMP, or export?
```

### LinkedIn DM — Export Buyer

**Connection Note (< 200 chars):**
```
Hi [Name] — I work in pharma formulation IP licensing. We have 
ready dossiers for [dosage form] molecules — might be relevant 
for your [export market] projects. Happy to connect.
```

**Follow-up DM after connection:**
```
Thanks for connecting, [Name]. 

We're PharmaDossier — we license validated formulation dossiers 
(MFR, analytical methods, stability data) for manufacturers 
filing in WHO-GMP, CDSCO, and ANDA markets.

I noticed [Company] works in [therapeutic area]. We have a 
[molecule] dossier that's been well-received by [market]-focused 
manufacturers.

Would a quick overview be useful? Happy to send the contents 
list first so you can decide if it's worth a conversation.
```

### Email — Formal Outreach

**Subject line options:**
- "Validated [Molecule] dossier — ready to license for [market] filing"
- "PharmaDossier: [Dosage Form] tech pack for [Company]"
- "MFR + STP + stability data: [Molecule] [strength] available"

**Body:**
```
Dear [Name / Dr. Name],

I'm reaching out because [Company] appears to be a strong fit 
for a dossier we have available.

We have a commercially validated [Molecule Name] [strength] 
[dosage form] dossier, developed on 600 L RMG infrastructure:
- Master Formula Record (complete BOM + process parameters)
- Validated HPLC methods for assay, RS, and dissolution
- 6-month accelerated stability data (40°C/75% RH)
- [Premium only: SOPs, PVP, and 1-hour tech-transfer call]

The dossier is compatible with [CDSCO/WHO-GMP/ANDA] filing and 
includes a bilateral NDA + Single-Site License Agreement.

Pricing starts at ₹[X] for India / $[X] for export buyers.

I've attached a 2-page product overview. If this looks relevant, 
I can share the full contents list and answer any questions.

Best regards,
Anirag Bansal
PharmaDossier.com | +91 70884 19261
```

## Objection Responses (First Contact)

### "Send me more details first"
```
Happy to. So I send something specific rather than a generic 
catalogue — which molecule are you focused on right now, 
and is this for a CDSCO or export filing?
```

### "We do our formulation in-house"
```
Understood — many of our clients have R&D teams too. They use 
our dossiers to shortcut the timeline on new molecules or 
backup regulatory submissions. Is there any molecule you're 
planning to add where timeline pressure is a factor?
```

### "What's the price?"
```
Depends on the tier — Starter (MFR only) starts at ₹10,000 
for India / $500 for export. Full tech pack (MFR + STP + 
stability + PDR) is ₹25,000–50,000 / $1,500–2,500.

Which molecule and which tier sounds closest to what you need?
```

### "We're not looking right now"
```
No problem at all. When would be a better time — next quarter, 
or after a specific milestone? Happy to send the catalogue now 
so you have it when the time comes.
```

## Output Format

When generating an outreach message, produce:

```
## Outreach Message: [Company Name] — [Channel]

**To**: [Name, Title, Company]
**Channel**: [WhatsApp / LinkedIn / Email]
**Hook Used**: [What personalisation was applied]

---
[Message text, ready to copy-paste]
---

**Fallback if no response in 48h**: [Brief follow-up approach]
**Objection to anticipate**: [Most likely pushback + response]
```

## Cross-References

- Run `prospect-research` before drafting to personalize the hook
- Run `dossier-qualification` after they respond
- Use `follow-up-emails` if they go silent after initial contact
