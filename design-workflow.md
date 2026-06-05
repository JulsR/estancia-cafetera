# JR Operator · Design Workflow
## The 11-Step Framework for Brand-to-Product Hospitality Projects

**Author:** Julissa Roa
**Status:** Framework v1.0
**Date:** June 5, 2026
**Use:** Apply to any new hospitality project. Reference when drift is suspected. Onboarding artifact for collaborators.

---

## 00 · Why This Framework Exists

Most design work drifts. Not because the designer is undisciplined — but because creative work has a natural pull toward EXECUTION before the strategic frame is set. You see a moodboard reference and want to start. You read a brief and want to open Figma. You have AI tools and want to generate.

The drift looks like progress. Until you realize you've built 6 surfaces that don't tell the same story.

This framework exists for one reason: **to make drift detectable.** If you can't trace a deliverable back to a step in this workflow, you don't have a project — you have a pile of artifacts.

---

## 01 · The Workflow at a Glance

```
PHASE A · DEFINE                    ← strategy + foundation
─────────────────────────────────
01 · Concept
02 · Research + Moodboard
03 · Strategic Brief
04 · Brand Visual System

PHASE B · PLAN                      ← surfaces + slot inventory
─────────────────────────────────
05 · Deliverable Surfaces
06 · Wireframes / Prototypes
07 · Asset Map
08 · AI Test Generation

PHASE C · SHIP                      ← build + release + share
─────────────────────────────────
09 · Deliverables Build (production gen embedded)
10 · Deploy
11 · Post / Submit
```

Three phases. Eleven steps. Each step gates the next.

---

## 02 · Phase A · DEFINE

The why and the what. No execution until this phase is complete.

### Step 01 · Concept

The seed. One sentence that names what this is.

Format: *`[Type of thing] for [audience] that [unique value proposition].`*

Example: *"A volcanic hospitality sanctuary for travelers who want to reconnect with slower rhythms."*

**Test:** If you can't say it in one sentence without "and also..." you don't have a concept yet. You have a list.

### Step 02 · Research + Moodboard

Inputs: 3-5 reference brands · competitor scan · atmosphere references.

**Discipline matters more than volume.** A Pinterest board with 200 pins is not a moodboard — it's avoidance. Pick 3-5 strong references and commit.

Output: A curated set of brands and aesthetic anchors named explicitly (e.g., *"Aman for restraint, Casa TO for atmosphere"*). These names go IN the AI prompts later — they're the most powerful style transfer tool available.

### Step 03 · Strategic Brief

The document that contains:
- **Audience** — who specifically is this for
- **Why** — what problem does this solve in their life
- **Philosophy** — the worldview the brand operates from
- **Positioning** — the category claim
- **Creative Direction** — one line that drives every decision

This is the **single most important artifact in the project.** Every later step references it. When a decision is unclear, return here.

Format: Markdown. Lives in repo as `[project-name]-strategic-brief.md` or similar.

### Step 04 · Brand Visual System

Palette · Typography · Voice · Tokens.

Outputs:
- `tokens.json` — machine-readable, Tokens Studio compatible
- `brand-system.html` — visual presentation of the system
- `brand.md` — machine-readable brand spec

Iterate as you learn the brand. The visual system often evolves through doing — that's healthy. Lock when the strategic brief feels embodied in the visuals.

### 🚪 Phase A Gate

Before advancing, audit:
- Can I state the concept in one sentence?
- Is the strategic brief ratified (not draft)?
- Could a stranger understand the brand from these four artifacts alone?

If any answer is "no" — do not advance. Return.

---

## 03 · Phase B · PLAN

The where and the slots. No generation or building until this phase is complete.

### Step 05 · Deliverable Surfaces

List every surface you'll ship. Be specific.

Typical hospitality surfaces:
- Brand book / brand system page
- Marketing website
- Booking / reservation flow (if applicable)
- Guest portal (welcome, itinerary, concierge)
- Social media (Instagram, LinkedIn, etc.)
- Email touchpoints
- Print collateral (menus, key cards, etc.)
- Motion / video assets

**Cut ruthlessly.** Each surface added doubles the asset map and triples the polish time. A 4-surface ambitious project beats a 10-surface drifty project.

### Step 06 · Wireframes / Prototypes

Lo-fi structure per surface. Boxes and labels.

This is the step most designers skip — and the one that prevents the most rework. Wireframes determine what assets you need. Without wireframes, the asset map is hypothetical.

Tools: paper, iPad, or Figma. Doesn't matter. **Speed > fidelity** at this step.

### Step 07 · Asset Map

Every image, video, audio, and other media slot mapped to a surface.

Format: a table or markdown doc with columns:
`Slot ID · Surface · Type · Brief · Source · Reuses`

**Generate against slots, not against ideas.** This is the single rule that saves 85% of AI generation budget.

### Step 08 · AI Test Generation

3-5 prompts to validate that the visual direction renders correctly in AI.

Goal: **NOT** to produce final assets. Goal: to confirm "yes, the direction is generating correctly" before committing budget to the production set.

If the test fails:
- Add specific brand references to prompts (e.g., Aman, Casa TO)
- Use image references (drag refs into Midjourney Web)
- Adjust the strategic brief if the direction itself is mis-specified

### 🚪 Phase B Gate

Before advancing, audit:
- Is every deliverable surface listed and bounded?
- Does every surface have a wireframe?
- Does the asset map account for every visual slot?
- Has AI test generation confirmed the direction renders?

If any answer is "no" — return to step 06.

---

## 04 · Phase C · SHIP

The build and the share. Phase A and B are now your defense against drift.

### Step 09 · Deliverables Build

Frames · code · components · copy · motion.

**Production AI generation happens HERE**, not in Phase B. Generate assets targeted to specific slots from the asset map. As frames/components are built, drop real assets in their slots just-in-time.

Working order: build hi-fi designs surface by surface, with assets generated as needed.

### Step 10 · Deploy

Push to staging, then production. Get URLs live. Test on multiple devices.

Practice: each deploy is a chance to capture screen recordings for Build-in-Public content. Don't skip the recording.

### Step 11 · Post / Submit

The work doesn't exist until you share it. LinkedIn, X, Instagram, Contra, Figma Community, Medium.

**Lead with the strategic frame** (from step 03), not the deliverable. The strategic frame is what makes the work memorable.

---

## 05 · Iteration Loops

The workflow is sequential but not rigid. Common healthy loops:

```
03 ⟷ 04   The brief sharpens as the visuals develop (and vice versa)
05 ⟷ 06   New wireframes may surface a new surface (or cut one)
06 ⟷ 07   The asset map updates as wireframes evolve
08 → 03   If AI can't render the direction, sometimes the brief needs sharpening
09 → 03   The brand's voice often clarifies through copy work
```

**Healthy iteration** loops back, sharpens, advances.
**Drift** adds new deliverables without going back through Phase A or B.

---

## 06 · Failure Modes (what drift looks like)

### Failure 01 · Generate before slot
**Symptom:** Generating AI images without knowing where they'll go.
**Fix:** Return to step 07. Build the asset map first.

### Failure 02 · Add deliverable mid-project
**Symptom:** Suddenly building a second site after the first is half-done.
**Fix:** Return to step 05. Does the new surface serve the strategic brief? If no, cut. If yes, add it formally and update the asset map.

### Failure 03 · Brief drift
**Symptom:** Halfway through, the brand feels like something other than what the brief says.
**Fix:** Update step 03 to match where the work is going. THEN re-verify steps 04-08.

### Failure 04 · Polish drift
**Symptom:** Spending 6 hours perfecting one frame while 4 frames sit untouched.
**Fix:** Time-box Phase C surface by surface. First pass on ALL surfaces before second-pass polish on any.

### Failure 05 · Surface inflation
**Symptom:** "And I should also make X, and a Y, and..."
**Fix:** Trace the new surface back through phases A and B. If it doesn't connect, cut.

---

## 07 · How to Use This Document

For each new project:

1. **Start a project folder.** Inside it, create a `WORKFLOW.md` that copies the 11-step list.
2. **Add an artifact column.** As each step completes, link the artifact (file, link, doc).
3. **Treat the workflow doc as the project's table of contents.** It is the single source of truth for "where are we?"
4. **When drift is suspected**, trace the suspect deliverable back through steps 05 → 03. If it doesn't connect: cut. If it connects but wasn't planned: update the relevant phase docs.
5. **When onboarding a collaborator**, this doc + the project's step-by-step artifact list = full context in 15 minutes.

---

## 08 · Case Study: Estancia Cafetera

How this framework mapped to the Config Makeathon work (14-day sprint):

| Step | Estancia Artifact |
|------|---------------------|
| 01 · Concept | Boutique hospitality + coffee experience in Tepoztlán |
| 02 · Research | Aman · Casona Sforza · Hotel 23 · Casa TO references + 14 trip photos |
| 03 · Strategic Brief | `volcanic-hospitality-system.md` |
| 04 · Brand Visual System | `brand-system-v4.html` + `tokens.json` + `estancia-cafetera.md` |
| 05 · Deliverable Surfaces | Figma Make site + Instagram grid + Guest Portal welcome + Weave motion |
| 06 · Wireframes | Lo-fi sketches for 5 Figma Make frames (Day 1-2) |
| 07 · Asset Map | `asset-map.md` |
| 08 · AI Test Generation | 3-prompt test set, ~12 Midjourney outputs (Day 1-2) |
| 09 · Build | Figma Foundations → Frames → Figma Make → Portal Welcome (Day 3-8) |
| 10 · Deploy | Vercel + Figma Make publish (Day 7) |
| 11 · Submit | Contra + LinkedIn + Instagram + Figma Community (Day 10) |

### Drift caught and corrected mid-project

- ❌ → ✅ Original plan: generate 40-prompt visual library before defining slots. **Caught at step 07/08, corrected to 3-prompt test set + targeted Day 4-5 generation.** Credit savings: ~85%.
- ❌ → ✅ Added Framer comparison site without strategic justification. **Cut at step 05 audit.** Saved ~6 hours.
- ❌ → ✅ Guest Portal scope crept to 4 React screens. **Reduced to 1 Figma welcome frame at step 05.** Saved ~8 hours, became cleaner case study evidence.

Three pieces of drift caught because we had a framework to trace back through.

---

## 09 · Glossary

**Phase Gate** — A checkpoint between phases. Audit questions must all answer "yes" before advancing.

**Drift** — Adding deliverables or work without tracing through Phase A and B. The most common project failure mode.

**Slot** — A specific placement target for an asset within a surface (e.g., "Hero image, Frame 01 of Figma Make site").

**Asset Map** — The inventory of every visual slot across every surface, used to plan targeted generation.

**Strategic Frame** — The one-line creative direction from step 03 that every deliverable answers against.

---

## 10 · Why This Differs from Other Design Workflows

Most design workflows (Double Diamond, IDEO Design Thinking, etc.) are conceptual and discipline-agnostic. This framework is:

- **Operator-grade**, not academic — every step has a tangible artifact and a gate
- **Built for AI-native workflows** — explicitly accounts for AI test generation as a phase gate
- **Built for hospitality work specifically** — surfaces and patterns reflect hotel/restaurant/experience design
- **Built for ONE designer**, not a team — pragmatic about what one person can ship in 14 days
- **Drift-detectable** — every deliverable can be traced back to a step or it gets cut

This is not a process to copy. It's a starting framework to adapt to a specific operator's tools, surfaces, and pace.

---

**Authored by Julissa Roa**
*Hospitality Brand & Experience Designer · AI-Native Operator*

---

*This framework is opinionated and personal. Adopt what works, modify what doesn't, but always have A framework — drift is the cost of working without one.*
