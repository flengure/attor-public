# Attor Branding Assets

> **Official Attor brand assets and usage guidelines**
> **Last Updated**: November 15, 2025

This directory contains all official Attor brand assets including logos, icons, and usage guidelines.

---

## Quick Start

**For most use cases**: Use `logo-icon.svg` (primary geometric diamond icon)

**Read first**: [`guidelines.md`](./guidelines.md) - Comprehensive usage rules

---

## Asset Inventory

### Current Assets

| File | Description | Use Case |
|------|-------------|----------|
| `logo-icon.svg` | Primary geometric diamond icon | Favicons, icons, compact spaces |
| `guidelines.md` | **Comprehensive usage guidelines** | **READ THIS FIRST** |
| `README.md` | This file - quick reference | Directory overview |

### Missing Assets (To Be Created)

According to `guidelines.md`, these assets are expected:

| File | Description | Priority | Notes |
|------|-------------|----------|-------|
| `logo-horizontal.svg` | Logo + "Attor" wordmark (horizontal) | **HIGH** | Primary logo variant |
| `logo-stacked.svg` | Logo + "Attor" wordmark (stacked) | **HIGH** | For hero sections, login screens |
| `logo-with-tagline.svg` | Logo + "Attor" + "intelligent agents" | **MEDIUM** | For marketing materials |
| `favicon-16x16.png` | 16×16 favicon | **HIGH** | Browser tabs |
| `favicon-32x32.png` | 32×32 favicon | **HIGH** | Browser tabs (retina) |
| `favicon-180x180.png` | 180×180 Apple touch icon | **MEDIUM** | iOS home screen |

---

## Current Logo Usage

### Web Application

**Location**: `web/logo-attor.svg`

**Used in**:
- `web/src/components/layout.rs` - Navbar (desktop and mobile)
- `web/src/pages/auth.rs` - Login and signup pages
- `web/Trunk.toml` - Build configuration (copies to dist/)

**Note**: The web app has its own copy in `web/` directory for the build process. Do not move or delete it.

---

## Logo Variants Explained

### Primary Icon (logo-icon.svg)

**Design**: Geometric diamond with orange and blue rectangles rotated 45°

**Colors**:
- Orange: `#F37A1F`
- Blue: `#0B2D52`

**Dimensions**: 260×260 viewBox

**Usage**: See `guidelines.md` § 1.1 Logo Only (Icon)

---

## Creating Missing Assets

### To create horizontal lockup:

1. Take `logo-icon.svg` (geometric diamond)
2. Add "Attor" wordmark to the right
3. Save as `logo-horizontal.svg`
4. Use font: [TBD - define brand font]
5. Spacing: [TBD - define spacing rules]

### To create stacked lockup:

1. Take `logo-icon.svg` (geometric diamond)
2. Add "Attor" wordmark below
3. Center-align both elements
4. Save as `logo-stacked.svg`

### To create favicons:

```bash
# From logo-icon.svg
convert logo-icon.svg -resize 16x16 favicon-16x16.png
convert logo-icon.svg -resize 32x32 favicon-32x32.png
convert logo-icon.svg -resize 180x180 favicon-180x180.png
```

---

## Usage Guidelines Summary

**Read the full guidelines**: [`guidelines.md`](./guidelines.md)

### Quick Rules

1. **Horizontal lockup** = Primary logo (use by default)
2. **Stacked lockup** = Hero sections, login screens, splash screens
3. **Icon-only** = Favicons, small spaces, when brand is established
4. **Tagline** = Only when clarifying what Attor is
5. **Marketing headline** = Only on marketing surfaces, never in product UI

### Context-Specific

| Surface | Variant | Tagline | Headline |
|---------|---------|---------|----------|
| README.md | Horizontal | ✅ | ✅ |
| Website navbar | Horizontal | ❌ | ❌ |
| Website hero | Stacked | ✅ | ✅ |
| OpenAPI docs | Horizontal | ❌ | ❌ |
| Favicon | Icon-only | ❌ | ❌ |

---

## Brand Colors

### Primary Colors

```css
/* Orange (primary) */
--attor-orange: #F37A1F;

/* Blue (secondary) */
--attor-blue: #0B2D52;
```

### Alternative Orange Shades

```css
/* Lighter orange (alternative icon) */
--attor-orange-light: #F97316;

/* Darker orange (alternative icon) */
--attor-orange-dark: #EA580C;
```

---

## Related Documentation

- [`guidelines.md`](./guidelines.md) - **Comprehensive usage guidelines**
- [`../overview.md`](../overview.md) - Product vision and positioning
- [`../design.md`](../design.md) - Design patterns and decisions

---

## Contributing

### Adding New Assets

1. **Read `guidelines.md` first** - Understand usage rules
2. **Follow naming convention**: `logo-{variant}.{ext}` (e.g., `logo-horizontal.svg`)
3. **Use brand colors**: Orange `#F37A1F`, Blue `#0B2D52`
4. **Provide multiple formats**: SVG (primary), PNG (raster fallback)
5. **Update this README**: Add new asset to inventory table
6. **Commit with description**: Explain what the asset is and when to use it

### Updating Existing Assets

1. **Check usage first**: Run `grep -r "filename" /home/user/attor/`
2. **Update all references**: Web app, documentation, build configs
3. **Test build process**: Ensure `trunk build` still works
4. **Update this README**: Document any changes
5. **Commit with explanation**: Describe what changed and why

---

## Notes

- **Web app copy**: `web/logo-attor.svg` must remain for build process (referenced in `web/Trunk.toml`)
- **Documentation copies**: This directory (`docs/branding/`) is the canonical source for brand assets
- **Missing assets**: See "Missing Assets" table above for priority creation list
- **Brand font**: To be defined (currently not specified)
- **Spacing rules**: To be defined for lockup variants

---

**Maintained by**: Attor Agents Brand Team
**Repository**: https://github.com/flengure/attor
**Last Updated**: November 15, 2025
