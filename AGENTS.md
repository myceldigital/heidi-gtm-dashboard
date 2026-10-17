# AGENTS.md — Heidi GTM Dashboard

Standing instruction for any agent/human working on this project. `index.html` (repo root) is the only canonical dashboard file — never keep a second HTML copy.

## Target
World-leading, elite-level, single-file HTML dashboard. Minimal, highly efficient code: no bloat, no dead code, no unnecessary dependencies. Keep it self-contained unless a change clearly pays for itself.

## UX / UI
- Mobile-first, fully optimised for every screen: small phone → tablet → laptop → large/wide desktop.
- Responsive layout, no horizontal scroll, generous touch targets, readable type scale.
- Optimised for fast scanability in GTM / facility-coverage use: search, filters, counts, and map must be obvious at a glance.

## Performance
- Inline critical CSS/JS only where it helps; defer / non-blocking where possible.
- Efficient DOM and Leaflet handling; throttle/debounce search, filter, and map interactions; lazy-load where sensible.
- Aim: instant first paint, smooth filtering/search/map on mid-range phones.
- Keep total file size lean. Flag any change that materially grows size or slows load before doing it.

## Quality bar
- Semantic, accessible markup: labels, visible focus states, sufficient contrast, full keyboard operability.
- Cross-browser, zero console errors, valid HTML.
- Test at 360, 390, 768, 1024, 1440, and 1920 px: verify layout, map, filters, and search at each breakpoint.

## Data integrity
- Facility/GP dataset, contacts, counts, and existing functionality must not be lost, dropped, or silently altered. Any data change must be explicit, stated in the commit, and verifiable against the previous version.

## Process
- Smallest diff that achieves the improvement; preserve working behaviour.
- Commit and push to `main` — GitHub Pages auto-deploys. After pushing, verify https://myceldigital.github.io/heidi-gtm-dashboard/ returns HTTP 200 with title `HEIDI GTM / FACILITY COVERAGE - IRELAND`.
- Source of truth is this folder (`~/Projects/heidi-gtm-dashboard`). The old Cursor AgentStore copy does not sync here.

## Requires Matthew's explicit approval first
- Adding any framework, build tooling, analytics, or trackers.
- Any new external dependency, or breaking the single-file model.
