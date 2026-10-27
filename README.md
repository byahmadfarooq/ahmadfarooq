# Ahmad Farooq — Personal Portfolio

Hand-crafted single-page portfolio for Ahmad Farooq (Go-to-market, Operations and Product). Built with Astro, hand-written semantic HTML, CSS custom properties, self-hosted typography, and zero client framework overhead.

## Design System

- **Background:** Warm cream `#F4EFE6` with subtle 36px architectural grid.
- **Typography:**
  - Display / Headings: `Newsreader` (self-hosted WOFF2, subsetted).
  - Body / UI: `Inter` (self-hosted WOFF2, subsetted).
- **Text:** Charcoal `#1A1A1A`.
- **Accent:** Burnt orange `#E4572E` for links, buttons, and highlights.
- **Performance:** 0 KB external JavaScript runtime, inlined critical CSS, preloaded fonts, responsive AVIF/WebP images.

---

## How to Edit Copy

All site sections and copy live directly in [`src/pages/index.astro`](src/pages/index.astro).

1. **Hero**: Lines 11–24
2. **What I do (Three Columns)**: Lines 27–64
3. **Selected work**: Lines 67–141
4. **Background**: Lines 188–200
5. **Contact**: Lines 203–240

To edit the 404 page copy, update [`src/pages/404.astro`](src/pages/404.astro).

---

## How to Add a Decision Framework Entry

The Decision Frameworks section is dynamically driven by [`src/data/frameworks.json`](src/data/frameworks.json).

> When `src/data/frameworks.json` is empty (`[]`), the section and its navigation link are **completely hidden**. No empty boxes or placeholder content are rendered.

### Step 1: Save the Screenshot
Save an annotated screenshot of the work into `public/images/frameworks/` (e.g. `public/images/frameworks/checkout-flow.webp`).

### Step 2: Add Entry to `src/data/frameworks.json`
Add an object to the JSON array:

```json
[
  {
    "id": "checkout-refactor",
    "title": "Checkout Flow Redesign",
    "clientLabel": "SaaS Platform",
    "image": "/images/frameworks/checkout-flow.webp",
    "decisionOverImage": "Replaced 4-step wizard with single-page drawer checkout",
    "decision": "Eliminated multi-step friction and condensed payment to a slide-over modal.",
    "why": "Drop-off analytics showed 62% of abandonments happened on step 3 address validation."
  }
]
```

### Fields:
- **`clientLabel`**: Badge displayed over the screenshot covering the client name.
- **`decisionOverImage`**: The strategic callout banner placed directly over the screenshot.
- **`decision`**: The "Decision" description line.
- **`why`**: The "Why" reasoning line.

Once saved and rebuilt, the Decision Frameworks section and its navigation link will immediately appear in the layout.

---

## Development & Deployment

```bash
# Install dependencies
npm install

# Start local development server
npm run dev

# Build production static bundle (dist/)
npm run build

# Preview production build locally
npm run preview
```
