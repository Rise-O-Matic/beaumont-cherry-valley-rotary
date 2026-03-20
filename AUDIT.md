# Beaumont-Cherry Valley Rotary Website Audit

**Date:** 2026-03-20
**URL:** https://beaumontrotary.com/
**Platform:** GoDaddy Website Builder 8.0
**Auditor:** Claude (Design + SEO)

---

## Executive Summary

The current site is a single-page GoDaddy Website Builder site with **critical structural, SEO, and design problems**. It functions as a vertical scroll of photo galleries and text blocks with no real navigation, no event system, and no clear calls to action. The biggest issue: **events are posted as JPEG flyers** with zero searchable text, zero accessibility, and zero SEO value.

**Overall Grade: D-**

---

## 1. Information Architecture — F

| Problem | Detail |
|---------|--------|
| **Single page, no routing** | Everything lives on one 14,400px tall page. No `/events`, `/about`, `/contact`, `/join` pages. |
| **Navigation is broken** | Nav contains only "Home" and a "More" dropdown with nothing in it. Every link points to `/`. |
| **No content hierarchy** | 12 sections dumped vertically with no logical grouping. Photo galleries for past events are mixed with current info. |
| **No event system** | Events are JPEG flyer images. No dates, no descriptions, no RSVP links, no calendar integration. |
| **Stale content mixed with current** | 53rd AND 54th Senior Thanksgiving Luncheon both displayed. Past Casino Night event still prominent. No way to tell what's upcoming vs. archived. |

## 2. SEO — F

| Signal | Status |
|--------|--------|
| **Meta description** | MISSING — completely absent |
| **Canonical URL** | Not set |
| **Structured data (JSON-LD)** | 1 block (likely GoDaddy default, not custom) |
| **Open Graph** | Title only — no description, no image |
| **Heading hierarchy** | Broken: 2 h1s (both same text repeated 4x each = 8 visible h1-level headings), 12 h2s with duplicate text |
| **Image alt text** | 12 of 120 images missing alt entirely; the rest likely have auto-generated or generic alt text |
| **Sitemap** | None detected |
| **robots.txt** | Not checked but unlikely configured |
| **Page speed** | 120 images on a single page, no lazy loading visible, GoDaddy builder overhead |
| **Local SEO** | No Google Business integration, no LocalBusiness schema, no NAP consistency |
| **Event markup** | Zero — events are JPEGs so Google can't index them at all |

### SEO Killer: JPEG Events
Events posted as flyer images mean:
- Google cannot read or index event details
- Screen readers cannot access event info
- Mobile users can't copy dates/locations
- No rich snippets in search results
- No calendar integration possible
- QR codes on flyers don't translate to web

## 3. Design & UX — D

| Problem | Detail |
|---------|--------|
| **No visual identity** | No logo visible, no consistent color palette, no brand typography |
| **GoDaddy template aesthetics** | Generic builder look with default spacing, fonts, and section dividers |
| **Photo gallery overload** | 5 separate carousels with 100+ photos total. No curation, no context, no captions |
| **Wall of text** | The "About" and "History of Rotary" sections are long unformatted paragraphs |
| **"Get Involved" CTA goes to homepage** | The primary call-to-action button links to `/` — the page you're already on |
| **Contact info buried at bottom** | Phone numbers and emails at the very bottom of a 14,000px page |
| **No responsive design audit done** | GoDaddy builder responsive is typically mediocre |
| **Duplicated headings** | Every heading appears 2-4 times in the DOM (likely responsive variants all rendered) |

## 4. Accessibility — D

- 12 images with no alt text
- Heading hierarchy is nonsensical (duplicate h1s, skipped levels)
- Color contrast not audited but GoDaddy defaults are often poor
- No skip-to-content link
- No ARIA landmarks beyond GoDaddy defaults
- Event info locked in images = completely inaccessible

## 5. Performance — D

- **120 images** on a single page
- No visible lazy loading
- GoDaddy builder JS overhead
- No CDN optimization beyond GoDaddy default
- Single monolithic page = everything loads at once

## 6. Content Inventory

| Section | Type | Status |
|---------|------|--------|
| Hero | Banner + CTA | CTA broken (links to self) |
| Annual Fundraising Event | Text + JPEG flyer | Event likely past, still prominent |
| 54th Senior Thanksgiving Luncheon | Photo gallery (23 imgs) | Nov 2025 — past event |
| Student Support May 2025 | Section header only | Past, minimal content |
| About / Rotary History | Long text blocks | Generic Rotary boilerplate + club info |
| Club Activities | Text list | Useful but unstyled |
| History of Rotary / Paul Harris | Long biography | Not club-specific, very long |
| Interact Club | Text | Good content, buried |
| Photo Gallery of Our Work | Carousel (57 imgs) | No context or captions |
| Interact Club in Action | Carousel (18 imgs) | No context |
| Casino Night 2025 | Carousel (19 imgs) | Past event |
| 53rd Thanksgiving Luncheon | Carousel (49 imgs) | Past event (2024!) |
| Board of Directors | Text list | Current 2025/2026 |
| Partners | Single logo | Only Beaumont Chamber |
| Contact | Text + emails | Buried at bottom |

---

## Recommendations

1. **Move off GoDaddy Builder** — it's the ceiling on everything
2. **Build a real multi-page site** with proper routing: Home, Events, About, Gallery, Contact/Join
3. **Create a structured event system** — HTML events with dates, descriptions, locations, schema markup
4. **Implement proper SEO** — meta tags, structured data, sitemap, local business schema
5. **Curate photo galleries** — 10-15 best photos per event, with captions
6. **Design a real brand identity** — colors, typography, logo treatment
7. **Make "Join/Get Involved" the primary CTA** — with a real destination
8. **Add meeting info prominently** — when, where, how to attend
