```markdown
# Design System Document

## 1. Overview & Creative North Star: "The Digital Curator"

This design system is engineered to elevate Premiere Pro templates from a "utility tool" to a "creative essential." Moving beyond the cluttered, high-intensity layouts typical of digital assets, we embrace **The Digital Curator** as our Creative North Star. 

The Curator doesn't scream for attention; it commands it through intentionality, breathability, and an editorial precision inspired by high-end consumer technology interfaces. By utilizing dramatic scale shifts in typography, asymmetrical product staging, and a depth-model based on tonal layering rather than physical borders, we create an experience that feels as premium as the animations being sold. This is a conversion-focused mobile experience that respects the user’s intelligence and aesthetic standards.

---

## 2. Colors

Our palette is a study in restrained sophistication. We use a monochrome foundation punctuated by a singular, authoritative "Action Blue" to guide the user's eye through the conversion funnel.

### The "No-Line" Rule
**Strict Mandate:** Designers are prohibited from using 1px solid borders to define sections or containers. The "box" is a relic of the past. Instead, boundaries must be defined solely through:
- **Background Color Shifts:** Use `surface-container-low` sections against a `surface` background.
- **Tonal Transitions:** A transition from `surface` to `surface-container-highest` creates an implicit edge that feels modern and expansive.

### Surface Hierarchy & Nesting
Treat the mobile UI as a series of physical layers. We use a "Material-Scale" nesting logic:
1.  **Base Layer:** `surface` (#f9f9f9).
2.  **Section Layer:** `surface-container-low` (#f3f3f3) for secondary content.
3.  **Component Layer:** `surface-container-lowest` (#ffffff) for primary cards or input areas to provide a "lifted" feel.

### The "Glass & Gradient" Rule
To prevent the UI from feeling "flat" or "web-like," use Glassmorphism for floating navigation or sticky CTAs. Apply `surface` at 80% opacity with a `backdrop-blur` of 20px. For primary CTAs, a subtle linear gradient from `primary` (#005bc1) to `primary_dim` (#004faa) at 135 degrees adds a "jewel-like" depth that a flat fill cannot achieve.

---

## 3. Typography

The typography is the voice of the product. By using a single, high-quality sans-serif (Inter/SF Pro), we rely on weight and scale—not font variety—to create hierarchy.

-   **Display (Display-LG/MD):** Used for "Hero" animation titles. These should be tight-leaded and bold, acting as a visual anchor.
-   **Headline (Headline-LG):** Used for value propositions. At 2rem, these provide clear, scannable benefits.
-   **Title (Title-LG/MD):** For card titles and features. These bridge the gap between "reading" and "scanning."
-   **Body (Body-LG/MD):** The "Workhorse." Set in `on_surface_variant` (#5f5f5f) to reduce eye strain while maintaining legibility.
-   **Label (Label-MD/SM):** Used for micro-copy, like "Compatible with M3." Always in Medium or Bold weights to ensure visibility at small sizes.

**Editorial Tip:** Use "Asymmetric Heading." Don't center-align everything. A left-aligned `Display-LG` title paired with a right-aligned `Label-MD` creates a sophisticated, editorial rhythm that feels custom-built.

---

## 4. Elevation & Depth

We eschew traditional drop shadows in favor of **Tonal Layering**.

-   **The Layering Principle:** Depth is achieved by "stacking." A `surface-container-lowest` card placed on a `surface-container` background creates a natural, soft lift.
-   **Ambient Shadows:** If an element must float (e.g., a "Buy Now" button), use an extra-diffused shadow: `box-shadow: 0 10px 40px rgba(0, 0, 0, 0.06)`. The shadow is a whisper, not a shout.
-   **The "Ghost Border" Fallback:** If accessibility requires a container edge, use `outline_variant` (#b2b2b2) at 15% opacity. It should be felt, not seen.
-   **Glassmorphism:** Use for mobile headers. A semi-transparent `surface` with a blur allows the animation previews to bleed through as the user scrolls, creating a sense of continuity and premium polish.

---

## 5. Components

### Buttons
-   **Primary:** Rounded `full` (9999px). Background: `primary` gradient. Text: `on_primary` (Bold). Generous horizontal padding (Spacing 6).
-   **Secondary:** Rounded `full`. Background: `secondary_container` (#e3e2e7). No border. This mimics the "Apple-style" button found on their product pages.

### Cards (The "Showcase" Card)
Forbid divider lines. Separate the animation preview from the description using a Spacing 4 (`1.4rem`) gap or a subtle background shift to `surface-container-high`. Use the `lg` (1rem) corner radius to match the flagship smartphone aesthetic.

### Input Fields
-   **State:** Background should be `surface-container-highest`. No border.
-   **Focus:** Transition background to `surface-container-lowest` and add a 2px "Ghost Border" using `primary`.

### Specialized Component: The "Feature Ribbon"
A horizontal scrolling list of "Chips" (e.g., "4K", "No Plugins", "Fast Render") using `secondary_container` backgrounds and `on_secondary_container` text. These should have a `md` (0.75rem) roundedness to contrast with the `full` roundedness of buttons.

---

## 6. Do's and Don'ts

### Do
-   **Do use generous whitespace:** If you think there is enough space, add 20% more. Use Spacing 12 (`4rem`) for section gaps.
-   **Do use "Airy" imagery:** Product mockups should have soft, natural shadows and be placed off-center to create visual interest.
-   **Do prioritize "Tonal Contrast":** Ensure the difference between `surface` and `on_surface` meets WCAG AA standards for readability.

### Don't
-   **Don't use 1px black borders:** They make the interface feel "templated" and cheap.
-   **Don't use pure black (#000) for text:** Use `on_surface` (#323232) to maintain a premium, editorial softness.
-   **Don't crowd the mobile screen:** If a section feels cramped, move content into a "See More" progressive disclosure or a horizontal carousel.
-   **Don't use high-intensity shadows:** If the shadow is clearly visible as a "dark smudge," it is too heavy. It should appear as an ambient occlusion.

---

**Director's Closing Note:** This system is about the "space between" as much as the elements themselves. Every pixel of whitespace is a deliberate choice. Build with the confidence that the content—our animations—is the hero; the UI is merely the gallery.```