<!--
 Source         : ChatGPT (GPT-4o)
 Date generated : 2025-07-07
 Title          : Do the Suggested Projects Align with Microsoft Learn?
 License        : © 2025 sking-dev.  Generated with assistance of OpenAI.
-->

# 📚 Do the Suggested SC-100 Projects Align with Microsoft Learn?

Yes. Every project in the SC-100 roadmap maps directly to at least one official Microsoft Learn module or learning path.  
The table below shows the alignment and highlights any areas where you’ll need supplemental (non-Learn) resources.

| Project | SC-100 Exam Domain | Core Microsoft Learn Content | Supplemental Resources |
|---------|--------------------|------------------------------|------------------------|
| **A – Zero-Trust Landing Zone** | 1 - Design a Zero-Trust strategy (25 %) | - Design a zero-trust network for Azure<br>- Plan and deploy landing zones | - Azure Well-Architected Framework – Security pillar<br>- Terraform CAF Enterprise-Scale repo |
| **B – Policy-as-Code & Secure-Score Uplift** | 2 - Evaluate governance & compliance (20 %) | - Implement Azure Policy to manage resources<br>- Monitor and improve Secure Score<br>- Design a governance solution on Azure | - tfsec docs + sample pipelines<br>- CAF landing-zone policy sets (GitHub) |
| **C – AKS + Gatekeeper + Signed SBOM** | 3 - Design infrastructure security (35 %) | - Secure Kubernetes services on Azure (RBAC, KMS, Defender)<br>- Enforce organisational standards with Gatekeeper | - Gatekeeper Rego library (OSS)<br>- Syft & Cosign docs for SBOM signing<br>- Trivy “Kubernetes & SBOM” tutorials |
| **D – Sentinel + GPT-4o Incident "Triager"** | 4 - Design security operations (20 %) | - Automate response with Sentinel playbooks (Logic Apps)<br>- Design a threat-protection strategy with Microsoft Sentinel | - Azure OpenAI function-calling docs<br>- MITRE ATT&CK mapping in Sentinel labs<br>- Cost-management blog for OpenAI tokens |

---

## What Microsoft Learn Already Covers

* Zero-Trust principles, Conditional Access, Private Link, Firewall  
* Azure Policy creation/assignment, Secure Score improvement  
* AKS security hardening, Gatekeeper deployment, Defender for Containers  
* Sentinel analytics rules, Logic Apps playbooks, incident workflows  

## What Requires External Docs or Blogs

| Topic | Why |
|-------|-----|
| **SBOM generation & Cosign signatures** | Not yet covered in Microsoft Learn. |
| **GPT-4o incident summarisation** | Gen-AI + Sentinel integration is too new for Learn modules. |
| **tfsec / Trivy pipeline integration** | Only referenced briefly in Learn—vendor docs give full YAML examples. |

---

## Quick “Getting-Started” Links

* SC-100 Skills Outline → <https://learn.microsoft.com/en-gb/credentials/certifications/resources/study-guides/sc-100#skills-measured-as-of-july-22-2025>
* Terraform CAF Enterprise-Scale → <https://github.com/Azure/terraform-azurerm-caf-enterprise-scale>
* Azure Policy tutorials → <https://learn.microsoft.com/azure/governance/policy/tutorials/create-and-manage>
* Gatekeeper on AKS → <https://learn.microsoft.com/azure/aks/governance-policy>
* Sentinel playbooks → <https://learn.microsoft.com/azure/sentinel/tutorial-use-playbooks>
* Syft & Cosign → <https://github.com/anchore/syft> | <https://github.com/sigstore/cosign>
* Azure OpenAI function calling → <https://learn.microsoft.com/azure/ai-services/openai/how-to/function-calling>

---

### How to Tackle Each Project Efficiently

1. **Skim the Microsoft Learn module(s)** first; take screenshots or notes to reuse in your README files
2. **Consult supplemental docs** for gaps (SBOM, GPT-4o, tfsec) 
3. **Capture commands, scripts and diagrams** in your GitHub repo as you go—these artefacts prove both SC-100 prep and portfolio value
