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
 ██║██╔██╗ ██║███████╗██████╔╝█████╗  ██║        ██║   ██║   ██║██████╔╝
 ██║██║╚██╗██║╚════██║██╔═══╝ ██╔══╝  ██║        ██║   ██║   ██║██╔═══╝
 ██║██║ ╚████║███████║██║     ███████╗╚██████╗   ██║   ╚██████╔╝██║
 ╚═╝╚═╝  ╚═══╝╚══════╝╚═╝     ╚══════╝ ╚═════╝   ╚═╝    ╚═════╝ ╚═╝
</pre>

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&size=26&duration=2200&pause=700&color=7C3AED&center=true&vCenter=true&width=900&lines=AI+Supply-Chain+Security;Inspect+Models+%7C+Map+Risk+%7C+Prove+Impact;Deterministic+%7C+Explainable+%7C+Enforceable" alt="AI-BOM Inspector" />

<p>
  <a href="https://github.com/MellyFinnese/AI-BOM-Inspector"><img src="https://img.shields.io/badge/PROJECT-AI--BOM%20INSPECTOR-111827?style=for-the-badge&logo=github" /></a>
  <img src="https://img.shields.io/badge/AI-SUPPLY%20CHAIN-7C3AED?style=for-the-badge" />
  <img src="https://img.shields.io/badge/SECURITY-ENGINEERING-DC2626?style=for-the-badge" />
  <img src="https://img.shields.io/badge/OFFLINE--FIRST-0F766E?style=for-the-badge" />
</p>

<p><strong>Not another SBOM viewer.</strong><br/>AI-BOM Inspector is built to turn AI supply-chain evidence into decisions.</p>

</div>

---

# ⚡ AI-BOM Inspector

> **Inspect. Explain. Prove. Enforce.**

AI-BOM Inspector is an **offline-first, deterministic security engineering platform** for analyzing the software, models, artifacts, dependencies, and relationships that make up modern AI systems.

Traditional SBOM tooling tells you what exists.

AI-BOM Inspector asks what matters next:

```text
What is actually inside this AI system?
        ↓
What evidence indicates risk?
        ↓
What is affected?
        ↓
How far can the problem propagate?
        ↓
Should this build be allowed, warned on, or blocked?
        ↓
Can the decision be reproduced and defended?
```

---

## 🧠 The Core Idea

AI systems aren't just packages.

They're **packages + models + artifacts + runtimes + applications + relationships**.

AI-BOM Inspector treats those pieces as a connected security problem rather than isolated inventory.

```text
                    ┌──────────────────┐
                    │    AI PROJECT    │
                    └────────┬─────────┘
                             │
             ┌───────────────┼───────────────┐
             ▼               ▼               ▼
          SBOMs           MODELS          ARTIFACTS
             │               │               │
             └───────────────┼───────────────┘
                             ▼
                  ┌────────────────────┐
                  │ DISCOVERY +        │
                  │ NORMALIZATION      │
                  └─────────┬──────────┘
                            ▼
                  ┌────────────────────┐
                  │ EVIDENCE +         │
                  │ RELATIONSHIPS      │
                  └─────────┬──────────┘
                            ▼
                  ┌────────────────────┐
                  │ DETERMINISTIC      │
                  │ RISK ENGINE        │
                  └─────────┬──────────┘
                            ▼
                  ┌────────────────────┐
                  │ POLICY +           │
                  │ ENFORCEMENT        │
                  └─────────┬──────────┘
                            ▼
             ┌──────────────┼──────────────┐
             ▼              ▼              ▼
          ALLOW           WARN           BLOCK
```

The result isn't just a score.

It's an **explainable security decision backed by evidence**.

---

## 🔥 Why It Gets Interesting

### 🧬 AI assets are first-class

Models and artifacts are analyzed alongside ordinary dependencies instead of being treated as opaque files.

### 🎯 Deterministic security decisions

The core result doesn't require hosted LLM inference. Same evidence in → reproducible decision out.

### 🔎 Evidence over guesswork

Findings are designed to remain traceable to the observations, identities, relationships, and evidence behind them.

### 🕸️ Relationship-aware security

A vulnerability can become a chain instead of a row in a spreadsheet:

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

That turns **"there is a vulnerability"** into **"here is the blast radius."**

### 🛡️ The scanner gets attacked too

Security assumptions are challenged adversarially. Confirmed weaknesses become regression tests and hardening work instead of disappearing into a backlog.

---

## 💀 What It Can See

```text
┌────────────────────────────────────────────┐
│              AI SUPPLY CHAIN               │
├────────────────────────────────────────────┤
│                                            │
│  📦 Dependencies                           │
│  🧠 Models                                 │
│  📄 SBOMs                                  │
│  🧩 Artifacts                              │
│  🔐 Integrity signals                      │
│  ⚠️ Vulnerabilities                        │
│  📜 Licenses                               │
│  🏗️ Applications                           │
│  👤 Ownership / criticality                │
│  🔗 Relationships                           │
│  📋 Policies                               │
│                                            │
└────────────────────────────────────────────┘
```

It covers dependency manifests, CycloneDX/SPDX SBOMs, model metadata, model artifacts, Safetensors and pickle-related security signals, provenance, licensing, advisory enrichment, organizational context, policy-as-code, and CI enforcement.

---

## ⚔️ From Finding → Impact

The interesting part isn't finding a vulnerable package.

It's understanding what that package **means** inside an AI system.

```text
                VULNERABILITY
                      │
                      ▼
                   PACKAGE
                      │
                      ▼
                 FRAMEWORK
                      │
                      ▼
                    MODEL
                      │
                      ▼
                APPLICATION
                      │
                      ▼
                    OWNER
                      │
                      ▼
                 BLAST RADIUS
```

This is where inventory starts becoming **security intelligence**.

---

## 🧪 Proof, Not Marketing

The repository contains a reproducible vulnerable-AI project that demonstrates the full decision path:

```text
Vulnerable AI Project
        ↓
       Scan
        ↓
    Findings
        ↓
 Risk Decision
        ↓
Policy Evaluation
        ↓
Evidence / Report
        ↓
CI Enforcement
```

Run it:

```bash
PYTHONPATH=src bash demo/golden-vulnerable-ai/run_demo.sh
```

**Claim → reproduce → inspect → harden.**

---

## 🔐 Security Philosophy

The project deliberately keeps concepts separate that security tooling can easily blur:

```text
Integrity Digest       ≠ Cryptographic Signature
Trust Root             ≠ External Trust
Missing Evidence       ≠ Positive Evidence
Component Name         ≠ Canonical Identity
Policy Failure         ≠ Silent Exception
```

Because when the scanner sits inside the security boundary, **the scanner itself has to be trustworthy.**

---

## 🌐 Offline-First

Privacy isn't an add-on.

The default posture is local:

```bash
aibom scan --format json
```

External enrichment is opt-in. Local-only and safe-mode controls can prevent outbound requests when the environment requires it.

---

## 📊 What Comes Out

| Output | Purpose |
|---|---|
| 🎯 Risk score | Deterministic security posture |
| 🔎 Findings | Explainable evidence |
| 🧭 Impact context | Dependency / relationship reasoning |
| 🚦 Policy decision | Allow / warn / block |
| 📄 Reports | JSON / Markdown / HTML |
| 🛠️ CI output | SARIF / automated enforcement |
| 📦 Standards | CycloneDX / SPDX |
| 🧾 Evidence | Audit and provenance artifacts |
| 🔄 Diffing | Detect changes between scans |

---

## 🚀 The Bigger Direction

AI-BOM Inspector is evolving around a simple question:

> **What would AI supply-chain security look like if evidence, relationships, and deterministic decisions were treated as first-class primitives?**

The architecture is designed to push toward deeper reasoning around:

```text
AI Supply Chain
      │
      ├── Asset discovery
      ├── Model security
      ├── Dependency intelligence
      ├── Evidence modeling
      ├── Deterministic risk
      ├── Policy enforcement
      ├── Impact analysis
      ├── Blast-radius reasoning
      ├── Attack-path analysis
      └── CI / audit workflows
```

---

## 👁️ Explore the Experiment

<p align="center">
  <a href="https://github.com/MellyFinnese/AI-BOM-Inspector"><img src="https://img.shields.io/badge/ENTER-AI--BOM%20INSPECTOR-7C3AED?style=for-the-badge&logo=github" /></a>
</p>

<div align="center">

### ⚡ Inspect. Explain. Prove. Enforce. ⚡

<strong>AI-BOM Inspector</strong><br/>
An experiment in turning AI supply-chain inventory into security intelligence.

</div>
