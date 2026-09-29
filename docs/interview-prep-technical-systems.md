# Interview prep · Technical Systems roles

Prepared for healthcare / enterprise payment infrastructure interviews (example target: **Technical Systems Manager** at Arrow Payments).  
Stories are grounded in real Clear Billing Services work. Public demos use synthetic data only.

**Author:** Benjamin M. Rivera · Director of Technical Operations, Clear Billing Services, Inc.

---

## Core framing

You are not "someone with tech experience." You already run technical operations for an anesthesia billing company: HIPAA and financial compliance, medical data pipelines, custom software, and client-facing reliability.

| Clear Billing work | What it signals |
|:--|:--|
| Command Center (ground up) | Full-stack ops vision, API/workflow automation, internal tooling |
| Prism Digital Intake | Secure onboarding, client/clinician portals, friction-free ingestion |
| Director of Technical Operations | Ownership, high-stakes reliability, compliance, strategic client care |
| Cursor + modern AI tooling | Fast prototype → production with review discipline |

---

## STARS model (use every time)

1. **Situation** - business context and pain  
2. **Task** - what you owned  
3. **Action** - architecture, tools, stakeholders (go deep, stay ordered)  
4. **Result** - outcome and what you would bring to their team  

---

## Story 1 · Command Center

**When:** building internal systems, automation, AI tooling, scaling ops capacity.

**Answer (long form):**

At Clear Billing Services, operational complexity outgrew off-the-shelf software. As Director of Technical Operations I designed and built **Command Center** from the ground up: a single-pane hub for vault intake, medical coding review, PM/EHR interface writeback, and Archive / Office / Audit.

I connected the workflow so humans sign off before any write, Draft only becomes Approved after the interface confirms, and exceptions (schedule gaps, holds) sit in owned queues instead of chat threads. I use AI-assisted development (Cursor) to move quickly on scripts, APIs, and UI, with compile checks and changelogs so speed never skips reliability.

The result is one operational truth for the team and leadership visibility into bottlenecks. That same approach - find manual friction, architect a custom system, ship durable automation - is what I bring to technical systems work that expands capacity and builds internal knowledge tooling.

**Demo:** https://github.com/brivera2005/command-center-demo

---

## Story 2 · Prism Digital Intake

**When:** client onboarding, payment/data security, digital switchovers, simplifying complex UX.

**Answer (long form):**

Healthcare financial ops usually onboard charge and demographic data through email and paper. I designed and shipped **Prism**: a secure clinician intake gateway with invited Access, MFA, an explicit PHI screen, then either practice-tuned Add Case entry or bulk PDF upload.

Backend integration matters as much as the form: data maps cleanly and routes into Command Center so operators never re-key from insecure channels. Demos can arrive later via MRN/DOS sync so the charge path stays unblocked.

Prism cut onboarding friction and reduced compliance exposure from email PHI. For teams helping healthcare systems move to hosted payment portals and P2PE environments, I already think in transition risk, clean data flows, and admin confidence through the switchover.

**Demo:** https://brivera2005.github.io/clinician-mobile-intake/

---

## Story 3 · High-stakes outage with EQ

**When:** client communication under pressure, EQ, incident response.

**Answer (long form):**

When a billing pipeline or upstream integration stalls, revenue and compliance anxiety spike immediately. In one Clear Billing incident, an upstream disconnect threatened daily flows.

I led with communication first: acknowledged impact, set expectation bounds, and translated API diagnostics into plain language. In parallel I isolated the break, deployed the fix, and verified data integrity. After restore I shared a transparent post-mortem and added monitoring in Command Center so the failure mode could not go silent again.

Technical excellence and care belong together. Owned incidents become trust.

---

## Questions to ask (examples)

**On internal AI and automation**

> Where do you see the biggest operational friction inside the team that an internal tool or automation pipeline could remove in months one through six?

**On healthcare and enterprise clients**

> How do you balance rigorous PCI/HIPAA standards with an effortless onboarding experience for clinic administrators?

**On growth**

> For a Technical Systems Manager who takes early ownership of systems engineering and internal automation, what does the path to senior leadership look like?

---

## Repo checklist for interviews

1. Share [healthcare-portfolio](https://github.com/brivera2005/healthcare-portfolio) as the index.  
2. Walk Prism live in the browser (2 minutes).  
3. Run or screen-share Command Center sandbox loop (Vault → Code Review → Simulate Approved → Office).  
4. Keep production secrets and real PHI offline. Always.
