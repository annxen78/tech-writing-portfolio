# Documentation System from Scratch

## The Challenge

When I joined the team, iBox — a SaaS ERP product — had no documentation at all. Business logic, workflows, and system rules existed only in the heads of stakeholders: the CTO, product owner, and support team. New employees had no reference material. Clients had no self-service option. Every question went directly to people.

The support load was high, onboarding was slow, and institutional knowledge was fragile.

## What I Did

### Built the content system from zero

I started by mapping what documentation the product actually needed. Using the **Diátaxis framework** as a foundation, I structured content into four types: learning materials, how-to guides, reference documentation, and problem-solving resources.

From this I built a full content tree covering:

- Step-by-step instructions for daily workflows
- Onboarding guides for new users
- Role-specific materials for business owners, department heads, and partners
- A glossary of product terminology
- FAQ and case-based problem-solving articles

### Extracted knowledge from stakeholders

The hardest part was not writing — it was capturing. Business processes, system logic, and edge cases lived in people's heads. I worked closely with the CTO, product owner, and support team to surface that knowledge and turn it into structured, reusable documentation.

### Established documentation standards

To make the system scalable and consistent, I wrote a style guide and editorial policy covering tone, structure, formatting rules, and content types. This ensured that anyone contributing to the knowledge base would follow the same standards.

The knowledge base was built in Wiki.js and later the team explored migration to Docusaurus for better versioning and developer-friendly workflows.

### Contributed to the onboarding system

Toward the end of the project, I collaborated with the product team and CTO on a broader onboarding initiative. The goal was to reduce Time-to-Value — the time it takes a new client to complete their first meaningful action in the system.

Together we designed:

- A **first-setup wizard** to replace manual configuration by the support team
- **Segmented onboarding flows** by business type (retail, wholesale, production)
- **In-product tooltips and guided tours** using UserGuiding — no engineering required
- An **onboarding analytics framework** to track where users drop off

## Results

- 50+ articles published covering core workflows, roles, and business processes — in under 9 months (April to December)
- New employees began using the knowledge base independently from day one
- Clients started self-serving common questions instead of contacting support
- The marketing team launched a GPT-powered assistant trained on the wiki content, further reducing the support load without additional documentation effort
- Institutional knowledge moved out of people's heads and into a structured, searchable system
