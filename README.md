# Angkor Craft — E-commerce Website

Week 08 assignment · HTML & CSS only · no JavaScript, no frameworks

A five-page storefront for a fictional Cambodian handicraft shop selling krama
scarves, silk, Kampot pepper, silver, lacquerware and wood carving.

---

## How to open it

Double-click `index.html`. Everything works straight from the folder — there is
no build step and nothing to install. The only part that needs internet is the
Google map on the contact page.

---

## Files

| File | What it is |
|---|---|
| `index.html` | Home — hero banner, categories, best sellers, why shop with us |
| `shop.html` | All 9 products, category filter bar, pagination |
| `product.html` | One product in detail — options, description, specification |
| `cart.html` | Shopping cart table and order summary |
| `contact.html` | Contact form, shop details, map, frequently asked |
| `css/style.css` | The one stylesheet used by all five pages |
| `images/` | All pictures used by the site |

Every page has the identical header, navigation and footer, so learning one page
means understanding all five.

---

## What each page demonstrates

| Page | Skills shown |
|---|---|
| `index.html` | Headings and text, images with `alt`, flexbox rows, the box model |
| `shop.html` | Relative links, a repeated card layout, hover states |
| `product.html` | `<dl>` description list, a two-column `<table>`, `<select>` and form controls |
| `cart.html` | A `border-collapse` table with prices and totals, like the week 6 invoice |
| `contact.html` | A full form with `<label>`, `required`, `<textarea>`, and an `<iframe>` map |

---

## How the CSS is organised

`css/style.css` opens with a numbered table of contents, and the sections appear
in that same order:

1. **Design tokens** — every colour and spacing size, declared once in `:root`
2. **Reset & base** — clears browser defaults, sets the body font
3. **Layout** — `.container`, `.section`, `.split`
4. **Buttons** — `.btn` and its variants
5. **Header & nav**
6. **Hero**
7. **Cards & grids** — product cards, category cards, product detail
8. **Tables** — cart and specification
9. **Forms**
10. **Footer**
11. **Utilities** — small helpers like `.text-center`, `.mt-md`
12. **Responsive** — one media query for screens 800px and narrower

Because all colours live in `:root`, changing the gold accent on the whole site
is a single-line edit:

```css
:root {
    --color-gold: #C08A2E;   /* change this one value */
}
```

---

## Class naming

Names read as `block__element` and `block--variant`:

- `.product-card` — the block
- `.product-card__body` — a part inside that block
- `.btn--gold` — a variant of `.btn`

---

## Images

All pictures live in `images/`. Filenames are fixed — replace the file, keep the
name, and the page picks it up with no HTML change.

If an image is missing the page still lays out correctly: the tile keeps its size
and shows the `alt` text instead. See `IMAGE-PROMPTS.md` for the list of images
the site expects.

---

## Deliberately not included

No JavaScript, no CSS framework, no web fonts. The "Add to cart", "Checkout" and
"Send message" buttons do not submit anywhere, because a static site has no
server behind it.
