# Cozy Brew — Artisan Coffee Shop Website

Welcome to the Cozy Brew website project — a modern, interactive multi-page site built with Tailwind CSS classes, progressive enhancements, and delightful micro-interactions. This repository is a lightweight static site served by a minimal Express server for easy local development and deployment to Render.

Project structure

my-project/
├── public/
│   ├── index.html          # Main landing page
│   ├── about.html          # About / story page
│   └── contact.html        # Contact & visit page
├── server/
│   └── index.js            # Minimal Express server to serve public/
├── package.json           # Dependencies and scripts
├── render.yaml            # Render.com deployment config
└── README.md              # This file

Key features

- Full-width, fluid layout that fills the viewport on all devices (uses full-bleed containers and w-full classes).
- Tailwind CSS utility classes used directly in HTML via CDN for rapid prototyping.
- Google Fonts integrated: Playfair Display (headings) and Inter (body) — each HTML file includes a comment at the top indicating the fonts.
- Design trends included: glassmorphism, gradient accents, parallax hero background, subtle micro-animations, and dark-mode support.
- Interactive elements: modal order form, image lightbox, FAQ accordions, newsletter and contact forms with validation, loyalty progress bar, and gallery with lazy-loading.
- Accessibility: ARIA labels for form elements, keyboard-friendly interactions (Enter to open images, Escape to close modals), visible focus styles.
- SEO and social meta tags added on the main page.

Local setup

1. Install dependencies:

   npm install

2. Run locally:

   npm start

   - The site will be available at http://localhost:3000
   - For development with auto-reload, use: npm run dev (requires nodemon)

Deployment (Render)

This repository includes render.yaml configured for a Node web service. To deploy:

1. Push the repo to GitHub.
2. Create a new Web Service on Render and connect to the repository branch (default `main`).
3. Render will run `npm install` and `npm start` as defined in render.yaml.

Customization notes

- Images: The HTML uses placeholder tags of the format `https://images.unsplash.com/photo-1634400414538-d3c0fc2bc63b?crop=entropy&cs=tinysrgb&fit=max&fm=jpg&ixid=M3w3ODkyNDZ8MHwxfHNlYXJjaHw3fHxkZXNjcmlwdGlvbnxlbnwwfDB8fHwxNzU1MzQ2MDU2fDA&ixlib=rb-4.1.0&q=80&w=1080`. When integrated into a pipeline that supports automatic image fetching, these will be replaced by high-quality images from stock sources. You can also replace those placeholders with your own image paths or base64 data URIs (especially if you have user-uploaded images).
- Fonts: Comments at the top of each HTML file indicate which Google Fonts are used. The files also include Google Fonts links for immediate use.
- Tailwind: For production, replace the CDN usage with a local Tailwind build (recommended) for better performance and purge capabilities.

Extending the site

- Add an orders API in server/index.js to process reservation and order requests.
- Hook forms to a transactional email provider (SendGrid, Mailgun) or a database for leads and reservations.
- Add an authenticated admin dashboard for menu management, events, and loyalty tracking.

Design & Content approach

The copy and structure are crafted to highlight the coffee shop's strengths: handcrafted roasts, community events, and a cozy in-store experience. CTAs encourage discovery (Explore Menu) and conversion (Order Now / Reserve). Social proof appears as testimonials and trust cues, and the loyalty progress bar creates a gamified nudge to return.

Accessibility & Performance

- Progressive enhancement strategies are used: functional forms even without JavaScript, lazy-loaded images, and reduced motion support via CSS transitions.
- Use Lighthouse to evaluate performance and accessibility and tweak further (compress images, use server-side rendering for heavy SEO pages, etc.).

Contact

If you need help customizing the site, adding integrations (POS, payment, subscriptions), or building a CMS for content editors, reach out with your requirements and assets.

Enjoy brewing something beautiful!

— Cozy Brew Web Team
