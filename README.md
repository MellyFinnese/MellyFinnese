<div align="center">

# AI-BOM INSPECTOR

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&size=26&duration=2200&pause=700&color=7C3AED&center=true&vCenter=true&width=900&lines=Independent+Security+Engineer;AI+Supply-Chain+Security;Graph+%7C+Provenance+%7C+Impact+Analysis;Build+%7C+Break+%7C+Measure+%7C+Harden" alt="MellyFinnese" />

<p>
  <a href="https://github.com/MellyFinnese/AI-BOM-Inspector"><img src="https://img.shields.io/badge/PROJECT-AI--BOM%20INSPECTOR-111827?style=for-the-badge&logo=github" /></a>
  <img src="https://img.shields.io/badge/SECURITY-ENGINEERING-DC2626?style=for-the-badge" />
  <img src="https://img.shields.io/badge/AI-SUPPLY%20CHAIN-7C3AED?style=for-the-badge" />
  <img src="https://img.shields.io/badge/OFFLINE--FIRST-0F766E?style=for-the-badge" />
</p>

<p><strong>I build security systems around problems that are still poorly modeled.</strong><br/>My current focus is AI supply-chain security, evidence, provenance, graph reasoning, and change-aware impact analysis.</p>

</div>

---

## Validation, Not Just Claims

My flagship project is currently backed by:

```text
152 tests passed
1 skipped
0 failed

JavaScript / TypeScript benchmark
30 labeled cases
Precision: 93.94%
Recall:    95.38%
F1:        94.66%
```

The benchmark includes positive, clean-negative, and adversarial-negative cases. The quality gate remains **precision, recall, and F1 >= 0.90**.

---

# What I'm Building

## AI-BOM Inspector

**AI-BOM Inspector** is my independent security-engineering project for turning AI supply-chain inventory into deterministic, evidence-backed security decisions.

It has evolved from AIBOM/SBOM scanning into a connected analysis workflow:

```text
AI / JS / TS source
        ↓
Discovery + semantic analysis
        ↓
Evidence + relationships
        ↓
AI-BOM identity / provenance
        ↓
Deterministic risk
        ↓
Impact / attack paths
        ↓
Behavioral drift
        ↓
Blast-radius context
        ↓
CI / policy enforcement
        ↓
Graph investigation
```

The core remains deterministic and offline-first. Graph infrastructure provides context and investigation rather than silently replacing the risk engine's source of truth.

### The security object I'm pushing hardest

```text
HTTP Input
    ↓
Prompt
    ↓
Agent
    ↓
Tool
    ↓
Privileged Operation
```

A change can then be evaluated as:

```text
Did the reachable graph change?
        ↓
Did a new impact path appear?
        ↓
What evidence supports it?
        ↓
What AI assets are downstream?
        ↓
Should CI block the change?
```

That is the direction I'm taking the project: **from inventory toward AI-system impact intelligence.**

---

# Engineering Principles

**Deterministic first.** Security decisions should be reproducible from the same evidence.

**Evidence over assumptions.** Findings should remain traceable to what was actually observed.

**Identity matters.** Models, versions, artifacts, and provenance need stable identity.

**Relationships matter.** Risk becomes operationally useful when you can understand what a change affects.

**Graph is context, not magic.** Traversal should explain and enrich decisions, not become an opaque scoring system.

**Attack the assumptions.** Adversarial cases, regression tests, and negative benchmarks are part of the engineering loop.

**Offline-first.** The default security path should not require shipping sensitive source code or metadata to a hosted model.

---

# Technical Focus

```text
Languages       Python · Rust · JavaScript · TypeScript
Security        AI security · Supply-chain security · SBOM/AIBOM
Analysis        Static analysis · risk modeling · attack paths · behavioral drift
Data            CycloneDX · SPDX · provenance · evidence · attestations
Graph           Memgraph · backend-neutral graph abstractions
Engineering     CLI tooling · CI enforcement · regression testing · benchmarking
```

---

# Proof Loop

```text
Build
  ↓
Measure
  ↓
Attack assumptions
  ↓
Inspect failures
  ↓
Add regression coverage
  ↓
Fix the underlying design
  ↓
Benchmark again
```

The important part is the loop, not the tool used to accelerate it.

---

# Current Direction

I'm building toward an AI-system graph that can connect:

```text
Dataset
   ↓
Training Run
   ↓
Fine-Tuned Model
   ↓
Model Version
   ↓
Artifact
   ↓
Deployment
   ↓
API
   ↓
Agent
   ↓
Prompt
   ↓
Tool
   ↓
Application
```

with evidence attached to identities and relationships.

The questions I care about are:

```text
What changed?
What is connected?
What became reachable?
What is affected?
Why?
Can the result be reproduced?
```

---

# Featured Project

<p align="center">
  <a href="https://github.com/MellyFinnese/AI-BOM-Inspector"><img src="https://img.shields.io/badge/EXPLORE-AI--BOM%20INSPECTOR-7C3AED?style=for-the-badge&logo=github" /></a>
</p>

**AI-BOM Inspector** is the canonical home for the project, its implementation history, architecture, benchmarks, experiments, and security validation.

---

<div align="center">

### Build. Break. Measure. Harden.

<strong>Independent security engineering focused on the AI supply chain.</strong>

</div>
