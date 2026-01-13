# Attor Branding Usage Guidelines

> **Official brand asset usage rules for documentation, product surfaces, and marketing materials**
> **Last Updated**: November 15, 2025

This document defines the rules for how Attor brand assets must be used across all project documentation, product surfaces, and marketing materials.

**Intended for**:
- Automated doc-organization steps (e.g., Claude restructuring the repo)
- Human contributors who need to reference branding rules
- Marketing and design teams
- External partners and integrators

---

## Table of Contents

1. [Logo Variants](#logo-variants)
2. [Marketing Headline](#marketing-headline)
3. [Placement Rules by Context](#placement-rules-by-context)
4. [Summary Table](#summary-table)

---

## Logo Variants

Attor has four official presentation modes:

### 1.1 Logo Only (Icon)

**Description**: Icon/symbol without text

**Use when**: Space is small, square, or when Attor is already visually established

**Use for**:
- ✅ Favicon
- ✅ Browser tab icon
- ✅ App icon / PWA icon
- ✅ Sidebar icon in the web UI
- ✅ CLI output banners
- ✅ Docker images and labels
- ✅ GitHub org avatar
- ✅ OAuth / Authentik provider icon
- ✅ Internal dashboards where the brand is already known

**Do NOT use for**:
- ❌ README header
- ❌ Landing page hero
- ❌ First-time brand introductions

---

### 1.2 Logo + Attor (Horizontal Lockup)

**Description**: Icon with "Attor" wordmark to the right

**Status**: **Primary logo - use by default**

**Use for**:
- ✅ README header
- ✅ Website navbar
- ✅ Documentation navbar
- ✅ OpenAPI docs header
- ✅ Emails and release notes
- ✅ Integrator documentation

**Avoid**:
- ❌ Very narrow/tall layouts
- ❌ Favicons or small icons

---

### 1.3 Logo Above Attor (Stacked Lockup)

**Description**: Icon with "Attor" wordmark below

**Use when**: Design layout is vertical or centered

**Use for**:
- ✅ Landing page hero section (mobile and desktop)
- ✅ Login/authentication screens
- ✅ Splash/loading screens
- ✅ Slide decks
- ✅ Stationery/letterheads

**Avoid**:
- ❌ Navbars
- ❌ Footers
- ❌ Compact UI elements

---

### 1.4 Attor + Tagline ("intelligent agents")

**Description**: Logo with descriptive tagline

**Purpose**: Clarify what Attor is (only when needed)

**Use for**:
- ✅ README introductory block
- ✅ Website home hero
- ✅ Press/media kits
- ✅ Marketing slides
- ✅ Product onboarding screens

**Do NOT use**:
- ❌ In navigation bars
- ❌ Within product UI pages
- ❌ As a favicon or icon
- ❌ In OpenAPI specs
- ❌ In CLI output

---

## Marketing Headline

### "Where systems talk."

**Type**: Marketing headline (NOT a tagline, NOT part of the logo)

**Use for**:
- ✅ Website landing hero
- ✅ README intro paragraph
- ✅ Marketing sections/pages
- ✅ Ads and promo materials
- ✅ Pitch decks

**Do NOT use**:
- ❌ In navbars or footers
- ❌ As part of a lockup
- ❌ In OpenAPI docs or technical documentation
- ❌ In favicons or icons

---

## Placement Rules by Context

### 3.1 Main README.md

```markdown
# [Horizontal Lockup: Logo + Attor]

**intelligent agents** ← Tagline

Where systems talk. ← Marketing headline

[Rest of content...]
```

**Rules**:
- **Top**: Horizontal lockup (Logo + Attor)
- **Under it**: Tagline ("intelligent agents")
- **Intro paragraph**: "Where systems talk."
- **Never** use icon-only at top

---

### 3.2 Website Root (/)

**Navbar**:
- Horizontal lockup

**Hero (desktop)**:
- Stacked lockup
- Tagline
- Marketing headline

**Hero (mobile)**:
- Stacked lockup
- Tagline

**Body sections**:
- Icon-only for visuals

---

### 3.3 Website /agents

**Context**: Functional page — not marketing

**Navbar**:
- Horizontal lockup

**Section markers**:
- Icon-only

**Exclusions**:
- ❌ No tagline
- ❌ No marketing headline

---

### 3.4 Favicon

**Format**: Always icon-only

**Sizes required**:
- 16×16 (browser tab)
- 32×32 (browser tab retina)
- 180×180 (Apple touch icon)

---

### 3.5 Other Website Paths

**Paths**: `/dashboard`, `/docs`, tenant UI

**Navbar**:
- Horizontal lockup

**Content**:
- Icon-only when needed as visual markers

**Exclusions**:
- ❌ No tagline
- ❌ No marketing headline

---

### 3.6 OpenAPI Documentation

**Header**:
- Horizontal lockup

**Favicon**:
- Icon-only

**Exclusions**:
- ❌ No tagline
- ❌ No marketing phrases

---

## Summary Table

| Surface | Logo-Only | Horizontal | Stacked | Tagline | Headline |
|---------|-----------|------------|---------|---------|----------|
| **README.md** | ❌ | ✅ | ❌ | ✅ | ✅ |
| **Website Navbar** | ❌ | ✅ | ❌ | ❌ | ❌ |
| **Website Hero** | ❌ | ❌ | ✅ | ✅ | ✅ |
| **/agents Page** | ⭑ small icons | ✅ | ❌ | ❌ | ❌ |
| **Favicon** | ✅ | ❌ | ❌ | ❌ | ❌ |
| **Dashboard UI** | ⭑ small icons | ✅ | ❌ | ❌ | ❌ |
| **OpenAPI Docs** | favicon only | ✅ header | ❌ | ❌ | ❌ |
| **Login/Splash** | ❌ | ❌ | ✅ | ✅ | ❌ |
| **CLI Output** | ✅ banner | ❌ | ❌ | ❌ | ❌ |
| **Docker Images** | ✅ label | ❌ | ❌ | ❌ | ❌ |
| **Email/Releases** | ❌ | ✅ | ❌ | optional | ❌ |

**Legend**:
- ✅ = Use this variant
- ❌ = Do not use
- ⭑ = Use sparingly for visual markers

---

## Quick Decision Tree

```
Do you have plenty of horizontal space?
├─ YES → Horizontal lockup
└─ NO
    └─ Is it a hero/splash/centered layout?
        ├─ YES → Stacked lockup
        └─ NO
            └─ Is space very small (< 50px)?
                ├─ YES → Icon only
                └─ NO → Horizontal lockup

Is this the first time someone sees Attor?
├─ YES → Add tagline
└─ NO → No tagline

Is this a marketing surface?
├─ YES → Add "Where systems talk."
└─ NO → No marketing headline
```

---

## Asset Inventory

**Expected files in `docs/branding/`**:

```
docs/branding/
├── guidelines.md          ← This file
├── logo-icon.svg          ← Icon/symbol
├── logo-horizontal.svg    ← Logo + Attor (horizontal)
├── logo-stacked.svg       ← Logo + Attor (stacked)
├── logo-with-tagline.svg  ← Logo + "intelligent agents"
├── favicon-16x16.png
├── favicon-32x32.png
├── favicon-180x180.png
└── README.md              ← Quick reference for this directory
```

---

## Related Documentation

- [Architecture Overview](../architecture.md) - System design
- [Product Overview](../overview.md) - Market positioning
- [AI Bootstrap Guide](../ai_bootstrap.md) - Documentation index

---

**Maintained by**: Attor Agents Brand Team
**Repository**: https://github.com/flengure/attor
**Last Updated**: November 15, 2025
