# Corient OS — Internal SOP

This is the internal reference document for the Corient delivery team. It maps lanes to phases so anyone on the team can look up:

- What activates in each phase
- Who owns each lane
- Which task pack runs
- Which tools are live, and what to add when
- The gates that move a client from one phase to the next
- Retainer pricing per phase

## What it is not

- **Not a sales document.** Don't send it to prospects. Pricing, gates, and tool specifics are commercially sensitive.
- **Not a client-facing page.** This is for Corient operators only.
- **Not deployed publicly.** Lives as a local HTML file or inside the team workspace (Notion, Drive, Slack).

## File

`corient-os.html` — single self-contained HTML. Open in any browser. Fonts load from Google CDN, the logo loads from corient.com.au CDN, so it works anywhere with internet access.

## How to read it

The whole document is a single table plus three small reference blocks. Top to bottom:

1. **Summary reference** — phases, lanes, the three Notion OS layers, key notes.
2. **The matrix** — 9 lane rows × 3 phase columns. Each cell shows status, deliverable, and tools active in that phase.
3. **Phase gates** — concrete criteria to advance Foundation → Base → Expansion.
4. **Retainer pricing** — Foundation $6,000/mo · Base $8,000/mo · Expansion $12,000/mo.

Read down a column to see everything happening in one phase. Read across a row to see one lane's progression across all phases.

## Updating

Edit the HTML directly at `/Users/amberburch/.claude/results/corient/corient-os/corient-os.html`. Common updates:

- **Lane status changes per client** — rare, since the matrix shows the standard progression. For a client-specific overlay, copy the file and tweak.
- **Tool stack changes** — when a new tool gets added or removed from Corient's standard stack, update the relevant cell.
- **Pricing changes** — update the retainer cells.
- **Gate criteria changes** — update the gate column lists.

## Distribution

- Drop a copy in the Corient team Notion workspace alongside the rest of the OS docs
- Share the file via Drive or Slack when a team member needs it offline
- Print-friendly: A3 landscape renders the full matrix on one page (`@page` rules already configured)

## History

The previous version of this file was a client-facing sales document deployed at `amberatorala.github.io/corient-os` (now private, Pages disabled). Goal pivoted on 2026-05-05 to internal SOP. The local git history at `~/Claude/Projects/corient-os/.git` retains the deployed sales version at commit `06e07da` if rollback is ever needed.
