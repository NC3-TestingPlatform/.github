# Security Policy

## Supported Versions

The following table lists which versions of NC3 Testing Platform tools currently receive security updates.

| Version | Supported          |
| ------- | ------------------ |
| latest  | :white_check_mark: |
| < latest | :x:               |

We only maintain and patch the latest released version of each tool. We encourage all users to keep their deployments up to date.

---

## Reporting a Vulnerability

**Please do not report security vulnerabilities through public GitHub issues, discussions, or pull requests.**

We use GitHub Private Vulnerability Reporting for all security disclosures. To report a vulnerability:

1. Navigate to the affected repository on GitHub.
2. Click the **"Security"** tab.
3. Click **"Report a vulnerability"** to open a private advisory draft.
4. Provide as much detail as possible: affected component, steps to reproduce, potential impact, and any suggested mitigations.

If you are unsure which repository is affected, you may open a private advisory in this `.github` repository and we will route it appropriately.

**Do not include exploit code or proof-of-concept that could cause harm if intercepted.**

---

## Response Timeline

We are committed to responding to all security reports in a timely and transparent manner.

| Milestone | Target |
| --------- | ------ |
| Initial acknowledgement | Within **72 hours** of receipt |
| Triage and severity assessment | Within **7 days** |
| Patch for Critical / High severity | Within **90 days** |
| Patch for Medium / Low severity | Within **180 days** |
| Public disclosure | Coordinated with reporter after patch is released |

We will keep you informed of our progress throughout the process. If we are unable to meet a deadline, we will notify you in advance and provide a revised estimate.

---

## Severity Classification

We follow the [CVSS v4.0](https://www.first.org/cvss/) scoring system for severity classification:

| Severity | CVSS Score |
| -------- | ---------- |
| Critical | 9.0 – 10.0 |
| High     | 7.0 – 8.9  |
| Medium   | 4.0 – 6.9  |
| Low      | 0.1 – 3.9  |

---

## Out-of-Scope Items

The following are explicitly **out of scope** for our vulnerability disclosure program:

- Vulnerabilities in third-party dependencies (report these upstream; we will update our dependency once a fix is available)
- Issues requiring physical access to a server or device
- Social engineering attacks against NC3 staff or users
- Denial-of-service attacks that require excessive resources or bandwidth
- Issues in end-of-life or unsupported versions
- Theoretical vulnerabilities with no demonstrated impact
- Missing security headers where no concrete exploit is demonstrated
- Rate-limiting or brute-force issues on non-authentication endpoints
- Self-XSS requiring the attacker to trick themselves
- Open redirects that do not lead to phishing or credential theft
- Publicly known CVEs already tracked in our dependency update pipeline

---

## Safe Harbor

We consider security research conducted under this policy to be authorised. We will not pursue legal action against researchers who:

- Act in good faith and follow this policy
- Avoid accessing, modifying, or deleting data that does not belong to them
- Do not disrupt services or degrade user experience
- Report findings promptly and give us reasonable time to remediate before disclosure

---

## Contact

For questions about this policy, contact the NC3 Testing Platform security team via the private vulnerability reporting mechanism described above, or reach us at **info@nc3.lu**.

*NC3 — National Cybersecurity Competence Center, Luxembourg*
*https://testing.nc3.lu/*
