<div align="center">

# AI-BOM Inspector

### Deterministic security analysis for the AI supply chain.

<a href="https://github.com/MellyFinnese/AI-BOM-Inspector">
  <img src="https://img.shields.io/badge/Explore-AI--BOM--Inspector-111827?style=for-the-badge&logo=github" alt="AI-BOM Inspector" />
</a>
<img src="https://img.shields.io/badge/AI%20Supply%20Chain-Security-7c3aed?style=for-the-badge" alt="AI Supply Chain Security" />
<img src="https://img.shields.io/badge/Architecture-Offline--First-0f766e?style=for-the-badge" alt="Offline First" />

</div>

---

## What is AI-BOM Inspector?

**AI-BOM Inspector** is an offline-first security engineering platform for analyzing the software, models, artifacts, and relationships that make up modern AI systems.

Traditional SBOM tooling can tell you **what components exist**. AI-BOM Inspector is designed to answer the harder questions:

- What AI assets are actually present?
- What evidence indicates that something is risky?
- Which models, packages, applications, and owners are affected?
- How far can a vulnerability propagate through the AI supply chain?
- Should a build be allowed, warned on, or blocked?
- Can the decision be reproduced and explained later?

The project is built around one principle:

> **AI security decisions should be traceable, reproducible, testable, and enforceable.**

---

## The architecture

```text
        AI Project
            │
            ├── SBOMs / manifests
            ├── Models / artifacts
            └── Metadata
                    │
                    ▼
          Discovery + Normalization
                    │
                    ▼
            Evidence + Context
                    │
                    ▼
        ┌─────────────────────────┐
        │ Deterministic Risk     │
        │ Engine                  │
        └─────────────────────────┘
                    │
                    ▼
              Policy Engine
                    │
          ┌─────────┴─────────┐
          ▼                   ▼
       Allow/Warn           Block
          │                   │
          └─────────┬─────────┘
                    ▼
          Report / CI / Evidence
```

The key architectural boundary is intentional: **relationship and graph context can enrich impact analysis without becoming the source of truth for deterministic risk scoring.**

That makes graph backends optional and keeps the core engine independently testable.

---

## Why AI-BOM Inspector is different

### 🧠 AI assets are first-class

Models and artifacts are analyzed alongside normal software dependencies instead of being treated as opaque files.

### 🎯 Deterministic by design

The core security decision does not depend on hosted LLM inference. The same inputs can produce a reproducible result.

### 🔎 Evidence over guesswork

Findings are designed to remain connected to the observations, identities, relationships, and evidence behind them.

### 🕸️ Relationship-aware impact analysis

A vulnerability can be traced through a chain such as:

```text
CVE
 ↓
Package
 ↓
AI Framework
 ↓
Model
 ↓
Application
 ↓
Owner
```

This turns an isolated vulnerability into an explainable **blast-radius problem**.

### 🛡️ The scanner gets attacked too

Security hardening is treated as part of the product rather than an afterthought. Confirmed weaknesses become regression tests and are used to strengthen the scanner itself.

---

## What it analyzes

- Python, JavaScript, Go, and Java dependencies
- CycloneDX and SPDX SBOMs
- AI model metadata and model references
- Model artifacts and hashes
- Safetensors and pickle-related security signals
- Dependency pinning and version posture
- Model freshness and provenance signals
- License and governance posture
- Vulnerability/advisory enrichment
- Policy-as-code decisions
- Organizational context such as criticality and data sensitivity

## What it produces

- Deterministic risk scores
- Explainable findings
- Policy decisions
- JSON, Markdown, and HTML reports
- SARIF / CI-oriented outputs
- CycloneDX and SPDX exports
- Evidence and attestation artifacts
- Dependency and impact context
- Scan-to-scan diffs

---

## Graph reasoning

AI-BOM Inspector includes a backend-neutral graph/context architecture for relationship-heavy security questions.

A graph database such as **Memgraph** can be used where graph traversal provides measurable value, including:

```text
"Which applications are affected by this vulnerability?"

"Which models depend on this package?"

"What is the common dependency between these findings?"

"What is the blast radius of this AI supply-chain issue?"
```

The graph layer is deliberately separated from the deterministic risk engine so graph infrastructure can improve **context, traversal, and explanation** without silently changing the underlying security score.

---

## Reproducible proof

The repository contains a reproducible vulnerable-AI project designed to demonstrate the complete decision path:

```text
Vulnerable AI project
        ↓
      Scan
        ↓
    Findings
        ↓
 Risk decision
        ↓
Policy evaluation
        ↓
Evidence / report
        ↓
CI-style enforcement
```

Run it with:

```bash
PYTHONPATH=src bash demo/golden-vulnerable-ai/run_demo.sh
```

The goal is **claim → proof**, not a feature-list disguised as a security product.

---

## Security model

The project explicitly distinguishes security concepts that are easy to blur together:

- **Integrity digest** ≠ **cryptographic signature**
- **Self-consistent trust root** ≠ **externally trusted root**
- **Missing evidence** ≠ **positive evidence**
- **Canonical component identity** ≠ **name-only matching**
- **Controlled policy failure** ≠ **silent exception**

Those distinctions matter because the scanner itself sits inside the security boundary.

---

## Offline-first

The default posture is local and privacy-preserving.

```bash
aibom scan --format json
```

Online enrichment is opt-in when external advisory or model information is required. Local-only and safe-mode controls can be used when outbound requests must be prevented.

---

## Built to evolve

AI-BOM Inspector is an actively evolving security-engineering project spanning:

```text
AI Supply Chain
      │
      ├── SBOM / BOM generation
      ├── Model security
      ├── Dependency intelligence
      ├── Evidence modeling
      ├── Deterministic risk
      ├── Policy enforcement
      ├── Graph impact analysis
      └── CI / audit workflows
```

The architecture is designed to support deeper application, ownership, blast-radius, and attack-path reasoning without sacrificing a deterministic security core.

---

## Explore the project

**Repository:** [MellyFinnese/AI-BOM-Inspector](https://github.com/MellyFinnese/AI-BOM-Inspector)

**Architecture:** [`docs/ARCHITECTURE.md`](https://github.com/MellyFinnese/AI-BOM-Inspector/blob/main/docs/ARCHITECTURE.md)

**Security validation:** [`docs/SECURITY_VALIDATION.md`](https://github.com/MellyFinnese/AI-BOM-Inspector/blob/main/docs/SECURITY_VALIDATION.md)

**Scoring model:** [`docs/SCORING.md`](https://github.com/MellyFinnese/AI-BOM-Inspector/blob/main/docs/SCORING.md)

---

<div align="center">

### Inspect. Explain. Prove. Enforce.

AI-BOM Inspector is an experiment in what AI supply-chain security looks like when **evidence, relationships, and deterministic decisions** are treated as first-class engineering primitives.

</div>
