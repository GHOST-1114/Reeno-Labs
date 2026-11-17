# Reeno Labs Website — Plan

## Product and implementation

Build a polished, responsive, public-facing one-page website for Reeno Labs with anchor navigation, hero, services, package comparison, project portfolio, about, contact form, and footer. Preserve the user's exact package names, prices, feature lists, delivery estimate, CTA labels, contact details, legal/accuracy constraints, and the specified messaging. All four offerings link to their dedicated detail content on the same page.

Use Astro with static output so the actual landing-page copy, package details, page metadata, and navigation are present in the initial HTML for crawlability. Use lightweight browser JavaScript only where interaction requires it: responsive menu, reveal/scroll behavior, contact form validation and submission choices, and prefilled WhatsApp/mailto links. Keep reduced-motion support and keyboard access. Use no database or server integration: none is needed for the public static content, and no email delivery service or credentials are configured. Email selection will launch the visitor's email application with a completed `mailto:` draft addressed to `amaannhuh@gmail.com`; the site must explain that the visitor sends it from their email app, and must not claim delivery. WhatsApp selection will open `https://wa.me/923182913073` with a URL-encoded draft for visitor review and sending. Offer both options when “Either” is selected. If genuine server-side email delivery is added later, it will require a configured email provider and protected credentials; do not simulate this now.

The portfolio includes the user-requested Asli Leather live storefront reference at `https://asileather.com/`, using the supplied homepage screenshot and describing the store as selling original leather products with a broad wallet range. Link to the store, label it as a live store reference, and do not imply it is Reeno Labs client work unless that relationship is confirmed. The Identity direction will feature the user-supplied KT&CO logo and a restrained black/charcoal/white palette as a logo-led identity study; do not invent KT&CO's business sector or unprovided brand claims. Do not invent testimonials, results, awards, statistics, social URLs, or unsupported payment-gateway claims. Budget and optional contact fields will be included only when provided in prepared messages. Add basic page metadata, semantic HTML, visible focus states, contrast, direct email and WhatsApp links, and the required static route manifest.

Replace the “Small business site” portfolio sample with the supplied Library Desk live-portal reference at `https://app-meqd.vercel.app`. Identify Library Desk as a role-based library management system and portal for schools, colleges, and institutions. Present its supplied React/Vite frontend and Python backend; dedicated librarian, student, and teacher portals; 3-book student and 5-book teacher limits with automated due dates; Rs. 10/day overdue fine calculation on returns; patron-submitted active-loan return requests for desk handover; dashboard metrics for total books, active issues, pending returns, and collected fines; and serverless multi-service deployment architecture. Make the live-app link accessible and open a new tab. Use a clearly illustrative interface visual (not a screenshot or claimed client result), and make no unsupported ownership, client, or Reeno Labs authorship claim.

The KT&CO Identity card's “View slides” arrow will open the user-supplied eight-slide strategy deck as a browser-viewable PDF in a new tab, rather than a decorative arrow or a PowerPoint download.

## Project structure

- `src/pages/index.astro` — statically rendered page composition and SEO metadata.
- `src/components/` — reusable header/navigation, hero, service cards, pricing cards, portfolio cards, about, contact form/panel, and footer.
- `src/data/services.ts` — authoritative package prices, feature lists, service labels and CTA copy shared by service/pricing sections.
- `src/scripts/site.ts` — compact browser behavior for navigation, motion preferences, validation, and email/WhatsApp draft preparation.
- `src/styles/global.css` — tokens, responsive layout, component styling, hover/focus states, and reduced-motion rules.
- `public/images/` — responsive Asli Leather WebP previews and the trimmed supplied KT&CO wordmark; the Reeno Labs hero artwork remains in project storage.
- `public/decks/ktco-brand-identity-ecommerce-strategy.pdf` — browser-readable copy of the supplied KT&CO slide deck, opened by the portfolio arrow.
- `public/manus-routes.json` — route manifest declaring the single public page.
- `public/favicon.svg` — small Reeno Labs brand mark.
- `astro.config.mjs`, `package.json`, `pnpm-lock.yaml`, `pnpm-workspace.yaml`, `tsconfig.json` — pinned static build/toolchain and explicit dependency lifecycle policy.
- `app.config.ts` — project logo URL metadata required by the website checkpoint workflow.

The static build output is `dist/`; the local preview server listens on the already-configured port 3000. No runtime server or database capability is required. Configure the matching static build declaration after implementation and retain the platform's existing runtime port/diagnostics settings.

For the mobile/performance update, preserve the static Astro architecture and avoid new runtime dependencies. Refine narrow-phone spacing and type sizing while retaining the existing tablet/desktop composition; optimize the oversized supplied store screenshot into responsive WebP variants, trim the logo's blank canvas without cropping the mark, add intrinsic dimensions where available, keep below-the-fold portfolio images lazy, and retain high priority for the hero visual.

## Design direction

### Design movement

A restrained contemporary Swiss/editorial digital studio aesthetic, using asymmetry, oversized typography, precise grids, and tactile technical details.

### Core principles

- Editorial clarity: generous space, strong type hierarchy, concise and specific copy.
- Designed restraint: charcoal and warm off-white carry most surfaces; lime is reserved for action and navigational cues.
- Crafted utility: package comparisons, anchors, and form labels prioritize legibility and real decisions.
- Quiet motion: reveal and hover effects add feedback without becoming a spectacle.

### Color philosophy

Deep charcoal signals technical confidence, warm off-white softens the page, and one electric acid-lime accent makes key actions and Reeno Labs' identity instantly recognizable. Secondary grays are for hierarchy, not decoration.

### Layout paradigm

An editorial long-scroll composition that alternates a split, oversized hero with left-aligned section introductions and carefully composed service/project groupings. Use deliberate offsets and full-bleed dark/light transitions rather than centering every section in identical card grids. Keep the comparison section compact and the contact area calm and direct.

### Signature elements

- A compact custom monogram formed from two offset geometric “R”/signal strokes, paired with the Reeno Labs wordmark.
- A modular, dimensional abstract hero visual: luminous lime signal lines/orbit traces over a deep matte field, generated as an original artwork and used only in the hero.
- Small uppercase mono labels and precise ruled dividers to give the editorial system a technical rhythm.

### Interaction philosophy and animation

Interactions should make navigation and decision-making feel direct. Menu controls expose real navigation; service calls-to-action scroll to the relevant package or contact form and preselect the matching service; the contact method choice launches only the selected draft channel. Hover/focus states use contrast and small positional shifts. Use short opacity/translation reveals with an intersection observer, do not hide essential content when scripts are unavailable, and disable/reduce motion when the user requests it.

### Typography system

Use a contemporary grotesk sans-serif for headings and body copy, with a system-safe fallback stack to avoid blocking first paint. Pair it with a restrained monospace face for small metadata/eyebrows. Oversized hero heading, medium-weight section headings, readable 16–18px body text, compact mono labels, and tabular/lining numerals for PKR ranges.

### Brand essence

A thoughtful digital partner for businesses that need a sharper, more useful online presence; distinctive, practical, dependable.

### Brand voice

Direct, warm, and specific. Headlines name the value plainly; CTA labels say exactly what happens. Example lines: “Digital experiences built to move your business forward.” and “Have a project in mind? Tell us what you’re planning, and let’s explore how Reeno Labs can bring it to life.”

### Wordmark and logo

A custom geometric signal/R monogram sits beside “Reeno Labs” in a clean, individually tuned wordmark lockup; create a small SVG site favicon and a square mark asset for project branding metadata.

### Signature brand color

Electric chartreuse / acid lime, used as a tightly controlled call-to-action and identity accent.
