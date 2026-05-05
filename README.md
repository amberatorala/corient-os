# Corient OS — Per-Client Cloning Guide

The single-page HTML at `corient-os.html` is the strategic Corient OS document. One file, every section. Cloning it for a client is two attribute changes and (optionally) some copy edits.

## Quick start

1. Duplicate `corient-os.html` into a per-client folder (e.g. `clients/acme/corient-os.html`).
2. Open the file. Find the `<body>` tag near the top:

```html
<body data-stage="foundation" data-view="team" data-client="Client Name">
```

3. Set the three attributes:

| Attribute | Values | What it controls |
|---|---|---|
| `data-stage` | `foundation` \| `base` \| `expansion` | Which phase block glows + which sequence dots are lit. Dim other phases to 55% so the active one stands out. |
| `data-view` | `team` \| `client` | Tightens or relaxes copy density. Team view shows tool-cost rows, optional tools, deeper task pack detail. Client view hides them. |
| `data-client` | Free text | The client name shown in the topbar chip. |

4. Save. Open in any browser. That's it.

## What changes between team and client views

| Element | `data-view="team"` | `data-view="client"` |
|---|---|---|
| Phase tools — optional adds (Hotjar, Mutiny, GHL pipeline detail) | Visible | Hidden |
| Stack cost-per-phase strip ($0–50, $650, $500) | Visible | Hidden |
| Reasoning rationale on tool gap calls | Visible | Hidden |

To add more team-only or client-only elements, use the existing CSS classes:

```html
<span class="team-only">Team-only detail.</span>
<span class="client-only">Client-only framing.</span>
```

## Copy edits

The default copy is the conviction draft. Per-client edits live in the HTML directly — find and replace, or open in any editor:

- **Hero subtitle** — usually unchanged.
- **Phase posture sentences** — sometimes tweaked per client (e.g. e-commerce vs SaaS).
- **Lane outcomes inside phase blocks** — the place to swap defaults if the client's path deviates.
- **KPIs and gates** — refine numbers if the client has clearer baselines.
- **Photoreal AI section** — swap in client-specific cost savings if comparison data exists.
- **Offer library** — usually unchanged (it's the menu, not the chosen offer).

## Brand assets

The hero topbar and footer reference the Corient white wordmark via CDN:
`https://www.corient.com.au/wp-content/uploads/2025/08/white-logo-1-1.webp`

For offline reliability, save the four brand-kit logo variants locally to `/Users/amberburch/.claude/reference/clients/corient/brand/` and update the `<img>` tags. The four variants are:

- Mark only on black (white mark)
- Mark only on light (black mark)
- Wordmark on light (black "corient" with mark)
- Wordmark on dark with ultramarine ambient glow ← used in hero topbar

## Verifying

After cloning, scroll the document end-to-end and check:

1. The active phase glows; the other two are dimmed to ~55%.
2. The sequence rail at the top of the timeline section fills to the right level (33%, 66%, 100%).
3. The stage chip in the topbar shows the right phase.
4. The client name appears in the topbar chip.
5. Resize the window to mobile width — the matrix collapses, the orb scales, copy stays readable.
6. Read every line aloud. Anything that sounds like AI filler, kill it.

## When something feels wrong

The doc fails the "stranger test" if a reader can't answer these in 3 minutes:

- What phase is the client in?
- What lanes are active?
- What tools come next?
- Why 3+ months minimum?
- What does Corient explicitly *not* do?

If any answer is unclear, the section needs sharpening.

## Voice rules

- Direct.
- No corporate filler.
- No em-dashes.
- Australian English throughout.
- Read aloud before shipping.
