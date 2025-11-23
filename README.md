diff --git a/README.md b/README.md
index 8b137891791fe96927ad78e64b0aad7bded08bdc..8ab147053884a86bc9e42440fa12200355578f2b 100644
--- a/README.md
+++ b/README.md
@@ -1 +1,127 @@
+<div align="center">
+  <h1>Hey, I'm Melly or Crypto — AI x Supply Chain Security Engineer</h1>
+  <p><em>Edge mindset, disciplined shipping. I build tools that explain risk instead of hiding it.</em></p>
+  <img src="https://github-readme-streak-stats.herokuapp.com?user=MellyFinnese&theme=tokyonight&hide_border=true" alt="GitHub Streak"/>
+</div>
 
+---
+
+## 🚀 Run a Quick Scan 
+```bash
+ai-bom-inspector \
+  --sbom path/to/sbom.json \
+  --format cyclonedx \
+  --verbose
+```
+
+- 💡 Drop into CI to block risky builds.
+- 📝 Rich explanations: CVEs, abandonware signals, license conflicts.
+- 🎯 Outputs CycloneDX/SPDX for the rest of your stack.
+
+## 🗂 Project Shelf (pinned for a reason)
+- 🧪 **AI-BOM Inspector** — AI + SBOM risk intel, license clarity, CI-ready.
+- 🛰 **Low-Level / Firmware Lab** — boot/OS experiments, failure hunts, hardware-near tooling.
+- ⚙️ **Clean Utility** — small but fully documented CLI with tests; proving discipline over hype.
+- 🧱 **Security Toolkit Skeleton** — reusable template for future offensive/defensive tools.
+
+> Pin the work that shows intent, not the tutorial leftovers.
+
+## 🗺 AI-BOM Inspector — Code ➜ Clarity Flow
+```mermaid
+graph TD;
+    A[SBOM: CycloneDX/SPDX] --> B[Parse & Normalize];
+    B --> C[Risk Engine];
+    B --> D[License Intel];
+    C --> E[Score: Critical · High · Medium · Low];
+    C --> F[Explain: CVEs · Maintenance · Exposure];
+    D --> G[Detect: License Conflicts · Copyleft Issues];
+    E --> H[CI/CD Gating];
+    F --> I[Reports];
+    G --> I;
+    H --> J[GitHub Action / Pipelines];
+```
+
+**Promises that matter**
+- Granular scoring (CVSS, maintenance health, popularity, ecosystem).  
+- Explain every flag (CVE, abandonware, license conflict) and suggest safer alternatives.  
+- GitHub Action & CI/CD mode to gate merges above a risk threshold.  
+- Lightweight dashboard/TUI to watch dependency health over time.
+
+## 🧰 Skill Matrix
+<div align="center">
+  <img src="https://skillicons.dev/icons?i=python,rust,c,linux,docker,git,githubactions,vscode&perline=8" />
+</div>
+
+<details>
+  <summary><b>🧪 Languages</b></summary>
+  <ul>
+    <li>Python — security tooling, CLIs, end-to-end workflows.</li>
+    <li>Rust — performance + safety when both matter.</li>
+    <li>C — peel away abstractions and see real behavior.</li>
+  </ul>
+</details>
+
+<details>
+  <summary><b>🛡 Security / Domain</b></summary>
+  <ul>
+    <li>SBOMs (CycloneDX/SPDX) and supply-chain analysis.</li>
+    <li>Dependency intelligence: risk, licenses, maintenance, ecosystem signals.</li>
+    <li>CI/CD hooks, GitHub Actions, risk-based gating.</li>
+    <li>Attacker mindset to build defenses that actually hold.</li>
+  </ul>
+</details>
+
+<details>
+  <summary><b>⚙️ Ecosystem</b></summary>
+  <ul>
+    <li>Linux as the lab.</li>
+    <li>Docker for reproducible environments.</li>
+    <li>GitHub Actions for continuous checks & automation.</li>
+    <li>Issues / Discussions as feedback loops.</li>
+  </ul>
+</details>
+
+## 🧠 Philosophy — Edge, Not Villain
+- I care about how systems really fail, not just the happy path.  
+- Curiosity fuels tools that reduce blast radius, not increase it.  
+- Ship fewer things, make them count. Antihero energy: aware of the dark, pointed toward defense.
+
+## 📈 Recently Shipped
+- ✅ Initial release of AI-BOM Inspector CLI.  
+- ✅ SBOM parsing + base risk highlighting.  
+- ✅ External review folded into roadmap (scoring, explainability, integrations).  
+- 🔜 GitHub Action: auto-comment risk insights on PRs.  
+- 🔜 CI/CD risk threshold mode: fail builds when dependency trees get sketchy.
+
+## 🛰 Ops Log
+<details open>
+  <summary><b>Timeline</b></summary>
+
+  - 2025-11 — AI-BOM Inspector tested by external users; workflow + feature ideas captured.  
+  - 2025-11 — GitHub profile refocused around AI x security, supply-chain defense, low-level work.  
+  - 2025-11 — Roadmap shaped: granular risk, explanations, remediation, GH Action, CI/CD.  
+  - 2025-12+ — Focus: integrations, more real SBOMs, polished UX for teams.
+</details>
+
+## 📊 GitHub Pulse
+<div align="center">
+  <img src="https://github-readme-activity-graph.vercel.app/graph?username=MellyFinnese&theme=tokyo-night" alt="Activity Graph" />
+  <br/><br/>
+  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=MellyFinnese&layout=compact&theme=tokyonight" alt="Top Langs" />
+</div>
+
+## 🧾 Project Hygiene Checklist (for trusted repos)
+- LICENSE — explicit (MIT / Apache-2.0 / etc.).
+- SECURITY.md — how to report issues responsibly.
+- CONTRIBUTING.md — how to open issues / PRs without wasting time.
+- CODE_OF_CONDUCT.md — shows you run a serious project.
+- GitHub Actions workflow (tests / lint) + CI badge in README.
+
+## 🤝 Collaborate
+If you’re working on security tooling, SBOM workflows / supply-chain security, or AI x SecOps and want to pair antihero perspective with disciplined engineering, reach out.
+
+<div align="center">
+
+🔗 <a href="https://mellyfinnese.github.io">mellyfinnese.github.io</a> — lab / landing (WIP)
+
+</div>

