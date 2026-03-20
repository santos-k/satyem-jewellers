# 💍 Satyam Jewellers – Landing Page

> **“Hans” — Where Gold Meets Grace**  
> A fully interactive, bilingual, single-file landing page for Satyam Jewellers, Gaya, Bihar.

Live at https://santos-k.github.io/satyem-jewellers/
-----

## 📋 Overview

This is a complete business landing page built as a single self-contained HTML file for **Satyam Jewellers** — a gold and silver jewellery shop located at Kotwa Bazar, Gaya (NH-99, Bihar). The page is designed to help the business grow online with a professional digital presence, bilingual support, and customer engagement features.

**Shop Details:**

- 📍 Dobhi Chatra Road, NH-99, Kotwa Bazar, Gaya – 824220, Bihar
- 📞 +91 97710 59935 / +91 83402 00054
- 🏅 BIS Hallmarked | 91.6 / 750 Certified
- 💛 18K & 22K Pure Gold | Pure Silver Available

-----

## 🚀 How to Use

No server, no installation, no dependencies needed.

1. Download `index.html`
1. Open it in any modern web browser (Chrome, Firefox, Edge, Safari)
1. That’s it — fully functional offline

```
# Optional: serve locally
npx serve .
# or
python3 -m http.server 8080
```

-----

## ✨ Features

### 🌐 Bilingual — English & Hindi

- Toggle between **English (EN)** and **हिंदी (HI)** instantly
- Every section translates: navigation, hero, catalog, products, why us, purity, testimonials, contact form, footer, modal, and toast messages
- Hindi rendered with **Tiro Devanagari Hindi** font for authentic display
- Default language: **English**

### 🌙 Dark / Light Theme

- Toggle between **Dark mode** (gold-on-charcoal luxury aesthetic) and **Light mode** (warm ivory/cream tones)
- Smooth CSS transitions across all elements
- Default theme: **Dark**

### 📱 Fully Responsive

- Works on all screen sizes — mobile, tablet, desktop
- Hamburger menu on mobile with full-screen overlay nav
- Adaptive grids using CSS `auto-fill` / `minmax`
- Touch-friendly buttons and tap-to-call links

### 🗂️ Sections

|Section         |Description                                                                                           |
|----------------|------------------------------------------------------------------------------------------------------|
|**Hero**        |Full-screen brand intro with trust badges (BIS, 18K/22K, hallmarked) and animated mandala             |
|**Marquee**     |Scrolling ticker of jewellery categories                                                              |
|**Stats**       |Animated counters — 500+ families, 200+ designs, 22 years, 100% pure gold                             |
|**Catalog**     |6 clickable category cards — bangles, necklaces, earrings, silver, bridal, custom orders              |
|**Explore**     |12 product cards with live category filter (All / Bangles / Necklaces / Earrings / Silver / Bridal)   |
|**Why Satyam**  |6 trust pillars — BIS certified, master craftsmen, 200+ designs, fair pricing, custom orders, location|
|**Purity**      |18K / 22K / Silver / BIS certification showcase with animated hallmark badge                          |
|**Testimonials**|3 customer reviews with star ratings                                                                  |
|**Contact**     |Address, phone, hours, shop name + enquiry form with success state                                    |
|**Footer**      |Brand tagline, phone numbers, collection links, quick links, BIS badge                                |

### 📞 Interactive Features

- **Floating Call Button** — pulsing fixed button, opens tap-to-call modal with both phone numbers
- **Product Filter** — live filter by jewellery category, updates instantly
- **Enquiry Form** — name, phone, category dropdown, message; pre-fills from product “Enquire” click
- **Product Enquire** — clicking Enquire on any product auto-fills the contact form and scrolls to it
- **Toast Notifications** — contextual feedback for form actions and enquiries
- **Scroll-triggered Animations** — cards fade up on scroll using IntersectionObserver
- **Navbar Shrink** — navbar compacts on scroll
- **Mobile Hamburger Menu** — full-screen overlay navigation

-----

## 🏗️ Technical Stack

|Technology                  |Usage                                                                             |
|----------------------------|----------------------------------------------------------------------------------|
|**HTML5**                   |Semantic structure, single-file                                                   |
|**CSS3**                    |Custom properties (variables), flexbox, CSS grid, keyframe animations, transitions|
|**Vanilla JavaScript**      |All interactivity — no frameworks, no jQuery                                      |
|**Google Fonts**            |Cinzel, Cormorant Garamond, Lato, Tiro Devanagari Hindi                           |
|**IntersectionObserver API**|Scroll-triggered fade-in animations and counter triggering                        |
|**Base64 Images**           |Jewellery illustrations embedded directly — zero external image dependencies      |

-----

## 🎨 Design System

### Color Palette

```css
--gold:       #C9A84C   /* Primary gold */
--gold-light: #F0D080   /* Light gold / highlights */
--gold-dark:  #8B6914   /* Dark gold / shadows */
--crimson:    #9B1B30   /* Accent / branding red */

/* Dark Theme */
--bg:         #1A1410   /* Main background */
--bg-deep:    #141010   /* Deeper background */
--text:       #FDF8EE   /* Primary text (cream) */

/* Light Theme */
--bg:         #FDF8EE   /* Warm ivory background */
--text:       #1A1410   /* Dark text */
```

### Typography

- **Cinzel** — headings, logo, section titles (serif, Roman-inspired)
- **Cormorant Garamond** — subheadings, quotes, italic accents (elegant serif)
- **Lato** — body text, buttons, labels (clean sans-serif)
- **Tiro Devanagari Hindi** — all Hindi/Devanagari text

-----

## 📁 File Structure

```
satyam-jewellers.html    ← Single self-contained file (~886KB)
README.md                ← This file
```

The entire site — HTML, CSS, JavaScript, fonts (via CDN), and all jewellery images (base64 encoded) — lives in one file.

-----

## 🔧 Customisation Guide

### Update Business Details

Search for and replace in the HTML:

|Find                        |Replace With        |
|----------------------------|--------------------|
|`+91 97710 59935`           |Your primary phone  |
|`+91 83402 00054`           |Your alternate phone|
|`Kotwa Bazar, Gaya – 824220`|Your address        |
|`Mon–Sat: 9AM–8PM`          |Your opening hours  |
|`Satyam Jewellers`          |Your shop name      |

### Replace Images with Real Photos

Each product/catalog card has an `img` property in the JavaScript data arrays. Replace the base64 `data:image/jpeg;base64,...` values with direct `.jpg` URLs:

```js
// In the T.en.cats array, change:
img: "data:image/jpeg;base64,..."
// to:
img: "https://yourcdn.com/your-bangles-photo.jpg"
```

### Add / Remove Products

Find the `prods` array inside `T.en` and `T.hi` in the `<script>` section:

```js
prods: [
  {
    n:   "Product Name",
    ty:  "Product Type",
    img: "data:image/jpeg;base64,...",  // or URL
    c:   "bangles",   // category: bangles | necklaces | earrings | silver | bridal
    p:   "22K",       // purity label
    b:   "New"        // badge (or null for none)
  },
  // ...
]
```

### Change Default Language

In the `<html>` tag at the top of the file:

```html
<html lang="en" data-theme="dark" data-lang="en">
<!-- Change data-lang="en" to data-lang="hi" for Hindi default -->
```

### Change Default Theme

```html
<html lang="en" data-theme="dark" data-lang="en">
<!-- Change data-theme="dark" to data-theme="light" for light mode default -->
```

-----

## 🌍 Browser Support

|Browser             |Support|
|--------------------|-------|
|Chrome 80+          |✅ Full |
|Firefox 75+         |✅ Full |
|Safari 14+          |✅ Full |
|Edge 80+            |✅ Full |
|Mobile Chrome/Safari|✅ Full |

-----

## 📦 Deployment

The file can be deployed anywhere that serves static HTML:

- **Shared Hosting** — upload via FTP, rename to `index.html`
- **GitHub Pages** — push to repo, enable Pages in settings
- **Netlify / Vercel** — drag and drop the file
- **Google Drive** — share publicly, open with Google Docs viewer
- **WhatsApp / Email** — send the file directly; recipients can open in browser

-----

## 📜 Credits

Built with ❤️ for **Satyam Jewellers**, Gaya, Bihar.

- Prop: Late Shri Jitendra Prasad Soni
- Shop brand: **Hans** Satyam Jewellers
- BIS Hallmark No: **91.6 / 750**
- Generated with Claude AI (Anthropic)

-----

*For updates, customisations, or adding real product photos — contact your web developer.*
