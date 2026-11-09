# PharmaDossier Claude Code Plugin

A Claude Code plugin marketplace for pharmaceutical formulation tech-transfer sales. Built for [PharmaDossier.com](https://pharmadossier.com) — India's pharma dossier licensing clearinghouse.

## What This Does

This plugin gives Claude Code 5 specialized skills for closing pharma B2B dossier licensing deals — from researching a manufacturer to delivering watermarked documents after payment.

## Skills Included

| Skill | When to Use |
|-------|------------|
| `prospect-research` | Researching a pharma manufacturer before first contact |
| `dossier-qualification` | Scoring an inbound enquiry or responding prospect |
| `nda-outreach` | Drafting WhatsApp, LinkedIn, or email first-contact messages |
| `follow-up-emails` | Re-engaging prospects who have gone quiet |
| `dossier-orchestrator` | Running the full pipeline from prospect to delivery |

## Installation

```bash
# Add to Claude Code
claude plugin add https://github.com/anirag1206/pharmadossier-plugin

# Or install the pharma-dossier-skills plugin directly
claude plugin add ./pharma-dossier-skills
```

## Quick Start

```
# Research a new prospect
/prospect-research Company: "Alkem Laboratories", Molecule: "Pantoprazole 40mg pellets"

# Qualify an inbound enquiry
/dossier-qualification Company: "Cipla Kenya Ltd", Molecule: "Amoxicillin-Clavulanate dry syrup"

# Draft first WhatsApp message
/nda-outreach Company: "Sun Pharma", Channel: WhatsApp, Molecule: "Telmisartan+Metformin bilayer"

# Full pipeline orchestration
/dossier-orchestrator Company: "Zydus Cadila", Stage: "1-research"
```

## Plugin Architecture

```
pharmadossier-plugin/
├── .claude-plugin/
│   └── marketplace.json          # Marketplace manifest
├── pharma-dossier-skills/        # Main plugin
│   ├── .claude-plugin/
│   │   └── plugin.json           # Plugin metadata
│   └── skills/
│       ├── prospect-research/    # Company + decision-maker intel
│       ├── dossier-qualification/# PHARMA scoring framework
│       ├── nda-outreach/         # First-contact message templates
│       ├── follow-up-emails/     # 4-touch re-engagement sequence
│       └── dossier-orchestrator/ # Full pipeline management
└── README.md
```

## Context

Pharma B2B dossier sales are different from SaaS sales:
- Deals close over WhatsApp and phone, not email campaigns
- Buyers are R&D heads, Regulatory heads, and MDs — not procurement
- Trust signals are technical (WHO-GMP, validated scale, stability data)
- Price ranges from ₹10K–₹1L (India) and $500–$4,500 (export)
- Timeline from enquiry to payment: 3–14 days for warm leads

These skills are built for that reality.

## Contributing

Built for [PharmaDossier.com](https://pharmadossier.com). For questions: info@pharmadossier.com
