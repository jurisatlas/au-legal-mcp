---
name: au-legal-mcp-skill
description: Official Australia (AU) legislation, multi-tier court precedent research, and citation verification skill.
version: 2.0.0
author: JurisAtlas
license: MIT
---

# Australia Legal Research & Multi-Tier Case Law Skill (`au-legal-mcp`)

Use this skill whenever the user asks a legal question, drafts a pleading or contract, or researches case law across any judicial instance in **Australia (AU)**.

## Verification & Research Rules

1. **Citation Verification:** Never fabricate a statutory provision or case citation. Query `search_legislation`, `search_case_law`, `search_tiered_court_decisions`, or `verify_citation` before citing any authority (e.g., `[2024] HCA 10 or [2023] FCA 105`).
2. **Multi-Tier Judicial Coverage:**
   - **First Instance (Trial / Municipal / District):** Federal Circuit and Family Court, State District/County & Magistrates/Local Courts (NSW, VIC, QLD, WA, SA, TAS, ACT, NT)
   - **Second Instance (Cantonal / Regional / Appellate):** Federal Court of Australia (FCA / FCAFC) & State/Territory Supreme Courts and Courts of Appeal (NSWCA, VSCA, QCA, WASCA, SASCA)
   - **Supreme & Constitutional Instance:** High Court of Australia (HCA)
   - **Primary Tiered Database:** AustLII & State/Federal Caselaw Portals (caselaw.nsw.gov.au / fedcourt.gov.au / hcourt.gov.au) (`https://www.caselaw.nsw.gov.au`)
