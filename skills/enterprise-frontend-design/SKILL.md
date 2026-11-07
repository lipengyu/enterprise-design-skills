---
name: enterprise-frontend-design
description: Design, implement, review, or refactor enterprise-grade frontend pages using a consistent design system. Use for admin consoles, financial applications, data governance platforms, rule engines, analytics dashboards, and enterprise AI/agent workspaces. Enforces shared design tokens, business-oriented information architecture, accessible interaction states, financial data presentation, and reusable UI components.
---

# Enterprise Frontend Design

Use this skill whenever the user asks to create, redesign, implement, review, or standardize an enterprise application frontend.

## Required workflow

1. Inspect the project before changing files:
   - Identify framework, router, styling method, UI component library, chart library, existing design tokens, and current page patterns.
   - Find and read the project's `DESIGN.md`, `AGENTS.md`, and relevant theme/component references if present.
   - Do not replace an existing design system without an explicit request.
2. Select a business theme:
   - `enterprise`: general administration and business management.
   - `financial`: IFRS17, management accounting, accounting subjects, budgeting, financial reporting.
   - `analytics`: data governance, data assets, metrics, BI and analytics.
   - `ai-workspace`: agents, models, tools, skills, workflows and execution monitoring.
   - `developer`: rule engines, API consoles, developer portals and operations tools.
3. Define the page structure before implementation:
   - Identify user role, primary task, key data, main action, secondary actions, permissions, and exceptional states.
   - Prefer established enterprise patterns over decorative layouts.
   - For complex pages, briefly present the proposed information architecture before making broad changes.
4. Implement using existing project conventions:
   - Reuse the existing component library and shared components.
   - Map project components to the design tokens in `references/design-tokens.css`.
   - Avoid introducing another UI library or parallel styling system.
   - Keep business logic and authoritative calculations on the backend.
5. Validate the result:
   - Check loading, empty, error, no-permission, and partial-data states where applicable.
   - Check keyboard focus, labels, contrast, responsive behavior and consistent formatting.
   - Check desktop layout at 1280px or wider.
   - Run the project's available lint, typecheck, tests and build commands when practical.

## Design direction

Use this combination as the default:
- IBM Carbon: information hierarchy and data-dense enterprise layouts.
- Ant Design: mature enterprise component and interaction patterns.
- Linear: restrained visual language and efficient interaction.
- Stripe: financial data readability and metric presentation.

The result should feel professional, calm, precise, and operationally efficient. Do not imitate any brand pixel-for-pixel.

## Non-negotiable rules

- Treat the project's `DESIGN.md` as the visual source of truth when it exists.
- Do not invent colors, font scales, spacing, radii, shadows, or component states without checking existing tokens.
- Prefer neutral surfaces, clear hierarchy, restrained borders, and purposeful whitespace.
- Avoid gratuitous gradients, glassmorphism, oversized rounded cards, decorative animations, and emoji as business icons.
- Do not put every element inside a card.
- Tables must prioritize scanability, filtering, sorting, pagination, alignment, and useful row actions.
- Right-align numeric and monetary values; keep date, currency, percentage, negative-number, and null formatting consistent.
- Never calculate authoritative premiums, cash values, commissions, allocations, or IFRS17 results in the frontend.
- Show business period, reporting period, currency, data batch, calculation/rule version, and source lineage where relevant and authorized.
- High-impact actions such as publish, approve, post, enable/disable, delete, or production execution require explicit permission and confirmation.
- Frontend visibility is not authorization; backend authorization remains mandatory.
- Do not expose secrets, personal data, or sensitive tool parameters in URLs, logs, or error messages.

## Theme and component references

Read only the references relevant to the current task:
- `references/design-system.md`: global design system and layout rules.
- `references/themes/enterprise.md`
- `references/themes/financial.md`
- `references/themes/analytics.md`
- `references/themes/ai-workspace.md`
- `references/themes/developer.md`
- `references/components/tables.md`
- `references/components/forms.md`
- `references/components/navigation.md`
- `references/components/dashboards.md`
- `references/components/workflows.md`
- `references/components/ai-components.md`
- `references/design-tokens.css`

## Expected output

For implementation tasks:
1. State the selected theme and the reason in one sentence.
2. Implement the requested page or component in the project's existing architecture.
3. Summarize changed files and important interaction/state coverage.
4. Report checks actually run; never claim tests passed if they were not run.

For review tasks:
- List concrete design inconsistencies, usability issues, accessibility gaps, and missing states.
- Prioritize issues by severity and point to the affected files/components.
- Do not rewrite the entire UI unless requested.
