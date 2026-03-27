# Design System Document: The Botanical Archivist

## 1. Overview & Creative North Star
**Creative North Star: The Botanical Archivist**
This design system moves away from the sterile, rigid grids of traditional Customer Management Software. Instead, it adopts an editorial, high-end aesthetic that feels like a curated digital workspace. We are building a "Botanical Archivist"—a system that is systematically organized (professional) but feels organic and breathing (friendly). 

To achieve this, we lean into **Soft Minimalism**. We break the "template" look by using intentional asymmetry in dashboard layouts, high-contrast typography scales (pairing large Manrope headlines with functional Inter body text), and overlapping "paper-on-paper" layers. The interface should feel less like a database and more like a high-end digital journal.

---

## 2. Colors & Surface Philosophy
The palette transitions from the legacy purple to a sophisticated sage green (`primary`) and a series of muted pastels.

### The "No-Line" Rule
**Explicit Instruction:** Designers are prohibited from using 1px solid borders for sectioning or layout containment. Boundaries must be defined solely through:
- **Background Color Shifts:** Use `surface_container_low` sections sitting on a `background` (`#f7faf8`).
- **Tonal Transitions:** A side panel in `surface_container` against a main stage in `surface_bright`.

### Surface Hierarchy & Nesting
Treat the UI as a series of physical layers. Use the surface tiers to create depth without relying on shadows:
- **Level 0 (Base):** `background` (#f7faf8) or `surface`.
- **Level 1 (Sections):** `surface_container_low` (#f0f5f2).
- **Level 2 (Cards/Modules):** `surface_container_lowest` (#ffffff).
- **Level 3 (Pop-overs):** `surface_container_high` (#e2eae7) with backdrop-blur.

### The Glass & Gradient Rule
To ensure a custom, premium feel, main CTAs and "Hero" cards should utilize a subtle linear gradient from `primary` (#4c6456) to `primary_dim` (#40584a). For floating navigation or modals, use **Glassmorphism**: semi-transparent `surface_bright` with a 12px-20px backdrop blur to allow the sage tones to bleed through the background.

---

## 3. Typography
We utilize a dual-typeface system to balance personality with extreme legibility.

- **Display & Headlines (Manrope):** These are our "Editorial" voices. Use `display-lg` and `headline-md` with generous tracking (-0.02em) to create a sophisticated, authoritative presence. Headlines should drive the brand's welcoming personality.
- **Body & Labels (Inter):** Our "Functional" voice. Inter is used for all data-heavy CMS views to ensure readability. 
- **The Contrast Rule:** Pair a very large `headline-lg` (Manrope) with a small, uppercase `label-md` (Inter) in `on_surface_variant` to create a high-end magazine feel in dashboard summaries.

---

## 4. Elevation & Depth
In this design system, depth is "baked" into the surface colors, not "applied" with heavy shadows.

- **The Layering Principle:** Achieve lift by stacking. Place a `surface_container_lowest` card on a `surface_container_low` section. The slight delta in brightness creates a soft, natural lift.
- **Ambient Shadows:** Shadows are reserved only for elements that truly "float" (modals, dropdowns).
  - **Specs:** Blur: 24px–40px, Spread: -4px, Opacity: 6%–8%.
  - **Color:** Use a tinted version of `on_surface` (#2c3432) rather than pure black to keep the lighting organic.
- **The Ghost Border Fallback:** If accessibility requires a container boundary, use a "Ghost Border": `outline_variant` at **15% opacity**. Never use 100% opaque borders.

---

## 5. Components

### Buttons
- **Primary:** Filled with `primary` (#4c6456), text in `on_primary`. Corner radius: `md` (0.75rem).
- **Secondary:** Surface in `primary_container` (#cee9d6) with text in `on_primary_container`. 
- **Tertiary:** No background. Text in `primary`. Use for low-priority actions like "Cancel."

### Input Fields
- **Style:** Instead of a white box with a dark border, use `surface_container_highest` (#dbe4e2) as a solid background with no border. 
- **States:** On focus, transition the background to `surface_container_lowest` and add a 2px "Ghost Border" in `primary`.
- **Corners:** `sm` (0.25rem) for a more structured, professional feel.

### Cards & Lists
- **The Divider Ban:** Strictly forbid 1px lines between list items. Use `spacing-4` (1rem) of vertical white space or alternating backgrounds (`surface` vs `surface_container_low`).
- **Cards:** Use `xl` (1.5rem) rounded corners for "Hero" or "Highlight" cards, and `lg` (1rem) for standard data cards.

### Navigation (The Signature Component)
- **Side Nav:** Use a wide gutter (`spacing-8`) and `surface_container_low`. Active states should be indicated by a soft `primary_fixed` (#cee9d6) background pill with `lg` rounding.

---

## 6. Do's and Don'ts

### Do:
- **Embrace White Space:** Use `spacing-12` (3rem) and `spacing-16` (4rem) to separate major sections. Luxury is defined by space.
- **Use Tonal Color:** Use `on_surface_variant` (#58615f) for secondary text to maintain a soft, welcoming contrast.
- **Respect the Logo Form:** While the purple is gone, use the logo's "aperture" geometry as a subtle background watermark or as a mask for user avatars.

### Don't:
- **Don't use Purple:** All legacy purple must be replaced with the `primary` (Sage) or `tertiary` (Earth) tones.
- **Don't use Pure Black (#000):** Use `on_background` (#2c3432) for all dark text to keep the interface feeling "warm."
- **Don't use Standard Shadows:** Avoid the "drop shadow" look. If it looks like a 2010s app, the shadow is too dark and too small.
- **Don't use Default Grids:** Try offsetting cards by `spacing-4` to create an asymmetrical, editorial rhythm.