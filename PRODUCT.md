# Undefeated Detailing — PRODUCT.md

**Register:** brand (marketing site — the design *is* the product)

## What this is
A single-page site for **Undefeated Detailing**, an auto detailing business in Southern
California (909). Built by MVS Solves as an unrequested spec drop: the owner has a
perfect Google rating and no website at all. The site is the pitch.

## Who it's for
**Everyday drivers** — family cars, work trucks, commuters — not the show-car
enthusiast crowd. `CONFIRM:` the owner has never stated his target customer; this is
the likeliest read for a 909 detailer and is flagged in the markup.

Visitors arrive from a phone, from Google, having just seen a 5.0 rating. They want to
know: is this guy real, is he good, how do I reach him. In that order.

## The one job
Get a phone call. Everything else on the page exists to make that call feel safe.

## Voice
Plain and confident. The owner's own words are the reference — his reply to a review
reads *"We aim to be undefeated!"*. Warm, direct, a little proud. No jargon, no
"elevate your vehicle", no packages with names like Platinum.

## Hard constraints
Only claims verifiable from the Google Business Profile may appear. Everything else is
marked `CONFIRM:` in the markup and claimed nowhere. Full list at the top of index.html.
Currently unverified: service area, weekly hours, mobile vs shop, service list, pricing,
process, socials, years in business, certifications.

## Media reality
Stock imagery now; the owner's own **phone photos** after the drop. Layouts must
survive messy, badly-lit, vertical source material — fixed aspect boxes with
`object-fit: cover`, never a layout that needs a cinematic 16:9 crop to work.

## Non-goals
- Not an e-commerce or package-picker site — pricing is per-vehicle, by phone.
- No accounts, no quoting engine.
- Booking is a **preview** of a future Cal.com embed, not a live booking system.
