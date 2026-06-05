# Estancia Cafetera — Makeathon Asset Map
## What we actually need to generate, slot by slot

**Date:** June 5, 2026
**Author:** Julissa Roa
**Status:** Active — guides all Sprint 4.1 generation
**Companion to:** volcanic-hospitality-system.md (strategic brief) · image-direction-v5.md (prompt menu)

---

## 00 · The Operating Principle

**Generate against slots, not against ideas.**

The image-direction-v5.md file is now a *menu* of prompt patterns by category. This asset map is the *order ticket* — what specifically gets generated, for which slot, when.

Total expected generations: **~10-12 unique stills + 1 Weave motion loop.**

Not 40. Not 160. Just what each surface needs.

---

## 01 · Total Inventory by Surface

```
SURFACE                                   IMAGE SLOTS    MOTION SLOTS
──────────────────────────────────────────────────────────────────────
01 · Figma Make Live Site (5 frames)         7-10            0-1
02 · Instagram Grid (9 posts)                 ~4              0
03 · Guest Portal Welcome Screen              1               0
04 · Figma Weave Motion Hero                  0               1
05 · Submission Video                         0 (B-roll)      0
──────────────────────────────────────────────────────────────────────
TOTAL (after reuse dedup)                    ~10-12          1
```

---

## 02 · Surface Detail: Figma Make Live Site

Using the *reframed* 5-frame structure (Hero · Philosophy · Place · Ritual · Stay):

### Frame 01 · HERO
| Slot | Type | Brief | Source | Reuses |
|------|------|-------|--------|--------|
| H1 | Motion OR Still | Architectural anchor (basalt facade / courtyard at golden hour) | Weave loop preferred (see Surface 04); fallback Midjourney still | Stay-S1 if still |
| H2 | SVG | Estancia wordmark with ink-bleed | Existing brand assets | n/a |

### Frame 02 · PHILOSOPHY
| Slot | Type | Brief | Source | Reuses |
|------|------|-------|--------|--------|
| P1 | Still | Material texture — volcanic stone surface detail | Midjourney `01.10` Entry Threshold or new "stone macro" prompt | — |
| P2 | Still | Ritual texture — hands or ceramic detail (small, supporting) | Midjourney `02.06` Ceramic Vessels or `02.09` Beans Pouring | Ritual-R2 |

### Frame 03 · THE PLACE
| Slot | Type | Brief | Source | Reuses |
|------|------|-------|--------|--------|
| PL1 | Still | Wide architecture (courtyard or facade) | Midjourney `01.02` Interior Courtyard | — |
| PL2 | Still | Landscape with Tepozteco | Midjourney `03.01` Cerro del Tepozteco | Instagram-IG3 |
| PL3 | Still | Architectural detail (arch corridor or fireplace) | Midjourney `01.04` Long Corridor or `01.03` Stone Fireplace | — |
| PL4 | Still (optional) | Bougainvillea/color accent | Midjourney `03.02` Bougainvillea on Stone | Instagram-IG6 |

### Frame 04 · RITUAL
| Slot | Type | Brief | Source | Reuses |
|------|------|-------|--------|--------|
| R1 | Still | Hands holding ceramic cup (hero ritual moment) | Midjourney `02.01` Hands Holding Ceramic Cup | Instagram-IG5 |
| R2 | Still | Coffee preparation surface (V60 or olla) | Midjourney `02.02` V60 Pour-Over or `02.03` Mexican Olla | Philosophy-P2 |

### Frame 05 · STAY
| Slot | Type | Brief | Source | Reuses |
|------|------|-------|--------|--------|
| S1 | Still | Room/bedroom architecture, restrained | Midjourney `01.06` Linen Bedroom Suite | — |
| S2 | Still (small) | Detail moment (bathroom basin or threshold) | Midjourney `01.05` or `01.10` | — |

**Frame total: 9-10 unique stills (after reuse), 0-1 motion**

---

## 03 · Surface Detail: Instagram Grid (9 posts)

| Post | Type | Brief | Source |
|------|------|-------|--------|
| IG1 | SVG/Figma | Brand wordmark on dark base | Figma component |
| IG2 | SVG/Figma | Editorial quote ("Volcanic restraint.") in Cormorant | Figma component |
| IG3 | Still | Phase 01 AI landscape (Tepozteco) | **REUSE Place-PL2** |
| IG4 | Still | Room reveal | **REUSE Stay-S1** |
| IG5 | Still | Coffee ritual macro (hands or pour) | **REUSE Ritual-R1** |
| IG6 | Still | Architectural color story (bougainvillea or stone) | **REUSE Place-PL4** |
| IG7 | SVG/Figma | Token swatch flat-lay | Figma component |
| IG8 | Screenshot | Figma Make build-in-public moment | Screen capture (existing) |
| IG9 | SVG/Figma | CTA card with site URL | Figma component |

**Instagram unique generations needed: 0 — everything reuses from site stills**

---

## 04 · Surface Detail: Guest Portal Welcome Screen

| Slot | Type | Brief | Source |
|------|------|-------|--------|
| GP1 | Still | Mood image — architectural moment (single frame, atmospheric) | **REUSE Place-PL1 or Hero-H1** |

**Guest Portal unique generations needed: 0 — reuses from site**

---

## 05 · Surface Detail: Figma Weave Motion Hero

| Slot | Type | Brief | Source |
|------|------|-------|--------|
| MH1 | Motion 6s loop | Volcanic landscape at dawn, slow camera reveal, Tepozteco visible | Figma Weave |

**Weave generations needed: 1 motion loop (with 2-3 alternates).**
This replaces Hero-H1 still if going motion-led on the live site. Generate Day 7, not Sprint 4.1.

---

## 06 · Submission Video

Uses B-roll from:
- Screen Studio captures of token sync moment
- Figma Make build process recording
- Mobile responsive demo
- Guest Portal welcome screen reveal
- Existing stills from this asset map

**No new image generations needed.**

---

## 07 · Master Generation List (post-dedup)

These are the actual prompts to run. **~10-11 unique stills + 1 motion loop.**

| # | Prompt ID | Used in | Priority |
|---|-----------|---------|----------|
| 1 | `01.02` Interior Courtyard | Place-PL1, Portal-GP1 (maybe) | ⭐ HIGH |
| 2 | `01.04` Long Corridor with Arches | Place-PL3 | ⭐ HIGH |
| 3 | `01.06` Linen Bedroom Suite | Stay-S1, IG-Room | ⭐ HIGH |
| 4 | `02.01` Hands Holding Ceramic Cup | Ritual-R1, IG-Coffee | ⭐ HIGH |
| 5 | `03.01` Cerro del Tepozteco at Dawn | Place-PL2, IG-Landscape | ⭐ HIGH |
| 6 | `01.10` Entry Threshold (or stone macro) | Philosophy-P1 | MEDIUM |
| 7 | `02.06` Ceramic Vessels (or `02.09` Beans) | Philosophy-P2 | MEDIUM |
| 8 | `02.02` V60 Pour-Over (or `02.03` Mexican Olla) | Ritual-R2 | MEDIUM |
| 9 | `01.05` Stone Slab Wet Room | Stay-S2 (optional detail) | LOW |
| 10 | `03.02` Bougainvillea on Stone | Place-PL4 (optional accent), IG-color | LOW |
| 11 | `01.01` Basalt Facade (still fallback) | Hero-H1 if no motion | CONDITIONAL on Weave going well |
| MH1 | Weave motion loop | Hero-H1 (replaces still) | Day 7 |

---

## 08 · Workflow: Tonight vs Day 4-5

### TONIGHT (Sprint 4.1 — corrected scope)

The right work is **NOT** "generate the full library." It's:

```
HOUR 1 — Lo-fi wireframes
   Sketch the 5 Figma Make frames on paper or in Figma (boxes + labels).
   Confirm slot positions for each image.
   Output: frame thumbnails with slot annotations.

HOUR 2 — Test Generation Set (~5 prompts)
   Generate prompts 01.02, 02.01, and 03.01 in Midjourney Web — 
   1 grid each = 3 grids = 12 outputs.
   Goal: validate the visual direction works.
   Is "Modern Luxury Volcanic Hospitality" rendering correctly?
   Are the references (Aman, Casa TO) pulling the right aesthetic?
   
HOUR 3 — Curate the test set
   Drop grids in this chat — we score against Keep/Kill criteria.
   Lock 2-3 baseline images that prove the direction.
   Identify any prompt refinements needed before Day 4-5 full gen.

HOUR 4 — Document + commit
   Update photo-manifest.json with test set IDs.
   Commit asset-map.md + image-direction-v5.md + any test set notes.
   git push.
```

### DAY 4-5 (Build Frames + Targeted Generation)

When you're in Figma building the frames anyway:

```
Day 4 morning   — Generate remaining HIGH priority prompts (#2-5 from master list)
Day 4 afternoon — Build Hero + Philosophy + Place frames with real assets
Day 5 morning   — Generate MEDIUM priority prompts (#6-8)
Day 5 afternoon — Build Ritual + Stay frames, polish all 5, ready for Figma Make
```

Targeted, slot-driven, efficient.

---

## 09 · Credit Budget Estimate

Midjourney credit math (approximate):

```
Test set tonight:       3 prompts × 1 grid each       = 3 grids   ≈ 4-6 minutes generation
Day 4-5 HIGH priority:  5 prompts × 2 grids each      = 10 grids  ≈ 15 minutes
Day 4-5 MEDIUM:         3 prompts × 1-2 grids each    = 4-6 grids ≈ 8 minutes
Day 4-5 LOW (optional): 2 prompts × 1 grid each       = 2 grids   ≈ 3 minutes
                                                       ─────────
                                                       ~20 grids total
```

Compare to the original 40-prompt library × 4 grids each = 160 grids. **You save ~85% of the credit budget** and produce a tighter, more intentional visual library.

Weave: 1 motion loop × 2-3 alternates = ~3 generations from 1500 credits. No problem.

---

## 10 · Decision Log

This asset map adopts these rules:

1. **Generate against slots, not against ideas.** Every prompt has a placement target.
2. **Reuse aggressively.** One Tepozteco landscape serves the site, Instagram, and Portal.
3. **Wireframe before generating.** Slot positions inform the composition needed.
4. **Test the direction with a small set before committing to the asset set.**
5. **Use the right tool: Midjourney for stills, Weave for motion.** Don't blur the lines.
6. **The image-direction-v5.md prompt library is a menu, not a mandate.** Pull from it when slots need it.

---

**This asset map evolves.** If wireframes reveal additional slots, add them. If a planned reuse doesn't work visually, generate a unique. Track changes in this file so the slot inventory stays the source of truth.
