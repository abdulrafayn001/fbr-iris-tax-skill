# FBR IRIS Tax Return Skill for Claude

A [Claude](https://claude.com/claude-code) skill that guides you through preparing and filing a Pakistan FBR income tax return (form 114(1)) and wealth statement (116) in IRIS 2.0, then enters the approved values in IRIS through the Claude in Chrome extension.

**Tax year covered: TY2026** (1 July 2025 to 30 June 2026). Codes, rates and screens must be re-verified for any other year.

> **Read [DISCLAIMER.md](DISCLAIMER.md) first.** This is not tax advice and is not affiliated with FBR. You are responsible for every figure you file.

## What it does

1. **Intake:** asks about your income, assets and big events of the year.
2. **Document checklist:** tells you which documents to gather (employer certificate, bank statements, CDC and fund statements, certificates) and where each value goes in IRIS.
3. **Ledger and classification:** reads your statements, builds a ledger, classifies credits and flags pass-through transfers.
4. **FBR cross-check:** compares your numbers with FBR's own data (Maloomat, Summary of Economic Transactions).
5. **Income, tax and wealth statement:** computes each head and reconciles net assets to an unreconciled amount of 0.
6. **IRIS entry:** after you approve each value, fills it in through Chrome.
7. **Final verification:** red-flag checklist, then **you** press Submit.

Supports salary, freelance IT-export (s.154A), PSX shares, mutual funds, bank profit, property, vehicles and family money flows.

## Safety model

- Claude explains every field, its rule, source document and value, and waits for your approval before entering it.
- **You** log in, enter OTPs and PINs, type CNIC/bank numbers and click Submit. Claude never does.
- **Supervise the browser session.** Keep the window visible and stop it if anything looks wrong.

## Requirements

- [Claude Code](https://claude.com/claude-code) (or another Claude client that supports skills)
- The [Claude in Chrome](https://claude.com/chrome) extension, for the IRIS data-entry phase
- An active IRIS account and your tax documents

## Install

```bash
git clone https://github.com/<your-username>/fbr-iris-tax-skill.git
cp -r fbr-iris-tax-skill/fbr-iris-tax-return ~/.claude/skills/
```

Restart Claude Code, then ask something like:

> Help me file my FBR income tax return for tax year 2026.

## Repository layout

```
├── README.md
├── LICENSE
├── DISCLAIMER.md
├── CONTRIBUTING.md
└── fbr-iris-tax-return/
    └── SKILL.md
```

## Contributing

IRIS changes every year. If a code, rate or screen has changed, please [open an issue](../../issues) or send a pull request. See [CONTRIBUTING.md](CONTRIBUTING.md). **Never include personal data** (CNIC, NTN, account numbers, real amounts, screenshots of your return) in issues or PRs.

## License

[MIT](LICENSE). Use at your own risk; see [DISCLAIMER.md](DISCLAIMER.md).
