# Design System Document: High-End Editorial Strategy

## 1. Overview & Creative North Star: "The Fluid Architect"

This design system is built to transcend the standard enterprise grid. Our Creative North Star is **"The Fluid Architect."** Much like water itself, the UI should feel structured yet adaptive, authoritative yet clear. We move away from "boxed-in" dashboard tropes, instead utilizing a high-end editorial layout that prioritizes breathing room, intentional asymmetry, and sophisticated layering.

The goal is to communicate "Water Security" not through rigid lines, but through tonal depth and a sense of "digital flow." By utilizing overlapping elements and a dramatic typography scale, we establish a signature visual identity that feels custom-tailored for technical experts and community leaders alike.

---

## 2. Colors: Tonal Depth & The "No-Line" Rule

The palette is anchored in deep, professional blues and crystalline sky tones, supported by a clean, neutral foundation.

### Core Palette (Material Design Convention)
*   **Primary:** `#004f93` (Deep Professional Blue) – Used for core brand moments and primary actions.
*   **Secondary:** `#006781` (Sky Blue Variant) – Used for accents, illustrative callouts, and secondary indicators.
*   **Surface:** `#f7f9fb` (Digital Clean Water) – The standard canvas for all views.
*   **On-Surface:** `#191c1e` – Our primary ink for maximum readability.

### The "No-Line" Rule
To achieve a premium, modern feel, **1px solid borders are strictly prohibited for sectioning.** We define boundaries through background color shifts.
*   **Sectioning:** Use `surface-container-low` (`#f2f4f6`) sections against the main `surface` (`#f7f9fb`) to separate content areas.
*   **Nesting:** Place `surface-container-lowest` (`#ffffff`) cards within a `surface-container` (`#eceef0`) block to create a soft, natural separation.

### The "Glass & Gradient" Rule
Standard flat colors can feel "static." To inject "soul":
*   **Signature Textures:** Use subtle linear gradients for Hero sections, transitioning from `primary` (`#004f93`) to `primary_container` (`#1d67b5`).
*   **Glassmorphism:** For floating navigation or modal overlays, use `surface` colors at 80% opacity with a `24px` backdrop-blur. This ensures the "water" aesthetic remains cohesive, allowing background colors to bleed through softly.

---

## 3. Typography: Editorial Authority

We use a dual-font strategy to balance technical precision with modern accessibility.

*   **Display & Headlines (Manrope):** A geometric sans-serif that feels architectural.
    *   **Display-LG (3.5rem):** Used for high-impact hero statements.
    *   **Headline-MD (1.75rem):** Used for primary section titles to establish clear information hierarchy.
*   **Body & Labels (Inter):** A workhorse font optimized for technical legibility.
    *   **Body-LG (1rem):** The standard for long-form community content and articles.
    *   **Label-MD (0.75rem):** Used for metadata, captions, and micro-copy.

**Editorial Tip:** Use "Negative Leading" on Display-LG titles (setting line-height to roughly 1.1x) to create a tight, professional "magazine" look.

---

## 4. Elevation & Depth: The Layering Principle

Forget drop shadows. We communicate hierarchy through **Tonal Layering**.

*   **Natural Lift:** Instead of shadows, stack surface tiers. A `surface-container-highest` element sitting on a `surface` background provides all the "lift" needed for secondary information.
*   **Ambient Shadows:** If a floating element (like a FAB or Popover) requires a shadow, it must be an "Ambient Shadow."
    *   **Specs:** `0px 16px 32px rgba(25, 28, 30, 0.06)`. The color is a tinted version of `on-surface`, not a generic gray.
*   **The "Ghost Border":** For form fields or accessibility-required containment, use `outline-variant` (`#c1c6d3`) at **20% opacity**. It should be felt, not seen.
*   **Roundedness:** All interactive containers must use a **Scale-LG (0.5rem / 8px)** radius. This "sharp but soft" approach maintains enterprise authority while remaining accessible.

---

## 5. Components

### Buttons
*   **Primary:** Solid `primary` (`#004f93`) with `on_primary` (`#ffffff`) text. No shadow; use a subtle scale-up (1.02x) on hover.
*   **Secondary:** `primary_fixed_dim` (`#a5c8ff`) background with `on_primary_fixed` (`#001c3a`) text.
*   **Tertiary/Ghost:** No background. Use `primary` text with a `surface-variant` hover state.

### Cards & Lists
*   **Rule:** Forbid divider lines. Use `1.5rem` to `2rem` of vertical white space to separate items.
*   **Layout:** Use asymmetrical padding (e.g., more padding on the leading edge) to create an editorial, rhythmic flow.

### Input Fields
*   **State:** Default state uses the "Ghost Border." Focus state uses a `2px` solid `primary` border with a `surface-tint` glow.
*   **Labels:** Use `label-md` in `on_surface_variant` (`#414751`) placed 8px above the field.

### App-Specific Components
*   **The "Stream" Indicator:** A custom progress component using a wavy SVG path (referencing the "Three-Stream" content strategy) to indicate audio or reading progress.
*   **Data Ripples:** For iconography and data visualization, use concentric circles with decreasing opacity to represent "Impact" or "Reach."

---

## 6. Do’s and Don’ts

### Do:
*   **DO** use whitespace as a functional tool. If a layout feels crowded, increase the margin rather than adding a border.
*   **DO** overlap elements. Let an image from a "Phase" card slightly bleed over into the background of the next section to create "Flow."
*   **DO** use high-contrast typography scales. A small `label-sm` next to a large `headline-lg` creates professional tension.

### Don’t:
*   **DON'T** use 100% black. Use `on_surface` (`#191c1e`) to keep the "digital water" feel soft.
*   **DON'T** use standard "drop shadows." They feel dated and "out-of-the-box."
*   **DON'T** use default "grid" layouts for everything. Occasionally break the alignment of a sub-headline to the left or right to keep the eye moving.
*   **DON'T** use harsh, high-contrast dividers. Let the background color do the work.