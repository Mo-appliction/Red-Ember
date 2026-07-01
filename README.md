# The Red Ember — Fine Indian Dining Website

## Tech Stack
- **React 18** — UI framework
- **TypeScript** — Type safety
- **Vite** — Dev server & bundler
- **Tailwind CSS v4** — Styling
- **Framer Motion** — Animations
- **Wouter** — Client-side routing
- **jsPDF** — PDF generation for reservations
- **Lucide React** — Icons
- **@tanstack/react-query** — Data fetching (ready to use)

## Setup & Run

```bash
# 1. Install dependencies
npm install

# 2. Start dev server (opens at http://localhost:5173)
npm run dev

# 3. Build for production
npm run build

# 4. Preview production build
npm run preview
```

## Folder Structure

```
velvet-table/
├── index.html                  ← App entry HTML
├── vite.config.ts              ← Vite + Tailwind config
├── tsconfig.json               ← TypeScript config
├── package.json                ← Dependencies
└── src/
    ├── main.tsx                ← ReactDOM render
    ├── App.tsx                 ← Root component + router
    ├── index.css               ← Global styles, theme colors, fonts
    ├── assets/
    │   ├── hero.webp           ← Hero section background image
    │   └── menu-bg.mp4         ← Menu section background video
    ├── context/
    │   └── CartContext.tsx     ← Cart state (add/remove/clear items)
    ├── components/
    │   ├── Navbar.tsx          ← Fixed navbar with scroll effect
    │   ├── Hero.tsx            ← Full-screen hero + gold particle animation
    │   ├── About.tsx           ← Restaurant story + stats
    │   ├── Menu.tsx            ← Tabbed menu (Quarter/Half/Full sizes)
    │   ├── Experience.tsx      ← Features grid + private dining
    │   ├── Gallery.tsx         ← Photo grid with lightbox
    │   ├── Testimonials.tsx    ← Press quotes carousel
    │   ├── Reservation.tsx     ← Booking form → PDF + WhatsApp
    │   ├── Footer.tsx          ← Contact, hours, social links
    │   ├── FloatingCart.tsx    ← Floating bag + slide drawer
    │   └── ui/                 ← shadcn/ui component library
    ├── hooks/
    │   ├── use-mobile.tsx      ← Mobile breakpoint hook
    │   └── use-toast.ts        ← Toast notification hook
    ├── lib/
    │   └── utils.ts            ← cn() utility (class merging)
    └── pages/
        └── not-found.tsx       ← 404 page
```

## Key Customization Points

| What to change | File |
|---|---|
| Restaurant name, address, phone | `src/components/Footer.tsx`, `src/components/Reservation.tsx` |
| WhatsApp number | `src/components/Reservation.tsx` (line: `WHATSAPP_NUMBER`) and `src/components/FloatingCart.tsx` (line: `OWNER_WHATSAPP`) |
| Menu items & prices | `src/components/Menu.tsx` (the `MENU_DATA` array) |
| Colors & fonts | `src/index.css` (CSS variables under `:root`) |
| Hero image | Replace `src/assets/hero.webp` |
| Menu background video | Replace `src/assets/menu-bg.mp4` |
| Gallery photos | `src/components/Gallery.tsx` (the `galleryItems` array — Unsplash URLs) |
| Testimonials / press quotes | `src/components/Testimonials.tsx` |
| Opening hours | `src/components/Footer.tsx` |
