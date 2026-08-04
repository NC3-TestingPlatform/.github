<div align="center">

<img src="https://github.com/NC3-TestingPlatform.png" alt="NC3 Testing Platform" width="160" style="border-radius: 50%;"/>

# NC3 Testing Platform

**External attack surface assessment — recon, misconfiguration detection, no exploitation 🇱🇺**

[![Website](https://img.shields.io/badge/testing.nc3.lu-0066CC?style=for-the-badge&logo=firefox-browser&logoColor=white)](https://testing.nc3.lu/)
[![Email](https://img.shields.io/badge/opensource%40nc3.lu-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:opensource@nc3.lu)
[![GitHub followers](https://img.shields.io/github/followers/NC3-TestingPlatform?style=for-the-badge&logo=github&logoColor=white&color=181717)](https://github.com/NC3-TestingPlatform)

</div>

---

## About

The **NC3 Testing Platform** is an open-source security toolkit developed by [NC3.lu](https://nc3.lu/) — Luxembourg's National Cybersecurity Competence Center — operating under the [Luxembourg House of Cybersecurity](https://lhc.lu).

It automates **external attack surface assessments** from an unauthenticated, black-box perspective — covering passive reconnaissance, active service probing, and misconfiguration detection across DNS, PKI, mail security controls, and HTTP/S-exposed services. The platform operates strictly within a pre-exploitation scope: no vulnerability exploitation, no lateral movement, no payload delivery.

This organisation hosts the **v4** rewrite: a ground-up redesign built around independent, API-driven backend modules that can be composed and orchestrated by a central platform core.

> **v3** is live at [testing.nc3.lu](https://testing.nc3.lu/) · source at [NC3-LU/TestingPlatform](https://github.com/NC3-LU/TestingPlatform)

---

## Architecture

v4 is a full-stack application structured around autonomous backend modules. Each module targets a distinct attack surface area, lives in its own repository, exposes a consistent REST API, and can be deployed and tested independently.

| Layer | Repository | Description |
|---|---|---|
| **Modules** | see [Modules](#modules) below | Standalone assessment engines, scoped to a specific attack surface domain |
| **Backend** | [testing-platform-backend](https://github.com/NC3-TestingPlatform/testing-platform-backend) | Platform core — orchestration, aggregation, and REST API layer *(in development, private)* |
| **Frontend** | [testing-platform-frontend](https://github.com/NC3-TestingPlatform/testing-platform-frontend) | Analyst-facing web interface for result review and reporting *(in development, private)* |

---

## Modules

| Module | Role | Description |
|--------|------|-------------|
| [**chainvalidator**](https://github.com/NC3-TestingPlatform/chainvalidator) | `assessment` | DNSSEC chain-of-trust validator — verifies DS, DNSKEY, and RRSIG records from the IANA root trust anchor to the target domain |
| [**mailvalidator**](https://github.com/NC3-TestingPlatform/mailvalidator) | `assessment` | Mail security posture validator — checks MX, SPF, DMARC, DKIM, BIMI, MTA-STS, DNSSEC, and 104 DNSBLs with letter-grade verdicts |
| [**subdomainenum**](https://github.com/NC3-TestingPlatform/subdomainenum) | `assessment` | Subdomain enumeration CLI — passive and active discovery wrapping subfinder, findomain, assetfinder, gobuster, ffuf, and dnsrecon |
| [**headersvalidator**](https://github.com/NC3-TestingPlatform/headersvalidator) | `assessment` | HTTP security-header validator — checks headers against RFC 9110/9111, OWASP guidelines, and the IANA registry with letter-grade verdicts |
| [**tlsvalidator**](https://github.com/NC3-TestingPlatform/tlsvalidator) | `assessment` | TLS connection posture validator — grades protocol versions, cipher suites, certificate, and known vulnerabilities (Heartbleed/ROBOT/CCS/CRIME) via SSLyze, plus an informational post-quantum key-exchange check, with letter-grade verdicts |
| [**quantumvalidator**](https://github.com/NC3-TestingPlatform/quantumvalidator) | `assessment` | Post-quantum cryptography readiness validator — probes TLS and SMTP/STARTTLS endpoints for ML-KEM hybrid key exchange (CNSA 2.0 / BSI TR-02102-2) with a binary SAFE/UNSAFE verdict |
| [**zoneripper**](https://github.com/NC3-TestingPlatform/zoneripper) | `assessment` | DNSSEC zone-walking tester — walks NSEC chains, collects NSEC3 hashes, and exports cracking jobs for Hashcat |
| [**portscanner**](https://github.com/NC3-TestingPlatform/portscanner) | `assessment` | nmap-driven port and service inventory — reports open ports and detected services for any host, IP, or CIDR range, with nmap XML parsed via nmap2json (inventory only, no grading) |
| [**fileanalyzer**](https://github.com/NC3-TestingPlatform/fileanalyzer) | `assessment` | File analysis engine — CIRCL hashlookup known-file triage with policy-based verdicts, escalating unknown or suspicious files to Pandora deep behavioural analysis |

The platform core — [testing-platform-backend](https://github.com/NC3-TestingPlatform/testing-platform-backend) and [testing-platform-frontend](https://github.com/NC3-TestingPlatform/testing-platform-frontend) — is under active development in private repositories.

---

## Community & Partners

NC3 collaborates closely with the national and international cybersecurity community:

[![LHC](https://img.shields.io/badge/Luxembourg%20House%20of%20Cybersecurity-lhc.lu-005BAC?style=flat-square)](https://lhc.lu)
[![CIRCL](https://img.shields.io/badge/CIRCL-circl.lu-4CAF50?style=flat-square)](https://www.circl.lu)
[![Cybersecurity.lu](https://img.shields.io/badge/National%20Portal-cybersecurity.lu-E53935?style=flat-square)](https://cybersecurity.lu)
[![NC3-LU](https://img.shields.io/badge/Parent%20Org-NC3--LU-0066CC?style=flat-square)](https://github.com/NC3-LU)

---

## Contributing

All modules are open source and **contributions are welcome**. Whether you're reporting a bug, suggesting a feature, or submitting a pull request — check the `CONTRIBUTING.md` in each repository to get started.

For general inquiries or collaboration proposals, reach out at [opensource@nc3.lu](mailto:opensource@nc3.lu).

---

<div align="center">

*Building a safer digital Luxembourg — one commit at a time.*

📍 122 rue Adolphe Fischer, L-1521 Luxembourg &nbsp;|&nbsp; 📞 +352 274 00 98 601 &nbsp;|&nbsp; 🌐 [nc3.lu](https://nc3.lu)

</div>
