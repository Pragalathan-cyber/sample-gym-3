# Design System: Cyber-Industrial Interface

## 1. Overview & Creative North Star
**Creative North Star: "The Kinetic Command Center"**

This design system transcends the standard "gym website" template to create a high-performance tactical interface. It is built on the philosophy of **Kinetic Precision**—where the UI feels like a live telemetry feed for the human body. We move beyond generic dark modes by utilizing a "Machined Editorial" approach: a layout defined by aggressive asymmetry, technical "HUD" (Heads-Up Display) elements, and a high-contrast palette that demands focus. 

The goal is to make the user feel like they are logging into a restricted training terminal. We break the grid intentionally—using overlapping containers and diagonal visual anchors to mimic the raw, industrial energy of a futuristic power plant.

---

## 2. Colors & Surface Logic
The palette is rooted in a "Deep Space" charcoal, punctuated by high-frequency neon accents. 

### The Color Logic
- **Primary (`#c1fffe` / `#00ffff`):** The "Cyber Cyan." Use this for active states, data visualizations, and primary action triggers.
- **Secondary (`#ff51fa` / `#a900a9`):** The "Electric Magenta." Use this sparingly for high-intensity highlights, "Extreme" tier alerts, or secondary CTAs to create a dual-tone chromatic vibration.
- **Background (`#0e0e0e`):** A pure, industrial void. This is the bedrock of the system.

### The "No-Line" Rule
Traditional 1px borders are strictly prohibited for sectioning. Structural definition must be achieved through:
1.  **Tonal Shifts:** Transitioning from `surface` (#0e0e0e) to `surface-container-low` (#131313).
2.  **Negative Space:** Utilizing the Spacing Scale (specifically `16` and `24` units) to create "air" between functional blocks.
3.  **Light Leaks:** Using a 10% opacity `primary` glow at the edge of a container to imply a boundary without a hard stroke.

### Surface Hierarchy & Nesting
Treat the UI as a series of machined plates. 
- **Base Level:** `surface` (#0e0e0e).
- **Secondary Plates:** `surface-container` (#1a1919) for content cards.
- **Active Insets:** `surface-container-highest` (#262626) for inputs or interactive zones.

### Signature Textures: The "Machined Glow"
To avoid a flat, "vector" look, apply a subtle linear gradient to all main surfaces: `surface-container-high` transitioning to `surface-container-lowest` at a 135-degree angle. This mimics the way light hits brushed metal.

---

### 3. Typography
Typography is our primary tool for establishing an authoritative, technical tone.

*   **Display & Headlines (Space Grotesk):** Geometric, wide, and aggressive. 
    *   *Editorial Tip:* Use `display-lg` for hero statements but set them to `uppercase` with `-0.05em` letter spacing to create a dense, "block-like" industrial feel.
*   **Body (Manrope):** Chosen for its high legibility in low-light environments. 
    *   *Editorial Tip:* Use `body-md` for standard descriptions, but always set `on-surface-variant` (#adaaaa) for secondary text to maintain a clear hierarchy against the `on-surface` (#ffffff) headlines.
*   **Labels (Space Grotesk):** Used for technical metadata (e.g., "KCAL BURNT", "RPM"). These should always be uppercase with `0.1em` letter spacing to mimic terminal readouts.

---

## 4. Elevation & Depth

### The Layering Principle
Forget drop shadows. Depth in this system is achieved through **Luminance Stacking**. A `surface-container-high` element placed atop a `surface` background provides all the "lift" required.

### Ambient Shadows
If an element must float (e.g., a modal), use a "Cyan Halo." Instead of a black shadow, use a diffuse glow: `box-shadow: 0 20px 50px rgba(0, 255, 255, 0.08);`. This mimics the ambient light of a monitor in a dark room.

### Glassmorphism & Depth
For floating HUD elements or navigation bars, use `surface-container-low` at 70% opacity with a `backdrop-filter: blur(12px)`. This keeps the "Industrial" weight while adding a "Cyber" sophistication.

---

## 5. Components

### Buttons: The "Beveled Kinetic"
- **Primary:** `primary-container` (#00ffff) background, `on-primary` (#006767) text. 
- **Shape:** 0px border-radius. Use a CSS `clip-path` to "cut" the top-right and bottom-left corners at a 45-degree angle for a beveled, tech-military look.
- **State:** On hover, add a `primary` outer glow and shift the background to `primary-fixed`.

### Input Fields: The "Terminal Entry"
- **Style:** No background. Only a bottom border using `outline-variant` (#494847).
- **Focus:** When active, the bottom border morphs into `primary` (#00ffff) with a 2px thickness and a subtle glow.
- **Label:** `label-sm` placed above the input, always in uppercase.

### Cards: The "Module"
- **Forbid dividers.** Separate card header from body using a background shift from `surface-container-highest` to `surface-container-low`.
- **Accents:** Place a 2px vertical "power bar" of `secondary` (#ff51fa) on the far-left edge of featured cards to denote "High Intensity."

### Chips: "Status Indicators"
- Small, rectangular blocks with 0px radius.
- Use `primary-dim` for "Active" and `error-dim` for "Restricted."

---

## 6. Do's and Don'ts

### Do:
- **Use Intentional Asymmetry:** Align text to the left but place supporting data visualizations or "HUD" ornaments on the far right.
- **Embrace Mono-spacing:** Use Space Grotesk for numbers to ensure they look like a digital readout.
- **Leverage "Ghost Borders":** If a container feels lost, use the `outline-variant` at 15% opacity.

### Don't:
- **No Rounded Corners:** `0px` is the absolute rule. Rounded corners break the industrial "armored" aesthetic.
- **No Soft Gradients:** Avoid "sunset" or "natural" gradients. Use high-contrast transitions or solid color blocks.
- **No Generic Icons:** Avoid thin-line "friendly" icons. Use heavy-weight, geometric icons with sharp terminals.
- **No Pure Grey Shadows:** Shadows should always be tinted with the `primary` cyan or `secondary` magenta to maintain the neon-soaked atmosphere.

---

## 7. Spacing Scale
Consistency in spacing ensures the "machined" look doesn't become messy.
- **Functional Gap (2.5 / 0.5rem):** Between related labels and inputs.
- **Section Gap (16 / 3.5rem):** Between distinct content modules.
- **Hero Margin (24 / 5.5rem):** Massive breathing room for high-impact headlines to dominate the viewport.