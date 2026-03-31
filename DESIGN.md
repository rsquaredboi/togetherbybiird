# Design System — Together by Biird

## Product Context
- **What this is:** A standalone brand/product landing page for "Together," a couples card game with 180 psychology-backed conversation cards across 6 categories
- **Who it's for:** Couples (all stages) looking to deepen connection, spark conversations, and explore intimacy
- **Space/industry:** Intimacy/wellness products, couples games, relationship tools
- **Project type:** Single-page brand site with product showcase, editorial storytelling, and e-commerce CTA
- **Parent brand:** Biird (biird.co) — Together is a sub-brand with its own visual identity

## Aesthetic Direction
- **Direction:** Playful-Luxury
- **Decoration level:** Intentional (floating gradient orbs for atmosphere, subtle grain, product imagery does the heavy lifting)
- **Mood:** Warm, inviting, intimate without being clinical. Think: a beautiful candle-lit date night, not a sex-ed textbook. The product's colorful illustrations are the star... the design system wraps around them with warmth and breathing room.
- **Reference sites:** biird.co (parent brand DNA)

## Typography
- **Display/Hero:** Playfair Display — serif with italic for emotional moments ("closer", "really", "different"). Creates warmth and sophistication against the geometric sans body.
- **Body:** Space Grotesk — clean geometric sans-serif with excellent weight range (400-700). Readable at all sizes, modern feel.
- **UI/Labels:** Space Grotesk 600-700 — same family, heavier weight for buttons, badges, section labels
- **Data/Tables:** Space Grotesk with tabular-nums — consistent number alignment for pricing, stats, review counts
- **Code:** N/A (no code elements on this site)
- **Loading:** Google Fonts CDN
- **Scale:** 11px (labels) / 13px (small) / 14px (body small) / 16px (body) / 18px (large body) / 22px (card titles) / 40-48px (section headers) / 64-80px (hero headline)

## Color
- **Approach:** Balanced — teal anchors trust, warm tones create intimacy
- **Primary:** #2ab5b2 (Biird teal) — CTAs, links, badges, accent borders, section labels
- **Secondary:** #6b3fa0 (Jouissance purple) — collaboration section, accent cards
- **Warm coral:** #e85c5c — emotional emphasis, italic "really" in headlines
- **Soft pink:** #ff8fab — gradient partner for teal on hero headline "closer"
- **Gold:** #d4a843 — star ratings, trust signals
- **Neutrals:** warm white #ffffff (primary bg), cream #faf7f2 (alternating sections), #1a1a1a (dark CTA/footer blocks)
- **Semantic:** success #2ab5b2, warning #d4a843, error #e85c5c, info #6b3fa0
- **Dark mode:** Dark CTA section and footer use #0a0a0a with teal glow orbs — creates a "nighttime" bookend that mirrors the product's use case

## Spacing
- **Base unit:** 8px
- **Density:** Comfortable — generous breathing room, this is an editorial experience not a data app
- **Scale:** 2xs(2) xs(4) sm(8) md(16) lg(24) xl(32) 2xl(48) 3xl(64) 4xl(80) 5xl(120)

## Layout
- **Approach:** Creative-editorial
- **Grid:** Full-bleed sections alternating with max-width 1200px contained sections
- **Max content width:** 1200px (showcase grid), 1100px (card grids), 800px (FAQ list), 540px (hero text)
- **Border radius:** sm: 8px, md: 16px, lg: 20px, full: 50px (buttons/badges)
- **Section pattern:** Light bg → dark contrast → light → purple collab → light → dark CTA → dark footer

## Motion
- **Approach:** Expressive — the page should feel alive
- **Floating orbs:** 8s ease-in-out infinite float animation, blur(100px), subtle color gradients
- **Scroll reveal:** 0.8s ease fade-up with staggered delays (0.1s, 0.2s, 0.3s) via IntersectionObserver
- **Hero entrance:** Sequential fadeUp animations (0.8s ease) with staggered delays for badge, h1, subtitle, CTAs, proof, product image
- **Marquee:** 25s linear infinite horizontal scroll for announcement bar
- **Testimonial carousel:** 30s linear infinite horizontal scroll with duplicated cards for seamless loop
- **Hover effects:** translateY(-2px) + glow shadow on CTAs, translateY(-6px) + border highlight on cards, scale(1.02) rotate(-0.5deg) on product image
- **Sticky bar:** translateY(100%) → translateY(0) with 0.3s ease, triggered by hero leaving viewport
- **Category cards:** Animated top border scaleX(0→1) on hover using CSS custom properties for per-card colors
- **Easing:** enter(ease-out) exit(ease-in) move(ease-in-out)
- **Duration:** micro(50-100ms) short(150-250ms) medium(250-400ms) long(400-800ms) continuous(8-30s)

## Key Design Risks (deliberate departures)
1. **Gradient text on hero headline** — teal-to-pink on "closer" via -webkit-background-clip. Most product sites use flat color. This creates an emotional, premium feel.
2. **Floating gradient orbs** — animated decorative elements in hero and CTA sections. Most sites are static. This adds atmosphere without overwhelming the content.
3. **Dark cinematic CTA/footer** — breaks from the light, airy body to create a "nighttime" feeling that matches the product's use case (date night). Creates a satisfying emotional arc.

## Decisions Log
| Date | Decision | Rationale |
|------|----------|-----------|
| 2026-03-31 | Initial design system created | Created by /design-consultation. Sub-brand of Biird with own identity — Playful-Luxury aesthetic, Playfair Display + Space Grotesk type stack, teal-anchored palette with warm coral and pink accents. |
| 2026-03-31 | Chose light mode as default | Dark mode version was too heavy for an intimacy/couples product — the content (colorful card illustrations) needs a light backdrop to pop. Dark reserved for CTA/footer contrast sections only. |
| 2026-03-31 | Expressive motion selected | Product is experiential (date night card game), so the page itself should feel like an experience — floating orbs, scroll reveals, auto-scrolling testimonials, hover animations. |
