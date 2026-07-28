# Undefeated Detailing — DESIGN.md

## Scene
A phone, one-handed, outdoors, mid-afternoon glare, standing next to a car that needs
doing. Bright ambient light. That forces a **light-dominant page** — a dark site is a
mirror in sunlight — with dark sections used as punctuation, not as the base.

## Colour strategy: committed, two colours
Two brand colours, complementary, both pulled well back from full saturation. No third
accent, ever.

| Token | Value | Role |
|---|---|---|
| `--petrol` | `oklch(0.28 0.045 205)` ≈ `#12333A` | The brand colour. Dark sections, headings on light, primary buttons. |
| `--copper` | `oklch(0.58 0.11 45)` ≈ `#A8613C` | The single accent. Links, active states, the one thing your eye lands on. |
| `--shell` | `oklch(0.96 0.004 205)` ≈ `#F1F3F3` | Page base. Chroma leans to petrol, **not** warm — no cream/sand. |
| `--ink` | `oklch(0.20 0.02 205)` ≈ `#131B1D` | Body text on light. |

Teal ↔ orange is complementary, and both are automotive-native (petrol, oxidised
copper) rather than the "premium small business" defaults. Deliberately **not**: gold on
black (tacky template), electric blue (oversaturated), red (Nathan's site).

## Type
- **Bricolage Grotesque** 600/800 — display only. Real character, not on the overused list.
- **Archivo** 400/500/600 — body. Different construction, so it pairs on a contrast axis.
- Display ceiling **96px**. Letter-spacing floor **-0.03em**. `text-wrap: balance` on headings.
- Body measure capped at 68ch.

## The signature move — the wipe hero
The hero photo sits under a layer of grime on a `<canvas>`. Dragging across it wipes the
grime away and the clean car appears underneath. It auto-demos one stroke on load so the
affordance is obvious, and on touch it wipes on tap-drag.

This is the whole business as one interaction, and no other category can use it. It
replaces the stock hero video, which was a stranger's footage fronting someone's
business — the weakest thing on the page.

Reduced motion: the canvas starts fully cleared, no demo stroke, no loss of content.

## Section cadence — no eyebrow scaffold
Explicitly **not** a tracked uppercase kicker above every section. Cadence instead:
- Section intent carried by the heading itself.
- One numbered sequence on the page — the four process steps — because that is a real
  ordered sequence, not decoration.
- Section transitions carried by the surface flip (shell → petrol) rather than labels.

## Motion
Ease-out quint (`cubic-bezier(.22,1,.36,1)`). No bounce, no elastic. Reveals enhance
already-visible content — content is never gated behind a class, so a headless render or
a paused tab still ships a complete page. Everything has a reduced-motion path.

## Bans honoured
No gradient text, no glassmorphism, no side-stripe borders, no hero-metric template,
no coloured glow shadows, no identical card grids, no eyebrow on every section.
