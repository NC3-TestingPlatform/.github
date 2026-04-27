# NC3 Testing Platform

> **v3** is live at [testing.nc3.lu](https://testing.nc3.lu/) · source at [NC3-LU/TestingPlatform](https://github.com/NC3-LU/TestingPlatform)
> This organisation hosts the development of **v4** — a ground-up rewrite with a modular backend architecture.

---

## Overview

The NC3 Testing Platform is a set of security and network analysis tools maintained by [NC3.lu](https://nc3.lu/). It helps users evaluate domains and mail infrastructure for common misconfigurations and security weaknesses.

v4 is designed as a full-stack application built around independent backend modules. Each module lives in its own repository with a consistent interface, allowing the platform core to compose and orchestrate them as needed.

---

## Repositories

These repositories are the building blocks of the v4 backend:

| Module | Description |
|---|---|
| [subdomainenum](https://github.com/NC3-TestingPlatform/subdomainenum) | Subdomain enumeration via passive and active techniques |
| [mailvalidator](https://github.com/NC3-TestingPlatform/mailvalidator) | SPF, DKIM, DMARC and mail exchange validation |
| [headersvalidator](https://github.com/NC3-TestingPlatform/headersvalidator) | HTTP security header analysis |
| [chainvalidator](https://github.com/NC3-TestingPlatform/chainvalidator) | TLS/SSL certificate chain validation |
| [zoneripper](https://github.com/NC3-TestingPlatform/zoneripper) | DNS zone analysis and record enumeration |

A full-stack repository (frontend, API gateway, orchestration layer) will follow once the module layer is stable.

---

## Status

| Component | Status |
|---|---|
| Backend modules | In development |
| API gateway | Planned |
| Frontend | Planned |
| v4 release | Planned |

---

## About NC3

[NC3.lu](https://nc3.lu/) (National Cybersecurity Competence Center) is a Luxembourg public interest organisation dedicated to cybersecurity research, training, and tooling.
