# Chief Media website redesign — plan + implementation

**Owner:** Eisenhower (design architecture)  
**Coord:** Disney (motion/visual assets — CSS-only v1; motion optional later) · Patton (deploy drill if needed) · Chief (go-live)  
**Spend:** $0 (static HTML + existing brand exports + GitHub Pages)  
**Date:** 2026-09-28

## Situation (before)

| Item | State |
|------|--------|
| Live hosts | `https://myersonthemap.com/` · mirror `https://agentchief66.github.io/` |
| Product | **Chief Hunt** freelance buying-research landing |
| Visual | Generic dark freelance sales page; no Chief Media chrome |
| Identity | Heavy personal/legal naming in meta + footer (invoice honesty for Hunt) |
| Source | `/workspace/chief-hq/product/` |

## Goals

1. Pivot homepage to **Chief Media** media machine (Host Doc · Co-host Chief).  
2. Match brand kit: red `#E31B23` / black `#050505` / white — high contrast, mobile-first, large taps.  
3. Preserve Hunt as secondary path (don’t strand existing customers).  
4. No spend; no new SaaS.

## Information architecture (after)

```
/                 → Chief Media home (hero, watch, series, hosts, about)
/hunt.html        → Chief Hunt legacy offers + samples links
/sample-*.html    → unchanged research samples (linked from Hunt)
/assets/brand/*   → logo mark, cohost lockup, SVG
```

**Primary nav:** Watch · Series · Hosts · Start watching  
**Footer:** Watch · Series · Chief Hunt · Email

## Visual / UX system

- Surface A chrome only on site shell (per `CREATIVE-ELITE-PLAN/01-DESIGN-ARCHITECTURE.md`).  
- Series chips use Surface B steel/cream for content flavor without recoloring the mark.  
- Sticky header, skip link, focus rings, ≥48px tap targets, single-column → two-column from 560px.  
- Hero: mark + “Clear education. No fluff.” + Host Doc · Co-host Chief.  
- Motion v1: none (Disney may add subtle mark idle later — optional).

## Copy rules

- Public chrome: **Chief Media**, **Doc**, **Chief** only.  
- Hunt page may keep invoice/legal honesty for payments (separate product).  
- Homepage meta/OG: no personal legal IDs.

## Implementation status (this box)

| File | Status |
|------|--------|
| `index.html` | **Rewritten** — Chief Media home |
| `hunt.html` | Hunt landing + top banner to media home |
| `index.hunt-legacy.html` | Full backup of pre-rebrand home |
| `assets/brand/*` | Copied from `production/brand-chief-media/exports/` |
| Samples | Unchanged |

## Deploy ($0)

Working tree is ready under `/workspace/chief-hq/product/`.  
Live publish = sync to `agentchief66/agentchief66.github.io` **master** (and custom domain myersonthemap.com already pointed).

**Go-live needs Chief confirm** (live traffic change). Suggested:

```bash
# from authed agentchief66 box — after Chief GO
# clone/pull github.io, copy product files, commit, push master
```

## Verify checklist

- [ ] Mobile 375px: hero + nav usable; taps ≥48px  
- [ ] Mark circle-crops clean in header  
- [ ] `/` = Media; `/hunt.html` = Hunt with banner  
- [ ] No banned IDs on homepage HTML  
- [ ] Lighthouse-ish: contrast AA on body text  
- [ ] OG image resolves after deploy  

## Disney ask (optional follow-on)

- Subtle hero mark pulse / idle (CSS or short loop) — keep under 1s, no neon  
- Series card hover micro-motion if they want polish pass  

## Open decisions for Chief

1. Confirm **GO** to push `product/` → `agentchief66.github.io` master.  
2. Exact YT/X/FB/IG profile URLs to hard-wire (placeholders used where uncertain).  
3. Whether Hunt stays on myersonthemap.com forever or moves to `/hunt` subdomain later.
