<div align="center">

<pre>
 █████╗ ██╗       ██████╗  ██████╗ ███╗   ███╗
██╔══██╗██║      ██╔═══██╗██╔═══██╗████╗ ████║
███████║██║      ██║   ██║██║   ██║██╔████╔██║
██╔══██║██║      ██║   ██║██║   ██║██║╚██╔╝██║
██║  ██║███████╗ ╚██████╔╝╚██████╔╝██║ ╚═╝ ██║
╚═╝  ╚═╝╚══════╝  ╚═════╝  ╚═════╝ ╚═╝     ╚═╝

 ██╗███╗   ██╗███████╗██████╗ ███████╗ ██████╗████████╗ ██████╗ ██████╗
 ██║████╗  ██║██╔════╝██╔══██╗██╔════╝██╔════╝╚══██╔══╝██╔═══██╗██╔══██╗
 ██║████╗ ██║███████╗██████╔╝█████╗  ██║        ██║   ██║   ██║██████╔╝
 ██║██╔██╗ ██║╚════██║██╔═══╝ ██╔══╝  ██║        ██║   ██║   ██║██╔═══╝
 ██║██║╚██╗██║███████║██║     ███████╗╚██████╗   ██║   ╚██████╔╝██║
 ╚═╝╚═╝  ╚═══╝╚══════╝╚═╝     ╚══════╝ ╚═════╝   ╚═╝    ╚═════╝ ╚═╝
</pre>

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

# 🧠 What I'm Building

## AI-BOM Inspector

**AI-BOM Inspector** is my independent security-engineering project for turning AI supply-chain inventory into deterministic, evidence-backed security decisions.

It started with the question:

> **What does an AI system actually contain, and what happens when one of those components changes or becomes compromised?**

The project has evolved beyond simple SBOM scanning into a connected analysis workflow:

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

The core is deterministic and offline-first. Graph infrastructure is used for context and investigation rather than being allowed to silently replace the risk engine's source of truth.

### Current architecture

```text
┌────────────────────────────────────────────────────┐
│                  AI-BOM INSPECTOR                  │
├────────────────────────────────────────────────────┤
│                                                    │
│  Dependencies      Models       Artifacts          │
│       │               │              │             │
│       └───────────────┼──────────────┘             │
│                       ▼                            │
│               Evidence + Identity                 │
│                       │                            │
│             ┌─────────┴─────────┐                  │
│             ▼                   ▼                  │
│     Deterministic Risk     Relationship Graph      │
│             │                   │                  │
│             └─────────┬─────────┘                  │
│                       ▼                            │
│            Impact / Attack Paths                  │
│                       │                            │
│                 Behavioral Drift                  │
│                       │                            │
│             ┌─────────┴─────────┐                  │
│             ▼                   ▼                  │
│           Policy              Memgraph             │
│             │                   │                  │
│             └─────────┬─────────┘                  │
│                       ▼                            │
│                 CI / Evidence                     │
│                                                    │
└────────────────────────────────────────────────────┘
```

### The part I'm pushing hardest

The project now treats an impact path as a first-class security object:

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

A code change can therefore be evaluated as:

```text
Did the reachable security graph change?
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

# 🔬 Engineering Principles

**Deterministic first.** Security decisions should be reproducible from the same evidence.

**Evidence over assumptions.** Findings should remain traceable to what was actually observed.

**Identity matters.** A component name isn't enough; models, versions, artifacts, and provenance need stable identity.

**Relationships matter.** A vulnerability or code change only becomes operationally useful when you can understand what it affects.

**Graph is context, not magic.** Graph traversal should explain and enrich decisions, not silently become an opaque scoring system.

**Attack the assumptions.** Clean demos aren't enough. I build adversarial cases, regression tests, and negative benchmarks to find where the tooling lies.

**Offline-first.** The default security path should not require shipping sensitive source code or metadata to a hosted model.

---

# ⚙️ What I'm Working With

```text
Languages       Python · Rust · JavaScript · TypeScript
Security        Supply-chain security · AI security · SBOM/AIBOM · provenance
Analysis        Static analysis · risk modeling · attack paths · behavioral drift
Data            CycloneDX · SPDX · evidence · attestations · graph relationships
Graph           Memgraph · backend-neutral graph abstractions
Engineering     CLI tooling · CI enforcement · regression testing · benchmarking
```

---

# 🧪 Proof, Not Just Prototypes

AI-BOM Inspector includes a reproducible vulnerable-AI project and an adversarial benchmark corpus.

The project tests both sides of the scanner:

```text
Positive cases
    ↓
Can it find the problem?

Negative / adversarial cases
    ↓
Can it avoid inventing the problem?

Behavioral diff
    ↓
Can it identify a newly reachable path?

Graph context
    ↓
Can it explain the impact?
```

That validation loop is part of the product, not an afterthought.

---

# 🧭 Current Direction

The long-term model I'm building toward is an AI-system graph that can represent:

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

with evidence attached to the identities and relationships.

The interesting questions are then:

```text
What changed?
What is connected?
What became reachable?
What is affected?
Why did the system make this decision?
Can the result be reproduced?
```

---

# 🚀 Featured Project

<p align="center">
  <a href="https://github.com/MellyFinnese/AI-BOM-Inspector"><img src="https://img.shields.io/badge/EXPLORE-AI--BOM%20INSPECTOR-7C3AED?style=for-the-badge&logo=github" /></a>
</p>

**AI-BOM Inspector** is the main project where I am putting these ideas into code, benchmarks, experiments, and security engineering practice.

The repository is the canonical home for the project, its architecture, experiments, and implementation history.

---

<div align="center">

### ⚡ Build. Break. Measure. Harden. ⚡

<strong>Independent security engineering focused on the AI supply chain.</strong>

</div>
