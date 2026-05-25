# Estancia Cafetera — Brand Brief

> Machine-readable brand brief. Designed to be consumed by an LLM (Claude, GPT, Cursor, etc.) as system context so the AI can produce on-brand copy, image prompts, social posts, and surface designs without designer involvement.

---

## 01 · Brand direction

Estancia Cafetera is a 100-year-old coffee estate boutique hotel in Tepoztlán, Morelos, México. 10 rooms, 1 restaurant. Target price $500/night. The brand philosophy is **volcanic restraint** — premium through patience, not polish. Heritage coffee plantation that started welcoming guests; not a hotel that added coffee as an amenity. The brand IS the typography. No standalone logo. No decorative ornament. Light is punctuation; dark is base.

---

## 02 · Color tokens

| Token name | Hex | Use |
|---|---|---|
| `obsidian` | `#1A1814` | Deepest dark. Never pure black. |
| `ash` | `#E8E4DC` | Warm off-white. Primary text on dark. |
| `copper` | `#B87333` | Brief-locked accent. Use sparingly. |
| `clay-dark` | `#2E1F15` | **Document base** — dark coffee brown. |
| `clay-deep` | `#1F1410` | Cards, code blocks, deeper surfaces. |
| `clay-lift` | `#3A2818` | Hover states, elevated surfaces. |
| `terracotta-light` | `#E9D3C1` | Warm clay light. |
| `terracotta-deep` | `#B8704A` | Warm clay deep. |
| `ember` | `#C26A2C` | Primary accent — warmer than copper. |
| `green-deep` | `#2C3E2D` | Secondary — foliage in imagery, rare in UI. |
| `fog` | `#C4BDB0` | Muted grey-warm. |
| `cream` | `#F5F0E8` | Soft cream. Never pure white. |
| `ink-soft` | `#B8A88E` | Secondary body text on dark. |
| `ink-faint` | `#8A7B63` | Captions, metadata. |

```css
:root {
  --bg:                 #2E1F15;
  --bg-deep:            #1F1410;
  --bg-lift:            #3A2818;
  --ink:                #E8E4DC;
  --ink-soft:           #B8A88E;
  --ink-faint:          #8A7B63;
  --accent:             #C26A2C;
  --accent-brief:       #B87333;
  --terracotta-light:   #E9D3C1;
  --terracotta-deep:    #B8704A;
  --rule:               rgba(232, 228, 220, 0.1);
  --rule-soft:          rgba(232, 228, 220, 0.05);
}
```

**Never use:** pure white (`#FFFFFF`), pure black (`#000000`), corporate blue, bright orange, neon, saturated primaries.

---

## 03 · Typography rules

| Role | Font | When to use |
|---|---|---|
| **Wordmark** | Archivo Black + SVG ink-bleed filter | The name itself. Signage. Room numbers. Coffee bag labels. Leather tags. Always with `filter: url(#ink-bleed)`. |
| **Editorial** | Migra Light / Light Italic _(Cormorant Garamond as free placeholder)_ | Section headlines, pull-quotes, ledes, editorial body. Always lowercase or sentence case. Italic for emphasis. |
| **Body** | Söhne / Untitled Sans _(Inter as free placeholder)_ | All reading copy. UI text. Sentence case. |
| **Mono** | DM Mono | Labels, metadata, room codes, captions, dividers. Always uppercase. `letter-spacing: 0.14em` minimum. |

**SVG ink-bleed filter definition** (paste once per page, reference via `filter: url(#ink-bleed)`):

```html
<svg width="0" height="0" style="position:absolute">
  <filter id="ink-bleed">
    <feTurbulence type="fractalNoise" baseFrequency="0.04" numOctaves="2" seed="3" result="noise"/>
    <feDisplacementMap in="SourceGraphic" in2="noise" scale="2.5" xChannelSelector="R" yChannelSelector="G" result="displaced"/>
    <feGaussianBlur in="displaced" stdDeviation="0.3" result="blurred"/>
    <feComponentTransfer in="blurred"><feFuncA type="linear" slope="1.4" intercept="-0.1"/></feComponentTransfer>
  </filter>
</svg>
```

---

## 04 · Voice rules

Voice principles: **specific, slow, understated.** Names what's actually there. Trusts the reader. No marketing language, no exclamation marks, no adjective stacking.

### Do / Don't pairs

| ✓ We say | ✗ We don't say |
|---|---|
| "The coffee was planted in 1924. The rooms came later." | "Welcome to our luxurious historic boutique hotel experience!" |
| "Bourbon, washed. From the eastern slope." | "Premium artisanal single-origin specialty coffee." |
| "Ten rooms. One restaurant. The estate the rest of the time." | "Boutique luxury accommodation with world-class dining." |
| "Breakfast at 8. Dinner at 8." | "Indulge in our award-winning culinary experience." |
| "Hand-thrown ceramic. Made in Cuernavaca." | "Carefully curated artisanal tableware." |
| "Slow. Quiet. Specific." | "Discover your perfect escape." |
| "The hammock is by the higuera." | "Relax in our serene tropical sanctuary." |
| "We keep the lights low at dinner." | "Experience our intimate ambient dining atmosphere." |
| "Stone, wood, linen, copper. That's the room." | "Each suite is meticulously designed for ultimate comfort." |
| "It's cold in the mornings up here." | "Enjoy refreshing highland mornings in our climate." |

---

## 05 · Image direction rules

### ALWAYS

- Single-source natural light. Side light from camera left or right.
- Long shadows. Specular highlights on stone, ceramic, copper.
- Hand-touched textures in foreground: chisel marks, throwing rings, slubs, crema.
- Hands at work — barista tamping, farmer sorting, cook kneading. **No faces to camera.**
- Deep earth palette: terracotta, dark brown, ash linen, copper accent, deep green foliage.
- Medium format film aesthetic: Mamiya 7 / Hasselblad, Kodak Portra 400, slight grain.
- Off-center composition with generous negative space.
- Observed moments — looks caught, not posed.

### NEVER

- Flash, fill light, HDR, drone shots.
- Faces in clear focus, smiling to camera.
- Bright primaries, neon, pure white, saturated stock-photo color.
- Centered "brochure" compositions.
- Invented decorative objects — fake plants, ornamental serving ware, wellness props.
- Modern technology visible (phones, laptops, screens).
- Logos, watermarks, signage in shot.
- Pinterest-board mood without specific subject matter.

### Master Midjourney v7 prompt structure

```
[SUBJECT], [LIGHT direction], [COMPOSITION], hand-thrown ceramic/dark wood/copper/linen, 
warm terracotta and deep brown earth tones, no saturation, medium format film, Mamiya 7, 
Kodak Portra 400, slight grain, shallow depth of field, quiet observed documentary, 
no people facing camera, no logos, no modern technology --ar 4:5 --style raw --stylize 200 --v 7
```

**Never exceed `--stylize 250`** — higher values make Midjourney invent decorative kitsch.

---

## 06 · Guest profiles

### Profile 01 — The Coffee Pilgrim

**Signals:** Travels for varietals. Knows what bourbon means as a coffee. Asks about altitude, process, farmer name. Brings their own grinder. Writes in a notebook.

**Wants:** Single-origin transparency. Farmer access. Cupping sessions. Knowledge that respects their knowledge.

**Doesn't want:** Generic "coffee experience." Vague origin stories. Performance of expertise.

### Profile 02 — The Heritage Heir

**Signals:** Mexican or Mexican-American. Has hacienda ancestry, or wishes they did. Speaks Spanish at the restaurant. Asks about the original family. Notices the ceramic was made in Cuernavaca.

**Wants:** Cultural fluency without costume. Restraint with the Mexican identity. No mariachi, no piñatas, no "fiesta" anywhere.

**Doesn't want:** Tropical resort kitsch. English-only menus. Mexican identity flattened into decoration.

### Profile 03 — The Aesthete

**Signals:** 32-48. Creative director, architect, brand founder, photographer. Pays $500/night for material experience, not amenities. Notices the typography on the door tag. Asks who designed the bath fixtures.

**Wants:** Intentional restraint. Material truth. Reference-grade execution. To stay somewhere that could be a magazine feature without being designed for one.

**Doesn't want:** Themed rooms. Excessive amenity offerings. Anything that looks "designed" rather than considered.

### Convergence

All three profiles reward: **quiet expertise, cultural fluency without theatre, intentional restraint, and material truth over decoration.**

---

## 07 · Spacing and layout

8pt spacing scale (use these tokens, never arbitrary px values):

```
s-1: 4px    s-2: 8px     s-3: 16px    s-4: 24px
s-5: 40px   s-6: 64px    s-7: 104px   s-8: 168px
```

**Section padding:** vertical `s-8` (168px) top, `s-7` (104px) bottom.
**Card padding:** `s-5` (40px) all sides.
**Body line-height:** 1.6.
**Heading letter-spacing:** -0.02em.

---

## 08 · How to use this file

When prompting Claude or GPT to produce on-brand output for Estancia Cafetera, paste the relevant section(s) into the system context. For example:

**Producing copy:**
> "Use the voice rules in Section 04. Write three lines describing the hot stone bath in Casa Higuera. Max 25 words total."

**Producing image prompts:**
> "Use the image direction rules in Section 05 and the master prompt structure. Generate a Midjourney prompt for 'morning coffee service in the courtyard.'"

**Producing surface design:**
> "Use the color tokens in Section 02 and typography rules in Section 03. Design a guest welcome card for Casa Higuera. Output as HTML."

**Producing social content:**
> "Use the voice rules (Section 04) and guest profile signals (Section 06). Write three Instagram captions for an image of hands sorting coffee cherries. The Coffee Pilgrim is the primary audience."

---

## 09 · Files in this repo

- `index.html` — the human-readable brand system (rendered)
- `image-direction.html` — Sprint 4 prompt library (40 Midjourney + 8 Sora + 12 Kittl)
- `estancia-cafetera.json` — design tokens for Tokens Studio / Figma sync
- `estancia-cafetera.md` — this file. Brand rules for AI consumption.

---

_Last updated: 2026-05-22. Version 1.0._
