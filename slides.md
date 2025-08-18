---
marp: true
theme: product-docs
math: katex
paginate: true
size: 16:9
headingDivider: 2
footer: "© 2025 · 24f2000935@ds.study.iitm.ac.in · $current / $total"
description: "Product documentation presentation (Marp) with custom theme, pagination, background image, directives, and math."
---

<!--
  Custom theme lives inlined below so it's fully versionable in one file.
  You can also extract it to theme CSS and load via marp-cli (--theme).
-->
<style>
/* @theme product-docs */
@import "uncover"; /* base built-in theme for nice defaults */

:root {
  --color-bg: #0b132b;
  --color-fg: #e0e6f5;
  --color-accent: #5bc0be;
  --color-muted: #cdd4f1;
  --font-sans: Inter, ui-sans-serif, system-ui, -apple-system, Segoe UI, Roboto, "Helvetica Neue", Arial, "Noto Sans", "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol", "Noto Color Emoji";
}

section {
  font-family: var(--font-sans);
  color: var(--color-fg);
  background: var(--color-bg);
  letter-spacing: 0.1px;
}

h1, h2, h3 {
  color: var(--color-fg);
}

a, strong, em, code {
  color: var(--color-accent);
}

section.lead h1 {
  font-size: 1.9em;
  line-height: 1.1;
}

pre code {
  font-size: 0.9em;
  line-height: 1.45;
}

/* Utility classes */
section.compact p { margin: 0.25rem 0; }
.badge {
  display: inline-block; padding: 0.25rem 0.5rem; border-radius: 0.5rem;
  border: 1px solid var(--color-accent); color: var(--color-accent); font-weight: 600;
}
.kicker { text-transform: uppercase; letter-spacing: 0.2em; opacity: 0.75; font-size: 0.7em; }

/* Background overlay helper (for bg image slides) */
.overlay {
  background: rgba(11,19,43,0.50);
  padding: 1.25rem;
  border-radius: 0.75rem;
  backdrop-filter: blur(2px);
}

/* Footer pagination (enabled via front-matter paginate: true) is handled by Marp */
</style>

<!-- _class: lead -->
# Product Documentation with Marp  
### Maintainable, Portable, and Pretty

**Author:** 24f2000935@ds.study.iitm.ac.in  
<span class="badge">Marp • Git • PDF/HTML/PPTX</span>

---

## Why Marp for Product Docs?

- Store slides as plain **Markdown** → easy code review & version control  
- Convert to **PDF/HTML/PPTX** with a single CLI  
- **Custom themes** + **directives** = consistent branding  
- **Math** (KaTeX) for algorithms/specs  
- Reusable **partials** and fenced code blocks

> Tip: Keep `slides.md` as the source of truth; generate artifacts in `dist/`.

---

## Conventions

- **One topic per slide** (aim for ~6–8 bullets max)
- Use `<!-- _class: compact -->` to tighten spacing where needed
- Keep examples **runnable** and **linted**
- Document **inputs, outputs, constraints**, and **complexity**

```bash
# Project structure
docs/
  slides.md
  assets/
    bg-docs.jpg
    logo.svg
dist/  # generated
