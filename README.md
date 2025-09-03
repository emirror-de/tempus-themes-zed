# Tempus Themes (16 Variants) Adapted for Zed

Adaptations of all sixteen **Tempus Themes** variants by [Protesilaos Stavrou](https://protesilaos.com) (original Vim color schemes), packaged for the **Zed** editor: **Fugit, Dusk, Autumn, Classic, Dawn, Day, Future, Night, Past, Rift, Spring, Summer, Tempest, Totus, Warp, Winter**.

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

Supported variants (light and dark mixed as in upstream collection):
`Tempus Fugit`, `Tempus Dusk`, `Tempus Autumn`, `Tempus Classic`, `Tempus Dawn`, `Tempus Day`, `Tempus Future`, `Tempus Night`, `Tempus Past`, `Tempus Rift`, `Tempus Spring`, `Tempus Summer`, `Tempus Tempest`, `Tempus Totus`, `Tempus Warp`, `Tempus Winter`

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
- Adjust palette in `themes/tempus.json`
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
