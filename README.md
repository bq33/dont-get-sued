# Don't Get Sued

### Vibe-coded apps are cool. Lawyer fees aren’t.

As the great poet **Shawn Carter (JAY-Z)** once said: “Chains is cool to cop ... more important is lawyer fees.”

Run **Don't Get Sued** with your Lovable apps and coding agents to identify avoidable legal, privacy, security, intellectual-property and app-store risks **before launch**.

**THIS IS NOT LEGAL ADVICE. REVIEW YOUR ACTUAL APP WITH A QUALIFIED LAWYER OR LEGAL PROFESSIONAL TO ENSURE ALL APPLICABLE LEGAL REQUIREMENTS ARE MET BEFORE LAUNCH. THIS TOOL DOES NOT CERTIFY COMPLIANCE OR GUARANTEE AGAINST LAWSUITS, FINES OR OTHER LEGAL CONSEQUENCES.**

## Independent standalone project

This is a separate, open-source repository with no dependencies on any other skill, repository, or employer-private source materials.

- **58 evidence-first risk controls**: original 34 plus 24 privacy enhancements.
- **Six local MCP tools** for planning, jurisdiction-specific privacy reviews, evidence triage, source-pattern signals and counsel handoff.
- Coverage for **EU GDPR**, **EU ePrivacy**, **UK GDPR/PECR**, **US state privacy**, COPPA, CCPA/CPRA, app stores, subscriptions, IP and security.
- No runtime dependencies, outbound analytics, automatic project access, browser access or deployments.

## Getting started with Lovable

The skill is installed in the Lovable workspace under `dont-get-sued`. If you need to install it elsewhere, use [`skills/dont-get-sued/SKILL.md`](skills/dont-get-sued/SKILL.md) or paste [`lovable/KNOWLEDGE.md`](lovable/KNOWLEDGE.md) into the project's knowledge.

Ask Lovable:

> Activate `dont-get-sued`. Audit this app's privacy, cookies, EU GDPR, UK GDPR, applicable US state laws, app-store requirements, terms, subscriptions, intellectual property and security. Cite evidence, report P0–P3 issues and unknowns, and prepare a lawyer handoff. **Do not modify or deploy yet.**

The Lovable skill is an instruction layer; a GitHub URL does not automatically install a local stdio MCP server in Lovable.

## MCP setup (optional)

Requires **Node.js 20+**.

```bash
git clone https://github.com/bq33/dont-get-sued.git
cd dont-get-sued
npm test
node src/server.mjs
```

For a coding agent supporting MCP stdio servers:

```json
{
  "mcpServers": {
    "dont-get-sued": {
      "command": "node",
      "args": ["/ABSOLUTE/PATH/dont-get-sued/src/server.mjs"]
    }
  }
}
```

| Tool | Purpose |
|---|---|
| `get_legal_risk_catalog` | 58 sourced review controls with optional category filter |
| `get_privacy_review` | EU GDPR, ePrivacy, UK privacy and US state framework checklists |
| `build_review_plan` | Contextual questions by platforms, markets and features |
| `triage_legal_risk_evidence` | Evidence-based P0–P3 issues; never a legal-compliance verdict |
| `scan_source_signals` | Signals in supplied code snippets, not a security audit |
| `prepare_counsel_handoff` | Factual lawyer review questions and outstanding issues |

## Privacy-first module

See [privacy framework guidance](references/PRIVACY_FRAMEWORKS.md), the [risk catalog](rules.json) and [authoritative legal and platform references](references/LEGAL_SOURCES.md).

GDPR review includes territorial scope, lawful basis, transparency, data subject rights, consent and withdrawal, minimization, processors and DPAs, SCCs/transfers, DPIAs, data breaches, DPO and EU representative triggers, special categories and automated decisions. Review **EU ePrivacy** tracking separately from GDPR. UK GDPR/PECR are separate from EU law. US privacy compliance is assessed by relevant state, threshold and data practice.

## Safety and limits

- Unknown regional reach or app features must remain **unverified**, not "compliant."
- Cite actual code, sanitized network traces, live UI, dummy records or vendor contracts for each technical finding.
- Don't send raw customer data, credentials or production recordings to the MCP tool.
- Do not test production or take legal/financial actions without authorization.
- Do not automatically publish policies, accept legal terms, change consent gates or deploy.
- **Only qualified counsel can determine applicable legal obligations and review documents for a real release.**

## Project layout

```text
dont-get-sued/
├── README.md
├── AGENTS.md
├── LICENSE
├── .github/workflows/tests.yml
├── skills/dont-get-sued/SKILL.md
├── rules.json
├── src/server.mjs
├── package.json
├── lovable/KNOWLEDGE.md
├── lovable/STARTER-PROMPTS.md
├── references/LEGAL_SOURCES.md
├── references/PRIVACY_FRAMEWORKS.md
├── references/COUNSEL_HANDOFF.md
├── references/CONSENT_RECORD_EXAMPLE.md
├── examples/profile.json
└── tests/server.test.mjs
```

## License

MIT. See [LICENSE](LICENSE).
