# PPT Style Exploration Image — Creative Brief

## Intent

Generate **ONE single reference image** that shows **5 distinct visual style directions** for a future Mapii presentation deck. Each direction appears as a mini "cover slide / key visual" of the *same* presentation, arranged side-by-side in one composition so styles can be compared at a glance. This is a style-selection tool — **not** the deck itself, and not separate images.

## Subject (inferred from mapii.cloud — confirm below)

**Mapii** — an AI-powered Local SEO platform for Thai SMEs. It tracks Google Maps rankings, consolidates reviews into one inbox with AI-drafted Thai replies, and coaches shop owners on what to do each week. Positioning: "ให้ลูกค้าใกล้คุณ เจอร้านคุณก่อนใคร บน Google Maps" (help nearby customers find your shop first on Google Maps). Pricing ฿590–1,490/month, 14-day free trial, no card required.

> TODO: The original brief left `[TOPIC]`, `[AUDIENCE]`, `[GOAL]`, and `[KEY POINTS]` as placeholders. Defaults below are inferred from mapii.cloud — edit them before handoff.

- **Topic (assumed):** Mapii product introduction / pitch — Local SEO for Thai SMEs
- **Audience (assumed):** Thai SME owners, potential investors, or internal stakeholders — *TODO: confirm*
- **Goal (assumed):** Convince the audience that Mapii makes local businesses discoverable on Google Maps without agencies or guesswork — *TODO: confirm*

## Key content points to reflect (from mapii.cloud)

1. Rank Tracker — daily Google Maps ranking per keyword/area (geo-grid)
2. Review Inbox — all branches in one place, AI drafts polite Thai replies
3. AI Coach — weekly recommendations + drafted Google Posts, owner approves before publishing
4. 5-step onboarding — connect Google Business Profile in minutes, no technical skill needed
5. Results — e.g. café in Chiang Mai moved from rank 8 → 2; +312% discovery in 14 days
6. Pricing — Start ฿590 / Pro ฿990 / Business ฿1,490 per month, free 14-day trial
7. Built for Thai local search behavior ("คาเฟ่ อารีย์", "ใกล้ BTS อโศก")

## Image specification

- **Surface:** image (single file, e.g. `ppt-style-directions.png`)
- **Aspect:** 16:9 (per active plugin input)
- **Model:** default `vela/gpt-image-2` unless changed at handoff
- **Composition:** one canvas divided into 5 equal panels (row or 2+3 grid), each panel a self-contained cover-slide design with a small caption label underneath or in a corner
- **Each panel must show:** the same presentation title ("Mapii — Local SEO for Thai SMEs" or Thai equivalent), but rendered in a genuinely different layout, typography, color palette, texture, and visual language

## The 5 style directions

| # | Label | Visual language |
|---|-------|-----------------|
| 1 | **Swiss editorial** | White/off-white canvas, strict grid, huge grotesque type, one red or black accent, generous negative space, no decoration |
| 2 | **Neo-brutalist** | Raw blocks, thick black borders, clashing saturated colors, exposed grid lines, sticker-like badges, hard shadows |
| 3 | **Glassmorphism** | Dark gradient backdrop, frosted translucent cards, soft blur, glowing map-pin motif, light blue/violet rim light |
| 4 | **Cinematic technology** | Pure black void, electric blue accent (Framer-style), compressed display type with tight tracking, product UI screenshot as hero art, subtle blue ring glows |
| 5 | **Data magazine** | Editorial report look — charts, geo-grid map fragments, big numerals ("+312%"), serif/sans mix, warm paper or deep green ink palette |

Optional 6th: **Product launch** — glossy keynote style, floating 3D phone mockup, spotlight gradient, bold centered title.

## Style references

- **mapii.cloud** — source brand: friendly Thai SaaS, map-pin identity, blue/green tones, SME-warm voice
- **OpenDesign Homepage** (@ mention) — reference for the cinematic-technology panel: WebGL-grade dark hero craft, motion-rich, high-polish
- **Framer design system** (active) — informs panel 4: void black `#000000`, Framer Blue `#0099ff`, pill shapes, tight-tracked display type
- **3D Stone Staircase Evolution Infographic** (reference template) — borrow its structured multi-panel infographic discipline: clear separation, labeled sections, consistent caption treatment

## Generation prompt draft (to be finalized at handoff)

> A single 16:9 infographic image divided into 5 clearly separated vertical panels, each panel showing a different cover-slide design for the same presentation titled "Mapii — Local SEO for Thai SMEs". Panel 1 labeled "Swiss editorial": white background, strict grid, huge black grotesque typography, single red accent. Panel 2 labeled "Neo-brutalist": thick black outlines, clashing bright colors, hard shadows, sticker badges. Panel 3 labeled "Glassmorphism": dark gradient, frosted glass cards, glowing map pin, soft blur. Panel 4 labeled "Cinematic technology": pure black background, electric blue accents, compressed display type, floating dashboard UI screenshot. Panel 5 labeled "Data magazine": editorial report style with charts, a geo-grid map fragment, and a large "+312%" numeral. Each panel genuinely different in layout, typography, color, and texture. Clean labels under each panel. High detail, professional presentation-design quality.

## Reference asset map (Creative Director pass)

What exists, what it is good for, and what to watch out for. No image binaries are in Design Files yet; all references below are code/content evidence or live URLs — this run is text-to-image, so they steer the prompt rather than feed the model directly.

| # | Candidate | Source | Usage notes | Caveats |
|---|-----------|--------|-------------|---------|
| A | Mapii logo (`/icon.png`) + marketing photos (`cafe-owner-hero.jpg`, `agency-consult.jpg`) | mapii.cloud live assets | Ground truth for brand mark and photo treatment (real Thai café / agency photography). Keeps panels 3–5 honest to the brand world. | First-party assets (linked Mapii-Local-Marketing repo is the user's own) — confirm before external republishing. Cannot be fed as model input in this run. |
| B | Brand posture from linked code (`app/(marketing)/page.tsx`) | Linked code folder (read-only) | Extracted: Lucide monoline icons in glass squircles with soft gradient tints (teal / primary / accent), floating Thai search-query pills ("คาเฟ่ ทองหล่อ", "ใกล้ BTS อโศก"), map-pin motif, friendly light-SaaS tone. This is the component posture to echo in brand-adjacent panels. | Exact hex lives in `@/lib/og` + global CSS, outside the linked folder — palette inferred from class names, not read verbatim. |
| C | Real copy & metrics from mapii.cloud | Fetched page content | Panel copy must come from here: "+312% การค้นพบ · 14 วัน", "฿590 / ฿990 / ฿1,490", "อันดับ 8 → 2 (คาเฟ่เชียงใหม่)", geo-grid ranking, 5-step onboarding. Prevents invented-metric slop. | Thai text rendering in image models is unreliable — prefer short Thai fragments or English labels in the generated image. |
| D | OpenDesign Homepage plugin (@ mention) | Plugin context | Craft bar for panel 4 (cinematic technology): WebGL-grade dark hero, sticker collage, variable-font display type, parallax energy. | First-party OD showcase — quality reference only, do not copy assets or wordmark. |
| E | Framer design system (active) | tokens.css / DESIGN.md in context | Panel 4 recipe: void black #000000, Framer Blue #0099ff, pill radii, blue ring-shadow rgba(0,153,255,0.15), compressed display tracking. | Curated fixture, not upstream Framer evidence. |
| F | 3D Stone Staircase Evolution Infographic (reference template) | Plugin template | Structural discipline for the multi-panel grid: clear separation, labeled sections, consistent caption treatment. | CC-BY-4.0 (YouMind-OpenLab/awesome-gpt-image-2) — preserve attribution if template language is echoed. |
| G | Screenshot Website / ScreenshotOne / Pagecast / Aesthetics Wiki | MCP templates | Would give pixel-true captures of mapii.cloud and style moodboards for the 5 directions. | Templates only — 0 MCPs enabled in this run. Enable one if pixel fidelity is needed before generation. |

### Gap verdict

No connector or MCP is enabled and Design Files holds only this brief — so there is **no usable pixel asset in-project**. That is acceptable: the deliverable is a style-exploration concept image, and candidates A–F give enough brand + structure evidence to prompt it well. If pixel-true brand capture becomes a requirement, enable a screenshot MCP (G) first.

### Fallback generation prompt (if no asset is ever captured)

> A single 16:9 infographic image divided into 5 clearly separated vertical panels, each showing a different cover-slide design for the same presentation titled "Mapii — Local SEO for Thai SMEs". Panel 1 "Swiss editorial": off-white background, strict grid, huge black grotesque typography, single red accent. Panel 2 "Neo-brutalist": thick black outlines, clashing bright colors, hard shadows, sticker badges. Panel 3 "Glassmorphism": deep blue-violet gradient, frosted glass cards, glowing map pin, soft blur. Panel 4 "Cinematic technology": pure black background, electric blue #0099ff accents, compressed display type, floating dashboard UI with a geo-grid map. Panel 5 "Data magazine": editorial report style, warm paper texture, bar charts, a geo-grid map fragment, large "+312%" numeral. Each panel genuinely different in layout, typography, color, and texture; small clean style label under each panel; professional presentation-design quality; high detail.

## Image-slot audit & replacement specs (Creative Director pass 2)

Every visible image slot in the planned composition, graded, with exact replacement specs. The design currently has **zero pixels** — all slots are text specs — so "weak" here means *the current spec would produce generic or off-brand imagery at generation time*. Layout (5 equal panels + labels) is preserved; only the imagery inside each panel is re-specified.

| Slot | Role | Grade | Replacement spec |
|------|------|-------|------------------|
| S1 Swiss editorial — inline image | Small accent inside white grid | weak | Was "no decoration" → empty-panel risk. Spec: ONE macro B&W photo crop (map-pin metal head or Bangkok shophouse texture), high-contrast silver-gelatin grade, thin black frame, ~20% of panel. No stock business photo. |
| S2 Neo-brutalist — hero graphic | Main visual punch | weak | Was "sticker badges" → clipart risk. Spec: one flat 2D vector map-pin illustration, slightly rotated, 3-color max (e.g. yellow + blue + black outline), offset-print misregistration texture, hard 4px drop shadow. |
| S3 Glassmorphism — background | Full-panel backdrop | placeholder | Was "dark gradient" → purple-blue AI-gradient slop risk. Spec: blurred night-city bokeh photo (Bangkok street, teal/sodium lights) under frosted-glass cards; color grade locked to blue-teal, NOT violet. Glowing map pin stays as the single focal glow. |
| S4 Cinematic technology — hero image | Product UI as hero art | weak | Was "floating dashboard UI screenshot" → fake-dashboard slop risk. Spec: dark-mode rank-tracker UI crop — geo-grid heatmap over a dark map, one blue (#0099ff) data line, "+312%" as a quiet corner stat, 12px rounded corners, blue ring-shadow border. UI must look like a real analytics tool, not chart spam. |
| S5 Data magazine — supporting images | Report texture | weak | Was "charts + map fragment" → clip-art chart risk. Spec: duotone (deep green ink on warm paper) halftone photo of a Thai café counter + one hand-drawn-feel geo-grid map fragment + bar chart rendered as printed report graphics with slight ink texture. |
| L1–L5 Panel labels | Captions under panels | ok | Keep: small sans caps, consistent across all 5 panels (borrows staircase-template discipline). |

### Slot-source matrix

| Slot | Source choice | Why | Exact prompt fragment (for the generation pass) |
|------|---------------|-----|--------------------------------------------------|
| S1 | Generate (no real asset needed) | Macro B&W texture is style, not brand evidence | "one macro black-and-white photograph of a metal map pin head, high contrast, thin black frame" |
| S2 | Generate | Flat vector sticker must match the brutalist panel exactly | "flat 2D vector map-pin sticker, yellow and blue with thick black outline, offset print misregistration, hard drop shadow" |
| S3 | Generate (or replace with captured mapii.cloud hero if screenshot MCP is enabled later) | Blurred night-city backdrop; real asset A (`cafe-owner-hero.jpg`) can't be fed to the model this run | "blurred Bangkok night street bokeh, teal and warm sodium lights, dark blue-teal grade, behind frosted glass panels" |
| S4 | Generate; upgrade path = real screenshot | Product UI as hero art; a real capture of app.mapii.cloud would beat generation — enable Screenshot Website MCP to get it | "dark-mode local-SEO rank tracker dashboard, geo-grid heatmap over dark map, single electric blue #0099ff data line, 12px rounded corners, subtle blue ring border" |
| S5 | Generate | Duotone report graphics are style-specific | "duotone halftone photo of a Thai cafe counter in deep green ink on warm paper, hand-drawn geo-grid map fragment, printed bar chart with ink texture" |

### Anti-slop guards for the generation pass

- Ban purple→blue gradients (S3 must stay blue-teal), glowing orbs, floating spheres.
- No invented metrics beyond the sourced set: "+312%", "฿590/990/1,490", "rank 8 → 2".
- No generic dashboard chart spam in S4 — one map, one data line, one stat.
- Thai text: only short fragments ("คาเฟ่ ทองหล่อ") or English labels; image models mangle long Thai strings.
- Panel 4 binds Framer tokens (void black, #0099ff, ring shadow); panel 3 borrows Mapii's glass-squircle posture from the linked code.

### Verification checklist (run after generation)

1. 5 panels, clearly separated, each with a readable style label.
2. Each panel's layout/type/color/texture is genuinely distinct — no two panels share a palette.
3. S3 has a photographic bokeh backdrop, not a flat AI gradient.
4. S4's UI reads as a real analytics product (map + heatmap), not fake dashboard spam.
5. Only sourced metrics appear; no "10×" / "99.9%" inventions.
6. Labels legible; Thai fragments (if any) not garbled — regenerate once if they are.

## Style-direction evaluation (Creative Director pass 3 — with real brand evidence)

### New brand evidence (uploaded this turn)

- `wiNrC.jpg` — black lockup on white (icon + "Mapii Local" wordmark)
- `O37Wx.jpg` — color lockup with clearspace/construction guides
- `VKhuy.jpg` — color lockup on dark background
- `pr0hU.jpg` — mono mark (white mark on black squircle)
- `mapii_icon_color.png` — **the palette truth**: teal → orange gradient over a faint map-street grid, white "M + map-pin" glyph
- `mapii_lockup_color_transparent.png`, `mapii_mark_black_transparent.png` — transparent production assets

Brand read: Mapii is a **warm, friendly, dual-tone (teal/orange) Thai SaaS** — not a cold mono-blue tech brand. The icon's street-grid texture and pin glyph are the core motifs. This evidence overrides two earlier assumptions: panel 4's "Framer #0099ff electric blue" is off-brand, and panel 1's "single red accent" was a guess.

### Scorecard (each criterion 1–5, /20 total)

| Criterion | 1. Swiss editorial | 2. Neo-brutalist | 3. Glassmorphism | 4. Cinematic tech | 5. Data magazine |
|---|---|---|---|---|---|
| Supports the message (local discovery, warm SME help) | 3 — credible but cold | 2 — shouty, fights the "friendly coach" message | 4 — modern and approachable | 3 — impressive but enterprise-intimidating for SME owners | 5 — proof-first, matches "results you can see" |
| Fits the audience (Thai SME owners / investors) | 3 — owners may read it as sterile | 2 — reads as hype/sticker-chaos to non-designers | 4 — familiar consumer-app feel | 3 — investors like it, owners less so | 4 — numbers + maps are universally legible |
| Scales to a full deck (10–20 slides) | 5 — grid systems scale best | 2 — exhausting at slide 8+ | 3 — blur/glow gets repetitive, dark hurts print | 3 — dark deck strains projectors and print | 5 — editorial report = deck-native format |
| Room for text, charts, screenshots, logos | 5 — maximal whitespace | 2 — decoration eats content area | 2 — glass cards + glow consume contrast and space | 3 — dark UI shots blend into dark bg; logos need light boxes | 5 — built for charts, callouts, sidebar notes |
| **Total** | **16** | **8** | **13** | **12** | **19** |

### Recommendation: **Data magazine (5)** — with Swiss editorial (16) as the runner-up and the safety pick

**Why Data magazine wins:**

1. **Message fit** — Mapii's pitch is literally "see your rank move on a map, see the number go up" (+312%, rank 8→2, geo-grid). A report/editorial visual language makes the *proof* the hero instead of decoration. No other direction turns the product's own data into the aesthetic.
2. **Brand fit** — the deep-green-ink + warm-paper spec adapts cleanly to the real teal/orange palette (teal as primary ink, orange reserved for highlights and the "+312%" numerals). The icon's street-grid texture becomes the deck's recurring background motif — a move no other direction can absorb as naturally.
3. **Scalability** — editorial report structure (cover → executive summary → chart spreads → case-study pages → pricing table → closing) maps 1:1 onto a deck's anatomy. Charts, map fragments, big numerals, pull quotes all have native slots.
4. **Content room** — best-in-class: generous margins for Thai/English text, chart areas, screenshot frames with captions, and logo placement on every slide master. Thai text especially benefits — editorial layouts carry mixed-script content gracefully.

**Trade-offs to accept:** less "wow" than cinematic tech on slide 1; investors expecting a flashy keynote may find it quiet. Mitigation: borrow ONE move from cinematic tech for the cover only — a dark cover slide with the map-grid motif glowing in teal, then open into the light editorial interior. (Cover = cinematic tech panel 4; slides 2+ = data magazine.)

**When to pick the runner-up instead:** if the audience turns out to be primarily investors/VC (TODO: confirm — `[AUDIENCE]` is still a placeholder), Swiss editorial becomes the safer primary: maximum credibility, best print behavior, and the teal/orange duo sits beautifully on off-white.

### Open questions this evaluation raised

- [ ] `[TOPIC]` / `[AUDIENCE]` / `[CONCLUSION]` are still placeholders — the recommendation assumes "product pitch to SME owners/stakeholders, conclusion: Mapii is the low-effort way to win Google Maps locally." Confirm or correct.
- [ ] Confirm the hybrid cover move (dark cinematic cover + light editorial interior) or keep the deck single-style.
- [ ] Deck language: Thai, English, or mixed (affects type choices in the deck system).

## Open questions

- [ ] Confirm topic, audience, and goal (placeholders were left blank)
- [ ] Language of the deck: Thai, English, or bilingual labels?
- [ ] Keep 5 directions or add the 6th (product launch)?
- [ ] Any style to exclude or any brand colors that must appear?

## Next step

Review and edit this brief — especially the **Open questions** and the prompt draft. When it looks right, say so (e.g. "approved, generate it") and the next run will dispatch the single style-exploration image via the media generation pipeline, then you can pick the winning direction for the full deck.
