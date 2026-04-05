# Diamond Jasna – AI Agent Prompt za izradu websajta

Build a complete, single-page HTML website for **Diamond Jasna** – a premium hair salon. The project folder is located at `e:\PROJECTS\demo presentations\Diamond_Jasna\`. All assets (images) are already in place inside the `images/` subfolder. Do NOT move or rename any images.

---

## 🎨 Design Direction

- **Color palette:** Classy pink & rose gold theme. Use a rich palette: deep rose (`#c9748d`), blush pink (`#f2a7bb`), champagne/gold (`#d4a96a`), near-white cream (`#fff5f7`), and soft charcoal (`#2a1f24`) for text. Avoid flat or neon colors — use gradients and subtle shimmer effects.
- **Typography:** Import Google Fonts. Use **`Playfair Display`** (serif, elegant) for headings and **`Lato`** or **`Nunito`** (sans-serif) for body text.
- **Aesthetic:** Glassmorphism cards, subtle glitter/sparkle CSS animations on accents, smooth scroll behavior, fade-in on scroll (IntersectionObserver), hover micro-animations on buttons and gallery thumbnails.
- **Overall feel:** Luxurious, feminine, classy — like a high-end Parisian beauty boutique.

---

## 📁 File Structure

Create a **single `index.html` file** (with all CSS embedded in `<style>` and all JS embedded in `<script>`) saved at:

```
e:\PROJECTS\demo presentations\Diamond_Jasna\index.html
```

All image `src` paths must be **relative**, e.g.:
- Hero: `images/HERO IMAGE.png`
- Balayage gallery: `images/balayage color cut/PHOTO-2026-04-05-17-14-31.jpg` (and all subsequent files in that folder)
- Extensions gallery: `images/ekstenzije/PHOTO-2026-04-05-17-12-47.jpg` (and all subsequent files in that folder)

---

## 🗂️ Sections (in order)

### 1. `<head>` — SEO & Meta

Include the following SEO-optimized meta tags:

```html
<title>Diamond Jasna | Premium Hair Salon – Balayage, Color, Extensions</title>
<meta name="description" content="Diamond Jasna – luksuzni frizerski salon. Balayage, kolor, šišanje i ekstenzije. Zakazivanje putem WhatsApp-a, Viber-a ili emaila. Klijenti iz Beča – posebna usluga dolaska na lokaciju.">
<meta name="keywords" content="frizerski salon, balayage, kolor kose, ekstenzije, Diamond Jasna, hair salon, Vienna hair, Bec frizerski salon">
<meta name="robots" content="index, follow">
<meta property="og:title" content="Diamond Jasna | Premium Hair Salon">
<meta property="og:description" content="Luksuzni hair salon – balayage, kolor, ekstenzije. Zakazivanje preko WhatsApp i Viber.">
<meta property="og:type" content="website">
<link rel="canonical" href="https://diamondjasna.com">
```

---

### 2. Navigation Bar (sticky, glassmorphism)

- Logo text: **"💎 Diamond Jasna"** in Playfair Display, gold gradient color
- Nav links: `Početna`, `Usluge`, `Galerija`, `Bečki Klijenti`, `Kontakt`
- Smooth scroll to section anchors
- On mobile: hamburger menu toggle
- Background: translucent frosted glass (`backdrop-filter: blur`) with a subtle pink-rose gradient border at the bottom

---

### 3. Hero Section (`id="pocetna"`)

- Full viewport height (`100vh`)
- Background: use `images/HERO IMAGE.png` as a full-width background image with `object-fit: cover`, overlay with a soft gradient (`rgba(201,116,141,0.35)` to transparent)
- Large centered heading: **"Diamond Jasna"** in Playfair Display, white, with a subtle text-shadow
- Subheading: *"Tvoj stil. Tvoj sjaj. Tvoje dijamantsko iskustvo."* (elegant italic)
- CTA button: **"Zakaži termin"** → smooth scrolls to `#kontakt`, styled in rose-gold gradient with shimmer hover animation

---

### 4. Services Section (`id="usluge"`)

- Section title: "Naše Usluge" (centered, Playfair Display)
- Display **3 service cards** in a row (flex/grid), glassmorphism style with hover lift:
  1. 💇‍♀️ **Balayage & Kolor** – "Savremene tehnike bojenja koje naglašavaju prirodnu lepotu vaše kose."
  2. ✂️ **Šišanje & Styling** – "Precizno oblikovanje i šišanje prilagođeno vašem licu i stilu."
  3. 💎 **Ekstenzije** – "Dodajte dužinu i volumen sa premium ekstenzijama za savršen izgled."

---

### 5. Gallery Section (`id="galerija"`)

- Section title: "Naši Radovi" with subtitle "Pogledajte transformacije"
- **Two subsections**, each as a horizontally scrollable carousel/lightbox slider:

**A) Balayage, Kolor & Šišanje** – load all 22 images from `images/balayage color cut/`:

```
PHOTO-2026-04-05-17-14-31.jpg
PHOTO-2026-04-05-17-14-31_1.jpg
PHOTO-2026-04-05-17-14-31_2.jpg
PHOTO-2026-04-05-17-14-31_3.jpg
PHOTO-2026-04-05-17-14-31_4.jpg
PHOTO-2026-04-05-17-14-32.jpg
PHOTO-2026-04-05-17-14-35.jpg
PHOTO-2026-04-05-17-14-35_1.jpg
PHOTO-2026-04-05-17-14-35_2.jpg
PHOTO-2026-04-05-17-14-36.jpg
PHOTO-2026-04-05-17-14-36_1.jpg
PHOTO-2026-04-05-17-14-36_10.jpg
PHOTO-2026-04-05-17-14-36_11.jpg
PHOTO-2026-04-05-17-14-36_12.jpg
PHOTO-2026-04-05-17-14-36_2.jpg
PHOTO-2026-04-05-17-14-36_3.jpg
PHOTO-2026-04-05-17-14-36_4.jpg
PHOTO-2026-04-05-17-14-36_5.jpg
PHOTO-2026-04-05-17-14-36_6.jpg
PHOTO-2026-04-05-17-14-36_7.jpg
PHOTO-2026-04-05-17-14-36_8.jpg
PHOTO-2026-04-05-17-14-36_9.jpg
```

**B) Ekstenzije** – load all 12 images from `images/ekstenzije/`:

```
PHOTO-2026-04-05-17-12-47.jpg
PHOTO-2026-04-05-17-12-47_1.jpg
PHOTO-2026-04-05-17-12-47_2.jpg
PHOTO-2026-04-05-17-12-47_3.jpg
PHOTO-2026-04-05-17-12-48.jpg
PHOTO-2026-04-05-17-12-48_1.jpg
PHOTO-2026-04-05-17-12-48_2.jpg
PHOTO-2026-04-05-17-12-48_3.jpg
PHOTO-2026-04-05-17-12-48_4.jpg
PHOTO-2026-04-05-17-12-48_5.jpg
PHOTO-2026-04-05-17-12-48_6.jpg
PHOTO-2026-04-05-17-12-48_7.jpg
```

- Gallery implementation:
  - Show images as a **horizontal scroll strip** with thumbnail cards (uniform height ~250px, `object-fit: cover`, rounded corners, subtle box-shadow)
  - On thumbnail **click**: open a **full-screen lightbox modal** showing the image enlarged with Prev/Next arrow navigation and close (✕) button
  - Thumbnail hover: scale up slightly + add rose-gold border glow
  - Arrow buttons (‹ ›) on both sides of the strip to scroll the strip left/right programmatically

---

### 6. Vienna / Bečki Klijenti Section (`id="becki-klijenti"`)

- **Visually distinct** section — use a deep charcoal or dark rose background with gold accents to make it stand out
- Heading: **"✈️ Klijenti iz Beča"** in Playfair Display, gold color
- Short elegant paragraph in Serbian AND English (bilingual, side by side or stacked):
  - **SR:** *"Jasna redovno posećuje Beč i pruža usluge na licu mesta. Kada se skupi dovoljan broj klijenata, ona dolazi direktno do vas – pravo luksuzno iskustvo u vašem prostoru. Prijavite interesovanje putem WhatsApp-a ili Vibera."*
  - **EN:** *"Jasna regularly visits Vienna to provide her services on-site. Once enough clients from Vienna express interest, she travels directly to you – a true luxury experience in your own space. Get in touch via WhatsApp or Viber to register your interest."*
- A stylized icon row: ✈️ 💎 🌍
- CTA button: **"Prijavi se / Register Interest"** → links to `#kontakt`

---

### 7. Contact Section (`id="kontakt"`)

- Section title: "Kontakt" centered
- Display **3 contact method cards** (glassmorphism, centered, responsive):
  1. 📱 **WhatsApp** – label "WhatsApp", value `+381 XX XXX XXXX` (mock), button: "Pošalji poruku" → `href="https://wa.me/381XXXXXXXXX"`
  2. 📳 **Viber** – label "Viber", value `+381 XX XXX XXXX` (mock), button: "Pozovi / Poruka" → `href="viber://chat?number=381XXXXXXXXX"`
  3. 📧 **Email** – label "Email", value `jasna@diamondjasna.com` (mock), button: "Pošalji email" → `href="mailto:jasna@diamondjasna.com"`
- Below the cards, a small elegant note: *"Radno vreme: Pon – Sub, 9:00 – 19:00"*

---

### 8. Footer

- Dark background (charcoal), centered
- Text: `© 2025 Diamond Jasna. Sva prava zadržana.`
- Small sparkling diamond emoji as decorative separator: `💎`
- Social note: "Pratite nas:" (for future use, just stylized text — no real links needed)

---

## ✨ Animations & Interactions

- **Sparkle/glitter effect:** Add a subtle CSS keyframe animation (`@keyframes sparkle`) that creates a shimmering gold shimmer on the logo and the section divider lines
- **Fade-in on scroll:** Use `IntersectionObserver` in JavaScript — every section fades in from below (`opacity: 0; transform: translateY(30px)`) when it enters the viewport
- **Smooth scroll:** `scroll-behavior: smooth` on `<html>`
- **Button shimmer:** Add a moving shine/glare effect (`::after` pseudo-element animation) on all primary CTA buttons on hover
- **Navbar scroll effect:** On scroll, navbar gains a slightly more opaque background

---

## 📱 Responsive Design

- Fully responsive: mobile-first
- Navbar: hamburger menu on screens < 768px
- Services: 3 cols → 1 col on mobile
- Gallery: horizontal scroll works on touch devices (touch-friendly swipe)
- Contact cards: 3 cols → 1 col on mobile

---

## ⚠️ Final Notes

- Write everything in a **single `index.html`** file — CSS in `<style>`, JS in `<script>` at bottom of `<body>`
- All image paths must be **relative** and exactly match the filenames listed above (case-sensitive)
- Do NOT use any external CSS frameworks (no Bootstrap, no Tailwind)
- Do NOT use any external JS libraries (no jQuery, no Swiper) — implement all interactivity in vanilla JS
- The site must be **fully functional when opened as a local file** (`file://` protocol) — no server required
