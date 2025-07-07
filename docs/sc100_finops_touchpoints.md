<!--
 Source         : ChatGPT (GPT-4o)
 Date generated : 2025-07-07
 Title          : FinOps Hooks Already Built Into SC-100 Portfolio Projects
 License        : © 2025 sking-dev. Generated with assistance of OpenAI.
-->

# 💰 FinOps Hooks in Your SC-100 Portfolio

| Portfolio Project | Core Security Goal | FinOps Angle to Implement | SC-100 / CV Benefit |
|-------------------|--------------------|---------------------------|---------------------|
| **A – Zero-Trust Landing Zone** | Segmented network, Private Link, Conditional Access | *Azure Policy* “Allowed SKU” to block premium VMs <br>- Monthly Budget + 80 % alert <br>- Terraform variables that default non-prod to Spot or B-series | Shows governance of **cost + security** (SC-100 Domain 2) |
| **B – Policy-as-Code & Secure-Score Uplift** | Automate CAF/CIS compliance | - Tag policy (`costCentre`, `env`) <br>- **Infracost** diff in PRs to expose £∆ before merge | Demonstrates **shift-left FinOps** alongside tfsec/Trivy |
| **C – AKS + Gatekeeper + Signed SBOM** | Container guard-rails & supply-chain | - Gatekeeper rule: deny node pools > 8 vCPU unless `costOverride=true` <br>- **Kubecost/OpenCost** dashboard export | Balances cluster security with spend — crucial for GPU/AI nodes |
| **D – Sentinel + GPT-4o Incident "Triager"** | AI-assisted SOC playbook | - Log GPT token usage → Log Analytics <br>- Logic App posts alert when usage > budget | Controls runaway LLM cost; merges FinOps into SecOps (Domain 4) |

---

## Concrete Artefacts to Commit

1. **Tag-coverage workbook** – “Tag compliance: 98 % of 420 resources”
2. **Infracost screenshot / GIF** – PR comment:  
   `💸 +£37/month (↑ 12 %) from Standard_D8s_v5 VM`
3. **Policy assignment JSON** – “Deny PublicIP and Non-Approved SKU”
4. **Budget ARM/Bicep** – `budget_monthly_£500.json` with email/Teams action group
5. **Kubecost report CSV** or **Cost Management** export for AKS
6. **OpenAI token spend chart** – Kusto query + Sentinel workbook

---

## Résumé Bullet Template

> “Integrated FinOps tagging, budget alerts and Infracost PR checks into a zero-trust Terraform pipeline—cut non-prod Azure spend by **≈ 15 %** while maintaining CIS compliance.”

---

Leverage these hooks and you’ll showcase a rare mix of **security, automation and cost-optimisation**—a key differentiator for both SC-100 and DevSecOps hiring managers.
