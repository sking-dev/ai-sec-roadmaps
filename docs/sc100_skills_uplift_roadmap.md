<!--
 Source         : ChatGPT (GPT-4o)
 Date generated : 2025-07-07
 Title          : SC-100 Skills-Uplift Roadmap & Portfolio Plan
 License        : © 2025 sking-dev. Generated with assistance of OpenAI.
-->

# 🏗️ SC-100 Skills-Uplift Roadmap

## Practical Projects That Double as a Portfolio

| SC-100 Exam Domain | Weight | Portfolio Project & Timeline | Public Deliverables |
|--------------------|--------|------------------------------|---------------------|
| **1. Design a Zero-Trust strategy** | 25 % | **Project A – Zero-Trust Landing Zone** (Weeks 1-4) | - Terraform / Bicep hub-and-spoke with Firewall, Private Link, Bastion<br>- Conditional-Access baseline<br>- Architecture diagram + README |
| **2. Evaluate governance & compliance** | 20 % | **Project B – Policy-as-Code & Secure-Score Uplift** (Weeks 3-6) | - Custom Azure Policy set (CAF + CIS)<br>- Pipeline YAML (tfsec → `az policy assignment`)<br>- Before / after Secure Score screenshot |
| **3. Design infrastructure security** | 35 % | **Project C – AKS + OPA Gatekeeper + Signed SBOM** (Weeks 5-9) | - Rego policies (`require-signed-image`, `restrictPublicIP`)<br>- Trivy SBOM + Cosign script<br>- Kusto workbook for `DeniedPod` events |
| **4. Design security operations** | 20 % | **Project D – Sentinel + GPT-4o Incident "Triager"** (Weeks 8-12) | - Logic App → Azure Function → GPT-4o summary (MITRE-mapped)<br>- Teams Webhook demo GIF<br>- Token-cost worksheet |

---

## 🗓️ 12-Week Sprint Plan (≈ 5 h / week)

### Weeks 1-2  |  Foundation

1. Spin up Azure sub / credits 
2. `gh repo create sc100-portfolio --public`
3. Install Terraform, Azure CLI, VS Code plugins

### Weeks 1-4  |  Project A – Zero-Trust Landing Zone

- Build hub-and-spoke VNet, Firewall, Private DNS, Bastion
- Conditional-Access baseline (MFA, block legacy authentication)
- Capture diagram + deployment walkthrough

### Weeks 3-6  |  Project B – Policy-as-Code

- Convert CAF & CIS controls to custom Policy JSON
- Integrate **tfsec** in Azure DevOps pipeline
- Record Secure-Score uplift (e.g. 68 % → 92 %)

### Weeks 5-9  |  Project C – AKS Guardrails

- Deploy AKS with Gatekeeper add-on
- Write 3 Rego policies; enforce Cosign-signed images
- Generate SBOM via Trivy; visualise denied pods in Kusto

### Weeks 8-12  |  Project D – Sentinel + AI SOAR

- Custom Sentinel rule from AKS logs
- Logic App triggers Function → GPT-4o summary → Teams
- Include token-cost FinOps sheet

---

## 📂 Suggested Repo Structure

```plaintext
sc100-portfolio/
│
├─ project-a_zero-trust-landing-zone/
│   ├─ main.tf          # or.bicep files
│   └─ diagram.png
│
├─ project-b_policy-as-code/
│   ├─ policies/        # custom Azure Policy JSON
│   ├─ pipeline.yml     # tfsec → az policy assignment
│   └─ secure-score.md  # before / after results
│
├─ project-c_aks-guardrails/
│   ├─ gatekeeper/rego  # OPA policies
│   ├─ sbom_cosign.sh   # Trivy SBOM + Cosign script
│   └─ workbook.json    # Kusto workbook for audit events
│
├─ project-d_sentinel-gpt/
│   ├─ function-app/    # Python or JS Azure Function
│   ├─ logicapp.json    # Sentinel playbook
│   └─ demo.gif         # short screen-capture
│
└─ README.md            # table mapping projects ↔ SC-100 domains
```

---

## 🔑 CV / LinkedIn Bullet Ideas

- *“Designed Zero-Trust landing zone on Azure; automated via Terraform and lifted Secure Score from 68 % → 92 %.”*  
- *“Integrated OPA Gatekeeper and signed-SBOM enforcement in AKS, blocking unsigned images pre-prod.”*  
- *“Built GPT-4o-powered Sentinel playbook that cuts analyst triage time by ~25 % per incident.”*

---

## 📚 Core Study & How-To Links

- SC-100 Skill Outline → <https://aka.ms/SC100-skills>  
- Landing-Zone Terraform → <https://github.com/Azure/terraform-azurerm-caf-enterprise-scale>  
- Azure Policy Tutorial → <https://learn.microsoft.com/azure/governance/policy/tutorials/create-and-manage>  
- Gatekeeper on AKS → <https://learn.microsoft.com/azure/aks/governance-policy>  
- Sentinel Playbooks → <https://learn.microsoft.com/azure/sentinel/tutorial-use-playbooks>  
- Syft & Cosign → <https://github.com/anchore/syft> | <https://github.com/sigstore/cosign>  
- OpenAI Function Calling → <https://learn.microsoft.com/azure/ai-services/openai/how-to/function-calling>

---

## ✅ Action Checklist (Today)

1. Create repo & scaffold `project-a` README  
2. Book SC-100 exam ≈ 14 weeks out  
3. Block two × 2 h + one × 1 h slots weekly for project work

Complete the sprint and you’ll have four public, SC-100-aligned projects plus fresh résumé bullets ready for Cybersecurity-Architect interviews.
