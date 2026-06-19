# Contributing to NC3 Testing Platform

Thank you for your interest in contributing to the NC3 Testing Platform!
All modules are open source and contributions are welcome.

## Code of Conduct

By participating in this project you agree to abide by our [Code of Conduct](CODE_OF_CONDUCT.md).
Please treat all contributors with respect and maintain a welcoming environment.

## How to Contribute

### 1. Fork and Clone

```bash
# Fork the repository on GitHub, then clone your fork
git clone https://github.com/<your-username>/<repo>.git
cd <repo>
git remote add upstream https://github.com/NC3-TestingPlatform/<repo>.git
```

### 2. Create a Branch

Always work on a dedicated branch — never commit directly to `master`.

```bash
git checkout -b feat/my-feature   # new feature
git checkout -b fix/issue-42      # bug fix
git checkout -b docs/update-readme
```

Branch naming convention:
- `feat/` — new feature or enhancement
- `fix/` — bug fix
- `docs/` — documentation only
- `chore/` — maintenance tasks (deps, CI, etc.)

### 3. Make Your Changes

- Follow the code style used in the repository (linting configs are in the repo root).
- Write or update tests for any changed behaviour.
- Keep commits focused and atomic; write clear commit messages:

```
fix: correct DNSSEC chain validation for wildcard records

Resolves #42. The previous logic skipped wildcard NSEC3 entries.
```

### 4. Open a Pull Request

1. Push your branch to your fork: `git push origin feat/my-feature`
2. Open a PR against the `master` branch of the upstream repository.
3. Fill in the PR template completely.
4. Ensure all CI checks pass before requesting review.
5. Address review feedback promptly; force-push to the same branch to update.

PRs are merged by the `@NC3-TestingPlatform/maintainers` team after at least one approving review.

## Issue Triage Process

| Label | Meaning |
|-------|---------|
| `triage` | Newly opened, not yet reviewed |
| `confirmed` | Reproduced and accepted |
| `good first issue` | Suitable for first-time contributors |
| `help wanted` | Extra attention needed from community |
| `blocked` | Waiting on external dependency or decision |
| `wontfix` | Out of scope or by design |

New issues are triaged weekly by the maintainers team.
If your issue has not received a response within 7 days, feel free to ping `@NC3-TestingPlatform/maintainers`.

## Security Issues

**Do not open public issues for security vulnerabilities.**
Please follow the [Security Policy](SECURITY.md) and report privately.

## Contact

For questions, collaboration proposals, or general inquiries:
- Email: [opensource@nc3.lu](mailto:opensource@nc3.lu)
- Website: [testing.nc3.lu](https://testing.nc3.lu/)
