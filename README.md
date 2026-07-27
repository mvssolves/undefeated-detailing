# Undefeated Detailing — spec site

Unrequested spec build by [MVS Solves](https://mvssolves.com) for **Undefeated Detailing** (909-205-3009).
Single self-contained `index.html`. No build step. Host anywhere.

## What is verified

Everything on the page traces back to the Google Business Profile (checked 2026-07-27):

| Fact | Source |
|---|---|
| Name, category (car detailing service) | GBP listing |
| Phone `+1 909-205-3009` | GBP listing |
| 5.0 rating from 3 reviews | GBP listing |
| All three reviews, quoted verbatim | GBP reviews (Richard Hung, Hens, West DAWG) |
| "We aim to be undefeated" | Owner's own reply to a review |
| Closes 7 PM | GBP hours line |
| No existing website | GBP shows "Add website" |

## What is NOT verified — owner must confirm before launch

Every item below is marked inline in `index.html` with a `CONFIRM:` comment. Nothing on
the page asserts any of them. Find them all with:

```bash
grep -n "CONFIRM:\|SWAP:" index.html
```

1. **Service area / cities** — map pin sits near Yucca Valley; number is 909. Page says only "909 · Southern California".
2. **Full weekly hours** — only the 7 PM close is known. The status chip computes open/closed from that alone.
3. **Mobile or shop-based** — unknown, so it is claimed nowhere.
4. **Service list** — Interior / Exterior / Full Detail is placeholder structure. No specialties, coatings, turnaround times or guarantees are claimed.
5. **Pricing** — deliberately absent. Every card reads "Quote on the vehicle".
6. **Cal.com booking** — the booking block is a *working preview*, not a live booking. It runs real calendar maths (past days dead, Sundays closed, slots stop before the 7 PM close) so the owner can see exactly how it behaves, and every slot is illustrative. Going live = create the event type on Cal.com and swap this block for the embed snippet; nothing else on the page changes. Needs: account, event types, real availability, buffers, deposit rules.
7. **Social profiles** — omitted entirely rather than linked to `#`.
8. **Years in business, certifications, insurance, guarantees** — not claimed.
9. **Photography** — all `placehold.co`, marked `SWAP:`. Needs the owner's own before/afters.

## Notes

- Concept: the name is *Undefeated*, so the site is built as a fight record — 3 reviews becomes **3–0, zero losses**, reviews become wins, the owner's own line closes the page.
- Stack: hand-written CSS, **no framework and no JS libraries**. Big Shoulders Display / Archivo / Chivo Mono.
- **Lenis and GSAP were removed deliberately.** Smooth-scroll hijacking made the page feel laggy; native scroll plus IntersectionObserver reveals is smooth and ships ~90KB less JS. Nothing is bound to the scroll event.
- Perf: hero video is 580KB (h264, muted, `playsinline`, poster-first, skipped on Save-Data), all images are lazy-loaded with intrinsic dimensions, lower sections use `content-visibility:auto`. No `backdrop-filter` — it was the other jank source.
- Respects `prefers-reduced-motion` — ticker, reveals and scramble all drop out.
- Sticky call bar on mobile: this is a phone-first local service, the tap-to-call is the conversion.

## Media credits (all licence-free, all placeholder)

| File | Source |
|---|---|
| `video/hero.mp4` | Mixkit clip 47588, trimmed/compressed |
| `img/hero-poster.jpg` | frame from the above |
| `img/ba-before.jpg`, `ba-after.jpg` | Pexels — dirty alloy macro / clean alloy macro, matched framing |
| `img/slab.jpg`, `interior.jpg`, `foam.jpg`, `polish.jpg`, `work-1..5.jpg` | Pexels, colour-graded to the palette |

No third-party brand marks appear in any shot (one candidate was dropped for a visible "Ceramic Pro" logo — that would imply a certification the business has not claimed).

Every one is demo material and the before/after is labelled as such **on the page**. Replace with the owner's own work before launch.
