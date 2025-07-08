<!--
 Source         : ChatGPT (GPT-4o)
 Date generated : 2025-07-08
 Title          : Terraform vs Bicep for Project A — Decision Recap
 License        : © 2025 sking-dev.  Generated with assistance of OpenAI.
-->

# 🏗️ Terraform or Bicep for Project A?

| Aspect | Stick with **Terraform** | Go **Bicep-First** | Hybrid → TF MVP + Bicep Port |
|--------|-------------------------|--------------------|------------------------------|
| Delivery speed | ✅ Fast (you know TF) | ❌ Slower (new DSL) | ⚖️ Quick win then learn |
| Azure-native showcase | Good | Great | Best of both |
| SC-100 relevance | Tool-agnostic | Tool-agnostic | — |
| Recruiter optics | Terraform keyword | Bicep keyword & Azure depth | Both keywords |
| Maintenance | One IaC stack | Two stacks career-wide | Slight repo overhead |

---

```plaintext
TL;DR

Start with Terraform for speed then port a subset to Bicep when time permits, thereby gaining Azure-native IaC experience without delaying visible progress.
```

---

## Recommended Path

1. **Ship MVP in Terraform** to prove the landing zone and integrate tfsec / Infracost quickly
2. **Port key modules to Bicep** in a separate folder or branch:  
   `project-a-zero-trust-landing-zone/bicep/`  
3. Highlight dual-IaC skill on CV:  
   > “Provisioned Zero-Trust landing zone via Terraform; ported core modules to Bicep to validate Azure-native IaC.”

## Quick 4-Hour Bicep Hands-On Plan

```bash
az bicep install                                # CLI
az bicep decompile --file main.tf               # bootstrap
# Split into VNet.bicep, Firewall.bicep, etc.
az deployment sub create \
  --location uksouth \
  --template-file main.bicep \
  --parameters @main.parameters.json            # test deploy
git add project-a-zero-trust-landing-zone/bicep
```

---

## When to Skip Bicep

- Timeline is tight & Terraform delivers portfolio value faster
- Target employers are multi-cloud and Terraform-centric
- You’d rather spend the hours on AKS Gatekeeper or Sentinel GPT work
