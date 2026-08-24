# Design System & UI/UX Guidelines: "En tus zapatos"

## 1. Brand Summary

* **Name:** En tus zapatos
* **Slogan:** "Put yourself in their shoes and find the solution"
* **Purpose:** "En tus zapatos" is an interactive, empathy-building web application designed to help family members understand different perspectives through role-based scenario roulette. By encouraging users to navigate everyday family dynamics from another person's standpoint, the application fosters constructive communication, deeper emotional connection, and collaborative problem-solving across generations.

---

## 2. Color Palette

The color system utilizes role-specific primary colors to establish instant visual context, paired with high-contrast neutral foundations for readability and accessibility.

### Core & Surface Colors

| Role / Element | HEX Code | Purpose / Usage | Contrast Ratio (vs #FFFFFF / Target) |
| :--- | :--- | :--- | :--- |
| **Typography** | `#000000` | Primary text, headers, and high-emphasis body content | 21.0:1 (Passes AAA) |
| **Background** | `#FFFFFF` | Core application background, card fills, clean modal surface | 1.0:1 (Base canvas) |
| **Surface Alt** | `#F8F9FA` | Off-white section backgrounds, subtle contrast fills | 1.05:1 (vs #000000 = 20.0:1) |
| **Pattern Pattern / Footprints**| `#EBECEF` | Subtle background footprint decorative pattern | 1.15:1 (Decorative only) |

### Role-Based Accent Colors

| Role | HEX Code | Theme / Persona Context | Contrast vs White (#FFFFFF) | Contrast vs White Text (#FFFFFF) |
| :--- | :--- | :--- | :--- | :--- |
| **Mom** | `#4F0377` | Deep Violet / Authority & Care | 12.2:1 (Passes AAA) | 12.2:1 (White text on Mom background) |
| **Dad** | `#1D3E89` | Royal Navy / Structure & Calm | 9.8:1 (Passes AAA) | 9.8:1 (White text on Dad background) |
| **Daughter** | `#AE00BC` | Vivid Magenta / Energy & Expression | 4.8:1 (Passes AA) | 4.8:1 (White text on Daughter background) |
| **Son** | `#00A0A0` | Teal / Playfulness & Curiosity | 3.1:1 (Requires dark text) | 3.1:1 (Use `#000000` text on light teal surface or `#004D4D` for icons) |
| **Pet** | `#AD7E40` | Warm Ochre / Comfort & Companionship | 3.2:1 (Requires dark text) | 3.2:1 (Use dark badge text or `#5C3E14` for dark text contrast) |
| **Grandfather**| `#B6BA6A` | Olive Gold / Wisdom & Tradition | 2.1:1 (Requires dark text) | 2.1:1 (Use `#1A200C` text on badge tags) |

---

## 3. Typography

The typographic hierarchy combines the warm, friendly, rounded display style of **Fredoka** for headings with the high-legibility, humanist sans-serif **Mukta Mahee** for paragraph and body text.

* **Display Font (Headings):** `Fredoka`, sans-serif (Weights: 500 SemiBold, 600 Bold, 700 ExtraBold)
* **Body Font (Copy & UI):** `Mukta Mahee`, sans-serif (Weights: 400 Regular, 600 SemiBold, 700 Bold)

### Typographic Scale

| Element | Font Family | Size (rem / px) | Line Height | Weight | Usage |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **H1** | Fredoka | `2.25rem` (36px) | `1.2` (43.2px) | 700 (Bold) | Main screen titles, roulette center headings |
| **H2** | Fredoka | `1.75rem` (28px) | `1.25` (35px) | 700 (Bold) | Section headers, "SITUACIONES" header |
| **H3** | Fredoka | `1.375rem` (22px) | `1.3` (28.6px) | 600 (SemiBold)| Card titles, scenario subheadings |
| **H4** | Fredoka | `1.125rem` (18px) | `1.35` (24.3px) | 600 (SemiBold)| Sub-section titles, modal titles |
| **H5** | Mukta Mahee | `1.0rem` (16px) | `1.4` (22.4px) | 700 (Bold) | Component headers, field labels |
| **H6** | Mukta Mahee | `0.875rem` (14px) | `1.4` (19.6px) | 700 (Bold) | Small badge headings, table headers |
| **Body (Large)**| Mukta Mahee | `1.125rem` (18px) | `1.6` (28.8px) | 400 (Regular) | Key scenario narratives, intro paragraphs |
| **Body (Default)**| Mukta Mahee| `1.0rem` (16px) | `1.5` (24px) | 400 (Regular) | General body text, descriptions |
| **Buttons** | Fredoka | `1.0rem` (16px) | `1.0` (16px) | 600 (SemiBold)| Interactive call-to-action buttons |
| **Captions / Tags**| Mukta Mahee| `0.75rem` (12px) | `1.33` (16px) | 600 (SemiBold)| Footnotes, meta tags, footprint labels |

---

## 4. Spacing and Grid Layout

A strict **8px Spatial System** (with a 4px sub-grid for micro-adjustments) governs layout, component padding, and margins to guarantee vertical rhythm and scale accuracy across screens.

### Base Spacing Scale

* `space-1` = 4px (`0.25rem`) - Micro spacing, badge padding
* `space-2` = 8px (`0.5rem`) - Icon margins, inline gap
* `space-3` = 12px (`0.75rem`) - Compact component padding
* `space-4` = 16px (`1.0rem`) - Standard card padding, input padding
* `space-5` = 24px (`1.5rem`) - Section spacing, container inner padding
* `space-6` = 32px (`2.0rem`) - Major element gaps, card border radius
* `space-8` = 48px (`3.0rem`) - Layout section gutters
* `space-10` = 64px (`4.0rem`) - Large hero padding

### Layout Containers & Grid

* **Mobile Max-Width:** `100%` (320px–767px), Margin: `16px` outer gutters.
* **Tablet Max-Width:** `720px` (768px–1023px), Margin: `auto`, Padding: `24px`.
* **Desktop Max-Width:** `1140px` (1024px–1439px), 12-Column Grid, Gaps: `24px`.
* **Large Desktop Max-Width:** `1320px` (1440px+), 12-Column Grid, Gaps: `32px`.
* **Mobile Layout Approach:** Mobile-first single-column layout stacked vertically with sticky floating action controls at the viewport base.

---

## 5. Responsive Breakpoints & Viewport Behavior

| Breakpoint | Layout Structure | Roulette Wheel Implementation | Scenario Card & Content Layout |
| :--- | :--- | :--- | :--- |
| **320px – 767px** *(Mobile)* | Single-column linear layout. Top role header, middle illustration card, bottom narrative body. | Compact radial wheel modal or bottom swipe selector. Wheel scale: 280px–320px diameter. | Card occupies 100% width. Header image aspect ratio 4:3. Floating action button (`48px`) anchored bottom-right. |
| **768px – 1023px** *(Tablet)* | Centered single-column or stacked 2-column hybrid with sticky top menu navigation. | Interactive spinning wheel centered above or inline with role card (420px diameter). | Card width max 600px. Expanded line height and increased typography scale (+2px). |
| **1024px – 1439px** *(Desktop)* | Dual-column side-by-side grid. Left side: Interactive Roulette + Role Selector. Right side: Dynamic Scenario Content. | Fully interactive SVG/Canvas 3D-styled roulette wheel fixed on the left grid (480px diameter). | Scenario Card fits right grid (6-col span). Text aligned left with rich multimedia attachments. |
| **1440px+** *(Wide Desktop)*| Centered 12-column layout with ambient decorative footprint pattern side margins. | Full-featured roulette with animated sector highlights and particle FX (540px diameter). | Scenario panel includes full historical log, solution prompt cards, and interactive family discussion notes. |

---

## 6. UI Components & Design Tokens

### 6.1 Buttons

#### Primary Button / Floating Action Button (FAB)
* **Visual Style:** Circular or pill-shaped, deep role color fill (`#4F0377`), white vector icon (`→`), elevation shadow.
* **Default:** `background: var(--role-color); color: #FFFFFF; border-radius: 50%; box-shadow: 0px 8px 16px rgba(0,0,0,0.18); min-width: 48px; min-height: 48px;`
* **Hover:** `transform: translateY(-2px); box-shadow: 0px 12px 20px rgba(0,0,0,0.25); filter: brightness(1.1);`
* **Active:** `transform: translateY(0px) scale(0.96); box-shadow: 0px 4px 8px rgba(0,0,0,0.2);`
* **Disabled:** `background: #E0E0E0; color: #9E9E9E; box-shadow: none; cursor: not-allowed; opacity: 0.6;`

#### Secondary / Pill Role Badges (e.g., "MAMÁ")
* **Default:** `background: #4F0377; color: #FFFFFF; font-family: 'Fredoka'; font-weight: 700; border-radius: 20px; padding: 6px 20px; box-shadow: 0px 4px 10px rgba(0,0,0,0.15);`

### 6.2 Cards

#### Scenario Header Card
* **Structure:** Top container for role illustration.
* **Styling:** `background-color: var(--current-role-color); border-radius: 24px; position: relative; overflow: hidden; padding: 24px; box-shadow: 0px 12px 28px -4px rgba(79, 3, 119, 0.3);`
* **Illustration Overlay:** White vector line artwork (`stroke: #FFFFFF`, `stroke-width: 2px`) centered within card frame.

#### Content Narrative Card
* **Styling:** `background: #FFFFFF; border-radius: 24px; padding: 24px 16px; margin-top: -16px; text-align: center;`

### 6.3 Input Fields
* **Default:** `border: 2px solid #E2E8F0; border-radius: 12px; padding: 12px 16px; font-family: 'Mukta Mahee'; font-size: 1rem; color: #000000; background: #FFFFFF; transition: all 0.2s ease;`
* **Hover:** `border-color: #CBD5E1;`
* **Focus / Active:** `border-color: var(--current-role-color); outline: none; box-shadow: 0 0 0 3px rgba(79, 3, 119, 0.2);`
* **Disabled:** `background: #F1F5F9; border-color: #E2E8F0; color: #94A3B8; cursor: not-allowed;`

### 6.4 Navbar
* **Header Structure:** Floating translucent header or integrated status bar.
* **Hamburger Menu Button:** Floating pill shape (`background: #FFFFFF; border-radius: 20px; padding: 8px 16px; box-shadow: 0 4px 12px rgba(0,0,0,0.1); border: 1px solid #F0F0F0;`). Includes 3 dark purple horizontal bars (`#4F0377`).

### 6.5 Footer
* **Styling:** Dynamic footer containing the indicator pill bar (`width: 134px; height: 5px; background: #4F0377; border-radius: 100px; margin: 16px auto;`) and quick navigation links.

### 6.6 Interactive Roulette Wheel Component
* **Structure:** Multi-segment circular canvas/SVG divided into 6 equal role sectors. Center pointer arrow pointing to the selected sector.
* **States:**
  * **Default / Idle:** Slow ambient rotation (`animation: spin-slow 20s linear infinite;`).
  * **Hover / Target Segment:** Sector scales outward by 4px with highlight outline (`filter: drop-shadow(0 0 8px rgba(255,255,255,0.8));`).
  * **Spinning (Active):** High-velocity CSS rotation easing (`transition: transform 4s cubic-bezier(0.15, 0.9, 0.2, 1);`).
  * **Selected / Result:** Pulsing halo effect around target scenario icon.

```css
/* CSS Variables Definition */
:root {
  /* Brand Role Colors */
  --color-mom: #4F0377;
  --color-dad: #1D3E89;
  --color-daughter: #AE00BC;
  --color-son: #00A0A0;
  --color-pet: #AD7E40;
  --color-grandfather: #B6BA6A;

  /* Active Context Defaults (Mom) */
  --current-role-color: var(--color-mom);
  --current-role-contrast: #FFFFFF;

  /* Typography Tokens */
  --font-heading: 'Fredoka', cursive, sans-serif;
  --font-body: 'Mukta Mahee', sans-serif;

  /* Elevation & Shadows */
  --shadow-card: 0px 12px 28px -4px rgba(79, 3, 119, 0.25);
  --shadow-button: 0px 8px 16px rgba(0, 0, 0, 0.18);
  --shadow-pill: 0px 4px 10px rgba(0, 0, 0, 0.12);

  /* Radius Tokens */
  --radius-lg: 24px;
  --radius-md: 16px;
  --radius-pill: 100px;
}
```

---

## 7. Accessibility (a11y) & Usability

* **WCAG AA Compliance:** All body text meets minimum contrast ratio of 4.5:1 against its background. Text rendered over dark role backgrounds (e.g., Mom `#4F0377`, Dad `#1D3E89`) uses `#FFFFFF` text to achieve >9:1 ratio. Roles with lighter HEX values (Son, Pet, Grandfather) automatically switch text badges to dark tones (`#000000` or `#1A200C`).
* **Minimum Touch Target Size:** All interactive buttons, floating navigation elements, role cards, and roulette sectors maintain a minimum interactive hit area of **44px × 44px** (48px × 48px recommended for mobile FABs).
* **Focus States:** Visible high-contrast focus ring (`3px solid #000000` or `3px solid var(--current-role-color)`) with `2px` offset on all keyboard-navigable elements.
* **ARIA & Screen Reader Support for Roulette Wheel:**
  * Container element: `role="region" aria-label="Interactive Scenario Roulette Wheel"`
  * Trigger button: `aria-controls="roulette-wheel" aria-expanded="false"`
  * Live Region: `aria-live="polite"` announcing scenario changes when the wheel stops spinning (e.g., *"Roulette stopped. Role selected: Mom. Scenario: Hijo no quiere hablar."*).
  * Reduced Motion: Respects `prefers-reduced-motion: reduce` by replacing fast wheel spin with a smooth fade-in reveal transition.

---

## 8. Visual Assets & Graphic Treatment

### Iconography & Vector Illustrations
* **Style:** Clean 2px white outline stroke vector art (`stroke: #FFFFFF; stroke-width: 2px; fill: none; stroke-linecap: round; stroke-linejoin: round;`).
* **Illustration Content:** Narrative family scenes with expressive thought/speech bubbles (`...`, `?`) emphasizing empathy and emotional state.

### Image & Container Treatment
* **Corners:** Heavy rounded corners (`border-radius: 24px`).
* **Shadow Depth:** Multi-layered soft drop shadows (`box-shadow: 0px 12px 28px -4px rgba(0,0,0,0.15)`).
* **Background Footprint Pattern:** Translucent repeating footprint track pattern on canvas background (`background-image: url('footprint-pattern.svg'); opacity: 0.08; background-repeat: repeat;`).

```css
/* Decorative Background Pattern & Container Treatment */
.app-container {
  background-color: #FFFFFF;
  background-image: url("data:image/svg+xml,%3Csvg width='60' height='60' viewBox='0 0 60 60' xmlns='http://www.w3.org/2000/svg'%3E%3Cpath d='...' fill='%2000000' fill-opacity='0.04'/%3E%3C/svg%3E");
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.scenario-card-header {
  background-color: var(--color-mom);
  border-radius: var(--radius-lg);
  padding: 32px 24px;
  box-shadow: var(--shadow-card);
  position: relative;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.role-badge-pill {
  background-color: var(--color-mom);
  color: #FFFFFF;
  font-family: var(--font-heading);
  font-size: 1.125rem;
  font-weight: 700;
  padding: 8px 28px;
  border-radius: var(--radius-pill);
  box-shadow: var(--shadow-pill);
  margin-top: -20px;
  z-index: 10;
}
```