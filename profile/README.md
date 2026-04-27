<div align="center">

<img src="https://github.com/NC3-TestingPlatform.png" alt="NC3 Testing Platform" width="160" style="border-radius: 50%;"/>

# NC3 Testing Platform

**Modular security analysis toolkit for domains and mail infrastructure 🇱🇺**

[![Website](https://img.shields.io/badge/testing.nc3.lu-0066CC?style=for-the-badge&logo=firefox-browser&logoColor=white)](https://testing.nc3.lu/)
[![Email](https://img.shields.io/badge/opensource%40nc3.lu-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:opensource@nc3.lu)
[![GitHub followers](https://img.shields.io/github/followers/NC3-TestingPlatform?style=for-the-badge&logo=github&logoColor=white&color=181717)](https://github.com/NC3-TestingPlatform)

</div>

---

## About

The **NC3 Testing Platform** is an open-source security toolkit developed by [NC3.lu](https://nc3.lu/) — Luxembourg's National Cybersecurity Competence Center — operating under the [Luxembourg House of Cybersecurity](https://lhc.lu).

This organisation hosts the **v4** rewrite: a ground-up redesign built around independent, API-driven backend modules that can be composed and orchestrated by a central platform core.

> **v3** is live at [testing.nc3.lu](https://testing.nc3.lu/) · source at [NC3-LU/TestingPlatform](https://github.com/NC3-LU/TestingPlatform)

---

## Architecture

v4 is a full-stack application structured around autonomous backend modules. Each module lives in its own repository, exposes a consistent REST API, and can be deployed and tested independently.

| Layer | Description |
|---|---|
| **Modules** | Independent analysis services, one per security check domain |
| **API Gateway** | Central orchestration and routing layer *(planned)* |
| **Frontend** | User-facing interface consuming the gateway *(planned)* |

---

## Modules

| Module | Description |
|--------|-------------|
| [**subdomainenum**](https://github.com/NC3-TestingPlatform/subdomainenum) | Passive & active subdomain discovery |
| [**mailvalidator**](https://github.com/NC3-TestingPlatform/mailvalidator) | SPF, DKIM, DMARC and mail exchange validation |
| [**headersvalidator**](https://github.com/NC3-TestingPlatform/headersvalidator) | HTTP security header analysis |
| [**chainvalidator**](https://github.com/NC3-TestingPlatform/chainvalidator) | TLS/SSL certificate chain & DNSSEC validation |
| [**zoneripper**](https://github.com/NC3-TestingPlatform/zoneripper) | DNSSEC zone walking vulnerability testing |

A full-stack repository (frontend, API gateway, orchestration layer) will follow once the module layer is stable.

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
