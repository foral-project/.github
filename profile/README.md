<div align="center">

# Foral

**Governance as code for federated repositories.**

Define schemas, enforce policies, validate compliance — across autonomous repos.

[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/license/apache-2-0/)
[![JSON Schema](https://img.shields.io/badge/JSON%20Schema-Draft%202020--12-green.svg)](https://json-schema.org/draft/2020-12/schema)
[![JSON-LD](https://img.shields.io/badge/JSON--LD-1.1-orange.svg)](https://www.w3.org/TR/json-ld11/)
[![OPA](https://img.shields.io/badge/OPA-CNCF%20Graduated-blueviolet.svg)](https://www.openpolicyagent.org/)
[![Go](https://img.shields.io/badge/Go-1.22+-00ADD8.svg)](https://go.dev/)

[Specification](https://github.com/foral-project/protocol/blob/main/PROTOCOL.md) ·
[Adopting Guide](https://github.com/foral-project/governance/blob/main/ADOPTING.md) ·
[Schemas](https://foral-project.github.io/protocol/schemas/v1/) ·
[Policies](https://foral-project.github.io/governance/policies/)

</div>

---

## What it does

Foral lets you govern multiple repositories through a shared protocol. Each repo declares a manifest (`catalog-info.yaml`), and CI workflows validate it against centralized schemas and OPA policies.

The protocol defines **what** is valid. The governance layer enforces **how** and **when**.

## Quick Start

```bash
# Install CLI
go install github.com/foral-project/cli@latest

# Scaffold a governed project
foral init my-project --owner my-org

# Validate compliance
cd my-project && foral validate
```

Or without CLI — [two YAML files and you're done](https://github.com/foral-project/governance/blob/main/ADOPTING.md#opção-3-manual-qualquer-git-host).

## Repositories

| Repo | Role | Live |
|---|---|---|
| [protocol](https://github.com/foral-project/protocol) | Specification, schemas, JSON-LD contexts | [Pages](https://foral-project.github.io/protocol/) |
| [governance](https://github.com/foral-project/governance) | Reusable workflows, OPA policies, federation | [Pages](https://foral-project.github.io/governance/) |
| [cli](https://github.com/foral-project/cli) | `foral init` · `validate` · `status` | [Releases](https://github.com/foral-project/cli/releases) |
| [template](https://github.com/foral-project/template) | GitHub template for new projects | [Use template →](https://github.com/foral-project/template/generate) |

## Standards

| Artifact | Standard | Org |
|---|---|---|
| Schemas | JSON Schema Draft 2020-12 | IETF |
| Semantic contexts | JSON-LD 1.1 | W3C |
| Manifest | Backstage catalog-info.yaml | CNCF |
| Naming | RFC 1123 DNS Labels | IETF |
| Policies | OPA/Conftest | CNCF |
| Versioning | SemVer 2.0.0 | semver.org |
| Commits | Conventional Commits 1.0.0 | — |

## License

[Apache-2.0](https://opensource.org/license/apache-2-0/)
