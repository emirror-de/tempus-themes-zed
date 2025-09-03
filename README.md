# Tempus Fugit & Dusk (Adapted for Zed)

Adaptations of the **Tempus Fugit** (light) and **Tempus Dusk** (dark) themes from [Protesilaos Stavrou's Tempus Themes collection](https://protesilaos.com), packaged for the **Zed** editor.

These themes aim to preserve the original *balance, contrast discipline, semantic consistency,* and *reading comfort* of the Tempus series while translating them into Zed’s theming surface (UI + syntax + diagnostics + VCS + terminal colors).

---

## ✨ Highlights

- Faithful palette adaptation from the original Vim color schemes
- WCAG-conscious contrast philosophy (as in upstream Tempus Themes)
- Consistent semantic color grouping (functions, types, keywords, constants)
- Light + Dark pairing designed to reduce cognitive switching fatigue
- Subtle UI accents: avoids over-saturation in chrome vs. syntax layers
- Fully defined terminal ANSI mappings matching each variant
- Attribution and licensing aligned with upstream (GPL-3.0-or-later)

---

## 🎨 Theme Names in Zed

- Light: `Tempus Fugit`
- Dark: `Tempus Dusk`

---

## 🧩 Design Principles (Inherited from Tempus Themes)

| Principle | Application in Adaptation |
|-----------|---------------------------|
| Readability first | Medium, calm chroma values; no neon “pop” noise |
| Semantic grouping | Closely related kinds retain adjacency in hue family |
| Reduced fatigue | No extreme pure white (#ffffff) or absolute black (#000000) in text surfaces |
| Disciplined contrast | UI surfaces use restrained deltas so syntax stands out |
| Symbol role clarity | Keywords, types, functions, and constants form distinct clusters |
| Accessibility mindset | Color choices avoid ambiguous low-contrast pairings |

---

## 🔍 Syntax Mapping Overview

| Category          | Tempus Fugit (Light) | Tempus Dusk (Dark) |
|-------------------|----------------------|--------------------|
| Background        | `#fff5f3`            | `#1f252d`          |
| Foreground/Base   | `#4d595f`            | `#a2a8ba`          |
| Comments          | `#796271` (italic)   | `#a29899` (italic) |
| Keywords          | `#a234c0`            | `#c69ac6`          |
| Functions / Tags  | `#a83884`            | `#b190af`          |
| Types / Enums     | `#007072`            | `#8e9aba`          |
| Constants/Nums    | `#1666b0`            | `#8c9abe`          |
| Strings           | `#485adf`            | `#9ca5de`          |
| Special / Symbol  | `#985900`            | `#bda75a`          |
| Preprocessor      | `#b93f1a`            | `#d39d74`          |
| Diff Added        | `#357200`            | `#8ba089`          |
| Diff Removed      | `#c61a14`            | `#cb8d56`          |

The palettes were mapped to Zed’s semantic keys (e.g. `syntax.keyword`, `syntax.type`, `syntax.string`, VCS badges, diagnostics, terminal ANSI set). Only minimal adjustments were made to maintain legibility in Zed’s UI context.

---

## 🖥 Terminal ANSI Alignment

Both variants provide a cohesive terminal experience (helpful if you embed a terminal in Zed):

| Slot     | Fugit (Light) | Dusk (Dark) |
|----------|---------------|-------------|
| Black    | `#4d595f`     | `#1f252d`   |
| Red      | `#c61a14`     | `#cb8d56`   |
| Green    | `#357200`     | `#8ba089`   |
| Yellow   | `#825e00`     | `#a79c46`   |
| Blue     | `#1666b0`     | `#8c9abe`   |
| Magenta  | `#a83884`     | `#b190af`   |
| Cyan     | `#007072`     | `#8e9aba`   |
| White    | `#efe6e4`     | `#a29899`   |
| Bright counterparts follow upstream hue intent |

---

## 🚀 Installation

### Development Install (Local)

1. Clone the repository:
   git clone https://github.com/emirror-de/tempus-themes-zed.git
2. Open Zed.
3. Command Palette → “Extensions: Install Dev Extension”.
4. Select the cloned directory.

### Activation

System-based automatic switching:
```json
{
  "theme": {
    "mode": "system",
    "light": "Tempus Fugit",
    "dark": "Tempus Dusk"
  }
}
```

Force one variant:
```json
{ "theme": "Tempus Dusk" }
```
or
```json
{ "theme": "Tempus Fugit" }
```

---

## ⚙️ Optional Customization

You can gently tune contrast without breaking intent:

Example (slightly dim strings + heavier comments):
```json
{
  "overrides": {
    "syntax": {
      "string": { "color": "#4450c8" },
      "comment": { "font_style": "italic", "color": "#6f5a68" }
    }
  }
}
```

Try to avoid:
- Shifting backgrounds (will alter palette balance)
- Over-saturating UI primitives (they should stay neutral)

---

## 🤝 Contributing

Contributions welcome when they:
1. Preserve semantic cohesion
2. Avoid arbitrary chroma escalation
3. Document rationale for any change
4. Consider both light and dark simultaneously

Workflow suggestion:
- Adjust palette in `themes/tempus-themes.json`
- Test with varied filetypes (Rust, TS, Markdown, diff views)
- Validate contrast (WCAG AA for text vs. background where feasible)
- Open a PR with before/after screenshots

---

## 📜 License & Attribution

- Original palette & design logic: **Tempus Themes** by Protesilaos Stavrou
  Source: https://github.com/protesilaos/tempus-themes
  License: **GPL-3.0-or-later**
- Zed adaptation (theme JSON, structural mapping): © 2025 Lewin Probst
- This repository (combined work) is distributed under: **GPL-3.0-or-later**
  See [LICENSE](LICENSE)

SPDX: `GPL-3.0-or-later`

If you redistribute modified versions:
- Retain attribution
- Indicate modifications
- Keep licensing consistent

---

## 🔗 Upstream & References

- Tempus Themes: https://protesilaos.com
- WCAG Contrast Guidelines: https://www.w3.org/WAI/WCAG21/quickref/
- Zed Editor: https://zed.dev

---

## ❓ FAQ

**Why GPL instead of MIT now?**
Because the themes derive from GPL-licensed upstream work; relicensing under a more permissive license would not be compliant.

**Can I extract just the colors?**
Color *values* individually are not copyrightable in most jurisdictions, but the curated arrangement + mapping constitutes expressive selection. Respect upstream licensing if redistributing as a derivative theme.

**Will more Tempus variants be added?**
Potentially. Contributions that add other Tempus schemes (e.g. Tempus Night, Tempus Day) while maintaining parity are welcome.

---

## ✅ Status

Current focus:
- Validation of palette in various languages
- Gathering feedback on Zed-specific affordances (minimap, inline hints, SCM gutter)
- Optional future: dynamic variant generator script

---

**Enjoy a calm, disciplined, accessible coding atmosphere.**
Refined aesthetics without sacrificing legibility.

*Tempus fugit — time flies. Code comfortably while it does.*
