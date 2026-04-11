---
name: ui-ux-pro-max
description: "UI/UX design intelligence for web and mobile. Includes 67 styles, 161 color palettes, 57 font pairings, 161 product types, 99 UX guidelines, and 25 chart types across 16 stacks (React, Next.js, Vue, Svelte, SwiftUI, React Native, Flutter, Tailwind, shadcn/ui, HTML/CSS, Angular, Laravel). Actions: plan, build, create, design, implement, review, fix, improve, optimize, enhance, refactor, and check UI/UX code. Elements: button, modal, navbar, sidebar, card, table, form, chart. Styles: glassmorphism, claymorphism, minimalism, brutalism, neumorphism, bento grid, dark mode, responsive, skeuomorphism, flat design."
---

<purpose>
Provide design intelligence for building professional UI/UX across web and mobile platforms.
Use the search script and data files at .github/prompts/ui-ux-pro-max/ for live recommendations.
</purpose>

<skill_files>
Main prompt:    .github/prompts/ui-ux-pro-max/PROMPT.md
Search script:  .github/prompts/ui-ux-pro-max/scripts/search.py
Data files:     .github/prompts/ui-ux-pro-max/data/
</skill_files>

<when_to_apply>

**Must Use:**
- Designing new pages (Landing Page, Dashboard, Admin, SaaS, Mobile App)
- Creating or refactoring UI components (buttons, modals, forms, tables, charts)
- Choosing color schemes, typography systems, spacing standards, or layout systems
- Reviewing UI code for user experience, accessibility, or visual consistency
- Implementing navigation structures, animations, or responsive behavior
- Making product-level design decisions (style, information hierarchy, brand expression)
- Improving perceived quality, clarity, or usability of interfaces

**Skip:**
- Pure backend logic, API/database design, infrastructure, or non-visual scripts

</when_to_apply>

<workflow>

## Step 1: Analyze User Requirements

Extract key information:
- **Product type**: SaaS, e-commerce, portfolio, healthcare, beauty, fintech, service, etc.
- **Target audience**: Age group, usage context (commute, leisure, work)
- **Style keywords**: playful, vibrant, minimal, dark mode, content-first, immersive, etc.
- **Stack**: React, Next.js, Vue, Svelte, SwiftUI, React Native, Flutter, HTML+Tailwind, etc.

## Step 2: Generate Design System (REQUIRED)

```bash
python3 .github/prompts/ui-ux-pro-max/scripts/search.py "<product_type> <industry> <keywords>" --design-system [-p "Project Name"]
```

**Example:**
```bash
python3 .github/prompts/ui-ux-pro-max/scripts/search.py "beauty spa wellness" --design-system -p "Serenity Spa"
```

## Step 3: Domain-Specific Searches

```bash
python3 .github/prompts/ui-ux-pro-max/scripts/search.py "<keyword>" --domain <domain>
```

| Domain | Use For |
|--------|---------|
| `product` | Product type patterns |
| `style` | UI styles (glassmorphism, brutalism, etc.) |
| `color` | Color palettes by industry |
| `typography` | Font pairing recommendations |
| `chart` | Chart type recommendations |
| `ux` | UX best practices and anti-patterns |
| `landing` | Page structure and CTA strategies |

## Step 4: Stack-Specific Guidelines

```bash
python3 .github/prompts/ui-ux-pro-max/scripts/search.py "<keyword>" --stack <stack>
```

Stacks: `react`, `next`, `vue`, `nuxt`, `svelte`, `astro`, `html-tailwind`, `shadcn`, `swiftui`, `jetpack`, `react-native`, `flutter`, `angular`, `laravel`

</workflow>

<rule_priority>

| Priority | Category | Impact |
|----------|----------|--------|
| 1 | Accessibility | CRITICAL — contrast 4.5:1, alt text, keyboard nav, aria-labels |
| 2 | Touch & Interaction | CRITICAL — min 44×44px targets, 8px spacing, loading feedback |
| 3 | Performance | HIGH — WebP/AVIF, lazy load, CLS < 0.1 |
| 4 | Style Selection | HIGH — match product type, SVG icons (no emoji) |
| 5 | Layout & Responsive | HIGH — mobile-first, no horizontal scroll |
| 6 | Typography & Color | MEDIUM — base 16px, line-height 1.5, semantic tokens |
| 7 | Animation | MEDIUM — 150–300ms duration, prefers-reduced-motion respect |
| 8 | Forms & Feedback | MEDIUM — visible labels, error near field |
| 9 | Navigation Patterns | HIGH — predictable back, bottom nav ≤5 |
| 10 | Charts & Data | LOW — legends, tooltips, accessible color pairs |

</rule_priority>

<pre_delivery_checklist>

- [ ] No emojis used as icons (use SVG: Heroicons, Lucide, Phosphor)
- [ ] Touch targets ≥ 44×44pt (iOS) / 48×48dp (Android)
- [ ] Primary text contrast ≥ 4.5:1 in both light and dark mode
- [ ] Micro-animation timing 150–300ms with native-feeling easing
- [ ] Mobile tested at 375px viewport width
- [ ] Safe areas respected for headers, tab bars, and bottom CTA bars
- [ ] Scroll content not hidden behind fixed/sticky bars
- [ ] Reduced motion supported (prefers-reduced-motion)
- [ ] Semantic color tokens used (no hardcoded hex in components)
- [ ] Form fields have visible labels, hints, and clear error messages

</pre_delivery_checklist>

Source: https://github.com/nextlevelbuilder/ui-ux-pro-max-skill (v2.5.0 · MIT)
