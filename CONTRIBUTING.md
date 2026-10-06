# Contributing

IRIS and Pakistani tax rules change every year, so updates from people who have just filed are the most valuable contribution.

## Reporting an IRIS change or a bug

Open a GitHub Issue and include:

- **Tax year** you were filing.
- **Where it happened:** the IRIS screen or menu path, and the field name or code.
- **What the skill said** versus **what IRIS or FBR actually showed** (error message text, new code, changed rate).
- **An official source**, if you have one (FBR press release, rate card, circular, SRO).

## Sending a pull request

1. Fork the repo and edit `fbr-iris-tax-return/SKILL.md`.
2. Keep changes specific: updated codes, rates, screen names, pitfalls or deadlines.
3. State the tax year each change applies to, and cite an official FBR source for rates and legal rules. Blogs, videos and social posts are not sources.
4. Keep the safety rules intact: Claude never logs in, enters OTPs or PINs, types CNIC or bank numbers, or clicks Submit, and the user must supervise the browser session.

## Never include personal data

Do not put any of the following in issues, pull requests, screenshots or commits:

- CNIC, NTN, passport, bank account, IBAN or card numbers
- Passwords, PINs, OTPs or document passwords
- Your real income, tax or balance figures, or screenshots of your return

Blur or replace values with illustrative ones before sharing.

## Disclaimer

Contributions are covered by the [MIT license](LICENSE). This project is not tax advice; see [DISCLAIMER.md](DISCLAIMER.md).
