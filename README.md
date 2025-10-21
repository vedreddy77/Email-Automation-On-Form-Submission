# n8n Form → Budget-Based Email Router

This repository contains an **n8n** workflow that:
- Collects inputs from a form (name, email, timeline for project, **budget** choice, project details, etc.)
- **Routes** submissions by budget tier (Low / Medium / High)
- **Sends a tailored email** to your Gmail inbox for each tier with a brief summary of all form fields
- **Auto-labels** the email in Gmail as `low budget`, `medium budget`, or `high budget`

> Perfect for quickly triaging inbound leads and prioritizing follow-ups.

---

## ✨ Highlights

- **One form, three outcomes**: Different subject lines and email bodies per budget range  
- **Gmail labeling**: Automatic labels help you filter and prioritize  
- **Portable**: Exported as JSON—import to any n8n instance in seconds  
- **Secrets-safe**: No API keys or decrypted credentials are committed

---

## 🧩 Nodes & Flow (at a glance)

1. **Form Trigger** (or Webhook + external form)  
2. **IF / Switch** node on `budget` field (`low` | `medium` | `high`)  
3. **Set / Function** nodes build an email summary from all form fields  
4. **Gmail** nodes:
   - **Send** email to your inbox with budget-specific template
   - **Modify Labels** to add `low budget`, `medium budget`, or `high budget`

---

