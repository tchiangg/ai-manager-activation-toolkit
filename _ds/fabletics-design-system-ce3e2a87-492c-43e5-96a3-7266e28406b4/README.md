# Fabletics Design System

Internal working design system reference for designs produced in this project. Based on the Fabletics.com web codebase (TechStyleOS / Fabletics brand theme).

---

## COMPANY CONTEXT

**Fabletics** is an activewear and lifestyle brand founded in 2013 by Kate Hudson, Adam Goldenberg, and Don Ressler. Part of TechStyle Fashion Group (TechStyleOS), Fabletics pioneered the VIP membership model for activewear — a monthly credit system that gives members access to discounted outfits and exclusive product drops.

**Product family covered by this system:**
- **Fabletics (Women's)** — primary brand. Activewear, loungewear, swim, scrubs, dresses. VIP membership is central.
- **Fabletics Men** — men's activewear, using the same tokens with masculine photography and typography treatment.
- **FabKids** — kids activewear and apparel. Playful, brighter palette, still anchored by Fabletics system.
- **Yitty** — shapewear by Lizzo (standalone brand, has its own theme — not covered here in depth).

**Voice & values:** empowering, body-positive, inclusive (extended sizes are table stakes — XXS–4X), community-driven, pragmatic-not-precious. Copy is conversational, direct, and occasionally playful. Avoid fitness-bro clichés and perfection tropes.

**VIP Membership is everywhere.** Almost every surface shows a member price, a credit badge, or a "become a VIP" nudge. Design for two price states (regular + VIP) and one loyalty state (Sunshine-yellow accent) by default.

---

## CONTENT FUNDAMENTALS

### Voice
- **Direct and active.** "Shop the collection" not "Explore our latest arrivals."
- **Confident, not pushy.** "Yours for $24.95 as a VIP" beats "ONLY $24.95!!!"
- **Inclusive by default.** Copy addresses "you" — never assume body type, ability, fitness level, or gender outside brand-specific surfaces.
- **Sparing use of ALLCAPS** — reserved for CTAs, eyebrow labels, and navigation tabs.

### Price & promo language
- Regular price is shown first, member/VIP price as the emphasized state.
- Sale prices use `--text-sale` (jewel-red-110). Strikethrough the original.
- "Member", "VIP", "Elite" are capitalized as proper nouns.
- Scarcity/urgency callouts use jewel-red — never invent new alert colors.

### Do / don't
- ✅ "2 for $24", "Yours for $39 as a VIP", "Almost gone"
- ❌ "AMAZING DEAL!", "Don't miss out!!", "Limited time only*" (footnoted legal)

---

## VISUAL FOUNDATIONS

### Philosophy
Fabletics is **product-first**. Photography is the hero — the UI exists to frame it. That means:
- Clean, bright, mostly-white surfaces.
- Sand (warm off-white) for softer secondary surfaces.
- Shadow (near-black) for text and primary buttons.
- Sunshine yellow as the single brand accent — used for hero moments, brand expression, and key emphasis.
- Jewel Red is the action color: CTAs, sale, urgency, and the saved wishlist heart.

### Grid & spacing
- 8px base grid. Spacing scale: 4, 8, 12, 18, 32, 36, 40, 48 (see `--sp-*`).
- Product grids: 2-up on mobile, 3-up on tablet, 4-up on desktop.
- Generous whitespace above and below editorial sections (48–80px).

### Surfaces
- Cards usually have **no shadow** — they rely on image + background contrast.
- When shadow is needed, it's subtle (`--shadow-sm`).
- Borders are hairline (1px, `--color-shadow-15` or `--color-shadow-25`).
- Rounded corners are **small or none**. Buttons use 4px radius, cards typically 0px.

### Buttons
- **Primary:** black fill, white text, uppercase, 4px radius, weight 600+. Hover → true black.
- **Secondary:** sand fill, black text, uppercase. Hover → sand-110.
- **Add to Bag:** jewel-red fill, white text, uppercase (primary PDP CTA).
- **Link:** black text, no background, underline on hover.
- All buttons use the brand font, 600 weight, tracking 0.02em, uppercase.

### Imagery
- Model photography dominates. In-studio on neutral/sand backdrops OR lifestyle in warm natural light.
- Flat-lays for details (fabric swatches, back-view, close-ups of waistband/pockets).
- Avoid heavy filters, duotones, or stylized color grading.

---

## ICONOGRAPHY

Fabletics uses **thin, geometric line icons** (1.5–2px stroke). Common glyphs:
- Search, Account (person), Wishlist (heart), Bag (shopping bag with handles), Store Locator (pin)
- Chevrons for navigation (right/left/down)
- Checkmark (bold), X close, Plus/minus accordion
- Truck (free shipping), Lock (secure checkout), Question mark (tooltips)

**Rules:**
- Line weight: 1.5px at 24px size. Scale proportionally.
- Corners: rounded (lineJoin: round, lineCap: round).
- Color: `currentColor` — never hard-code. Usually shadow (black) on light, white on dark.
- No filled icons except the **wishlist heart when saved** (jewel-red fill).
- No emoji in product UI.

If you need an icon and don't have a matching SVG, use a **minimal line placeholder** — do not generate illustrative SVG scenes.

---

## PRODUCT SURFACES

The system ships UI kits for Fabletics's core shopping surfaces:
- **PDP** (Product Detail Page) — swatches, size selector, member price, Add to Bag, outfit recommendations.
- **PLP / Grid** (Product Listing) — filter rail, sort dropdown, product cards.
- **Mini Cart** — slide-out drawer with free-shipping progress, line items, promo.
- **Checkout** — accordion steps, order summary, payment methods.
- **Account / VIP Home** — membership status, credits, skip-the-month.
- **Navigation** — meta nav bar, flyout mega-menu, mobile hamburger.

See `preview/` cards for each component family.

---

## FILES IN THIS PROJECT

| File | Purpose |
|---|---|
| `styles/colors_and_type.css` | Core tokens + type utilities. Import first. |
| `assets/` | Logos, brand marks, placeholder fonts. |
| `preview/` | Reviewable design-system cards (palette, type, buttons, etc.). |
| `SKILL.md` | How to use this system when designing in this project. |

---

## REFERENCES
- Source: `fabletics-design-system-source/01-tokens/themes/fabletics/` (colors, fonts, typography, buttons, sizes).
- Live site: [fabletics.com](https://www.fabletics.com)
