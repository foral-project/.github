<div align="center">

# 🏛️ Foral

**Protocolo de federação constitucional para governança de repositórios.**

Inspirado nos **forais medievais portugueses** — cartas reais que concediam
autonomia a municípios dentro de limites constitucionais definidos pela Coroa.

[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/license/apache-2-0/)
[![JSON Schema](https://img.shields.io/badge/JSON%20Schema-Draft%202020--12-green.svg)](https://json-schema.org/draft/2020-12/schema)
[![JSON-LD](https://img.shields.io/badge/JSON--LD-1.1-orange.svg)](https://www.w3.org/TR/json-ld11/)
[![OPA](https://img.shields.io/badge/OPA-CNCF%20Graduated-blueviolet.svg)](https://www.openpolicyagent.org/)
[![Go](https://img.shields.io/badge/Go-1.22+-00ADD8.svg)](https://go.dev/)

[Especificação](https://github.com/foral-project/protocol/blob/main/PROTOCOL.md) ·
[Guia de Adoção](https://github.com/foral-project/governance/blob/main/ADOPTING.md) ·
[Schemas Live](https://foral-project.github.io/protocol/schemas/v1/) ·
[Policies Live](https://foral-project.github.io/governance/policies/)

</div>

---

## O que é

O Foral é um **framework de governança federada** que permite governar múltiplos repositórios autônomos através de um contrato constitucional.

Cada repositório mantém total autonomia — mas opera dentro de limites definidos pelo protocolo.

```
Protocol (constituição)  →  Governance (judiciário)  →  Membros (municípios)
       schemas                 CI gates + OPA             repos autônomos
       templates               reusable workflows         catalog-info.yaml
       JSON-LD contexts        federation registry        compliance
```

## Início Rápido

```bash
# Instalar CLI
go install github.com/foral-project/cli@latest

# Scaffold de novo projeto governado
foral init my-project --owner my-org

# Validar compliance
cd my-project && foral validate

# Ver dashboard de status
foral status
```

Ou sem CLI — [2 arquivos YAML e pronto](https://github.com/foral-project/governance/blob/main/ADOPTING.md#opção-3-manual-qualquer-git-host).

## Repositórios

| Repo | Papel | Live |
|---|---|---|
| 📜 **[protocol](https://github.com/foral-project/protocol)** | Especificação, schemas, templates, JSON-LD | [foral-project.github.io/protocol](https://foral-project.github.io/protocol/) |
| ⚖️ **[governance](https://github.com/foral-project/governance)** | Reusable workflows, OPA policies, federation | [foral-project.github.io/governance](https://foral-project.github.io/governance/) |
| 🔧 **[cli](https://github.com/foral-project/cli)** | `foral init` · `validate` · `status` · `version` | [Releases](https://github.com/foral-project/cli/releases) |
| 📦 **[template](https://github.com/foral-project/template)** | GitHub template repo (Use this template) | [Usar template →](https://github.com/foral-project/template/generate) |

## Standards

Zero formatos inventados. Cada artefato rastreia a um standard da indústria:

| Artefato | Standard | Organização |
|---|---|---|
| Schemas | JSON Schema Draft 2020-12 | IETF |
| Contextos semânticos | JSON-LD 1.1 | W3C |
| Manifesto | Backstage catalog-info.yaml | CNCF |
| Naming | RFC 1123 DNS Labels | IETF |
| Eventos | CloudEvents 1.0.3 | CNCF |
| Policies | OPA/Conftest | CNCF |
| Versioning | SemVer 2.0.0 | semver.org |
| Commits | Conventional Commits 1.0.0 | — |
| Licença | Apache-2.0 | OSI |

## Licença

[Apache-2.0](https://opensource.org/license/apache-2-0/) — SPDX-License-Identifier: Apache-2.0
