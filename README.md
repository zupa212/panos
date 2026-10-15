# PANOS — Private Crewed Superyacht Charters

An ultra-luxury, cinematic landing page for **PANOS** private crewed superyacht charters across the Mediterranean and the Indian Ocean.

Built as a single, self-contained landing page (`index.html`) with zero external frameworks, zero build steps, and native CSS/JS scroll mechanics.

---

## Highlights & Architecture

- **Cinematic Golden-Hour Backdrop:**
  Positioned `fixed` full-bleed at `z-index: 0` with a 3-way gradient scrim that preserves the yacht hull untouched in the center frame while providing contrast for typography.
- **Vertical Film Snapping (`scroll-snap-type: y mandatory`):**
  Each of the first four screens acts as a dedicated 100vh cinema frame that locks crisply into place with `scroll-snap-stop: always`.
- **Dual Playback Engine (Loop & Scrub):**
  - **Loop Mode:** Continuous autoplay background video with graceful pointerdown unlock.
  - **Scrub Mode:** Direct scroll synchronization across the first four film screens (`progress = scrollY / (innerHeight * 3)`).
  - **Interactive Mode Switcher:** Dedicated frosted glass control in the fixed header to toggle between Loop and Scrub dynamically without page reload.
- **Native CSS Scroll-Driven Animations:**
  Powered by `@supports (animation-timeline: view())` with progressive fallback for browsers without scroll timelines.
- **Editorial Typography & Luxe Aesthetic:**
  Cormorant Garamond display serif paired with Manrope grotesque body copy, frosted glass capsules, hairline borders, and warm golden accents (`#C9A96E`).

---

## Quick Start

You can open `index.html` directly in any modern browser, or run the included streaming server:

```bash
# Run local streaming server with HTTP 206 Partial Content support:
node server.js
```

Then visit:
- **Loop Mode:** [http://localhost:8080/](http://localhost:8080/)
- **Scrub Mode:** [http://localhost:8080/?mode=scrub](http://localhost:8080/?mode=scrub)

---

## License

© 2026 Panos Yacht Charters. All rights reserved.
