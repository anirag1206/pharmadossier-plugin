# CLAUDE.md — PharmaDossier Plugin

This file guides Claude Code when working with this repository.

## Repository Overview

This is the **PharmaDossier Claude Code Plugin Marketplace** — a collection of skills for pharmaceutical formulation dossier sales. It mirrors the Salesably marketplace structure.

## Architecture

```
pharmadossier-plugin/
├── .claude-plugin/
│   └── marketplace.json          # Lists available plugins
├── pharma-dossier-skills/        # The main plugin (5 skills)
│   ├── .claude-plugin/
│   │   └── plugin.json           # Plugin manifest
│   └── skills/                   # One SKILL.md per skill
│       ├── prospect-research/
│       ├── dossier-qualification/
│       ├── nda-outreach/
│       ├── follow-up-emails/
│       └── dossier-orchestrator/
└── README.md
```

## Key Concepts

**Skill structure**: Each skill is a folder containing a `SKILL.md` with YAML frontmatter (`name`, `description`) and a markdown body. The `description` determines when Claude auto-suggests the skill.

**Sales context**: This plugin targets pharma B2B — manufacturers licensing formulation dossiers. The sales cycle involves:
- WhatsApp and LinkedIn outreach (not email campaigns)
- Technical buyers (R&D heads, Regulatory heads, MDs)
- 3–14 day deal cycle for warm leads
- NDA execution before document delivery
- India pricing in INR; export pricing in USD

## Working with Skills

```markdown
---
name: skill-name
description: When Claude should use this skill (triggers auto-suggest)
---

# Skill Title
[Detailed instructions]
```

## Adding New Skills

1. Create a new directory under `pharma-dossier-skills/skills/`
2. Add a `SKILL.md` with YAML frontmatter
3. Skills are auto-discovered via `"skills": "./skills"` in `plugin.json`

## Pharma Domain Context

**Key terms to use correctly:**
- MFR = Master Formula Record (not "recipe" or "formula")
- STP = Standard Testing Procedure
- RMG = Rapid Mixer Granulator (not just "granulator")
- PDR = Process Development Report
- PVP = Process Validation Protocol
- BOM = Bill of Materials
- ICH Zone IVb = stability protocol for tropical climates (India, Africa, SEA)
- WHO-GMP = WHO Good Manufacturing Practice (required for most export)
- CDSCO = Central Drugs Standard Control Organisation (India's FDA)
- ANDA = Abbreviated New Drug Application (US FDA generic filing)
- CTD/ACTD = Common Technical Document / ASEAN CTD

**Pricing (do not modify without user confirmation):**
- India Starter: ₹10,000–₹15,000
- India Standard: ₹25,000–₹50,000  
- India Premium: ₹75,000–₹1,00,000
- Export Starter: $500–$1,000
- Export Standard: $1,500–$2,500
- Export Premium: $3,000–$4,500
