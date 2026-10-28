# Master Video Prompt — Economic Geography Documentary

Two parts:
- **Part A** goes into any chat model with your finished script. It returns every beat with an image prompt and a video prompt.
- **Part B** is a style block you paste at the end of any single prompt in an image or video generator.

## Part A — Script → Beats → Image + Video Prompts

```
You are the visual director for a faceless YouTube documentary channel about economic geography and history. Turn the voiceover script below into a complete shot list for a 2.5D animated map video.

VIDEO TITLE: [title]
YEARS ON SCREEN: [YES / NO]   (match the script: if the script has no years, show no year tags)
SCRIPT:
[paste the full script]

STEP 1 — BEATS
- Split the ENTIRE script into beats in order. Do not skip, merge out of order, or rewrite any words.
- Each beat is at most 15 words (≈5 seconds at 2.98 words per second). Split long sentences at commas or colons, never mid-phrase.
- Number every beat: Beat 001, Beat 002…

STEP 2 — FOR EVERY BEAT OUTPUT
Beat ###
[Script Segment]: the exact words
Mode: PHYSICAL or VINTAGE (rules below)
Image Prompt: one standalone paragraph that does not rely on any other beat. Include: the exact place on the map (named countries, regions, cities, rivers), the subject, the 3D props and what they show, any on-screen label or number, the map mode colors, the camera, the lighting, the mood, and the full STYLE BLOCK at the end.
Video Prompt: one standalone paragraph. Include: "Start frame:" plus a short scene summary; the main motion (what moves, landing at about 70% of the clip, then settling); the camera move; ambient motion; the duration in seconds (segment words ÷ 2.98, rounded to 0.1); and the MOTION RULES at the end.
Camera Angle | Lighting | Mood | Action: one line each

MODE RULES
- PHYSICAL: geography, resources, modern economy, booms, present day. Photoreal shaded-relief satellite terrain: cerulean and turquoise ocean, vivid green lowlands, ochre and tan highlands, rust-brown ridges.
- VINTAGE: history before about 1950, empire, war, old trade, and scorecard recaps. Aged sepia parchment atlas: taupe seas, chocolate-brown land, cream paper grain.
- DARK lighting (in either mode): famine, war, crackdowns, crashes, debt and crisis beats. Dimmed, desaturated grading with ember-orange glows, drifting smoke and a strong vignette.

CAMERA OPTIONS (pick one per beat)
- Top-down orthographic: regional, continental, or ocean-wide/global scale.
- Slight 20-degree oblique tilt with a slow push-in.
- Low 25-degree oblique tilt, close regional scale, slow forward dolly.

VISUAL LANGUAGE
- Hero country: highlighted with a signal-yellow glow in positive beats and a glowing red-orange in crisis beats.
- Data: big 3D extruded glossy yellow-gold numbers with a dark outline, plus small dark rating tags.
- Labels: bold white uppercase sans-serif with a soft shadow, at most 1–3 words. Places get red teardrop pins.
- Flow and trade: glowing dotted routes with small white toy ships, trains or trucks moving along them.
- Comparisons: split frames, 3D balance scales, bar races, podiums, toy figures of different heights.
- Chapters: a numbered circular badge lights up when each chapter starts. Recaps use cream parchment scorecard cards with yellow (good) or red (bad) headers.
- Open loop: when the script teases something for later, show a locked or chained 3D badge, then open it when the script pays it off.
- People: ONLY small 3D toy figures. Never photoreal people or real likenesses of named individuals.
- Sensitive events (famine, war, repression): show them symbolically (empty bowls, smoke, glowing rings, toy trucks), never graphically.

STEP 3 — CHECKS (print at the end)
- Total beats, and confirmation that every word of the script appears exactly once.
- PHYSICAL vs VINTAGE beat counts.
- Total runtime = total script words ÷ 2.98.

STYLE BLOCK (append to every image prompt):
[paste Part B — Image Style]

MOTION RULES (append to every video prompt):
[paste Part B — Motion Style]
```

## Part B — Style Blocks (paste into any generator)

**Image Style**
```
Style: 2.5D animated map explainer: photoreal shaded-relief terrain map with crisp hillshade (or, in vintage mode, an aged sepia parchment atlas with subtle hand-engraved relief shading), overlaid with glossy toy-like 3D cartoon props (vinyl/clay finish, soft ambient occlusion, short drop shadows), bold white uppercase sans-serif map labels with soft shadow, signal-yellow (#FFD400) and glowing red-orange (#FF4A1C) highlight accents, puffy 3D clouds, soft top-down daylight from the northwest, gentle bloom on glowing elements, light vignette, people only as small 3D toy figures with no real likenesses, clean uncluttered composition with the four corners kept clear for UI, 16:9.
```

**Motion Style**
```
Style: 2.5D animated map explainer; terrain stays locked and stable; 3D toy-like props move with springy, bouncy ease-in-out animation and soft drop shadows; labels, year tags and yellow-gold 3D numbers pop in with a quick scale-bounce; clouds drift slowly, ocean shimmers subtly, glowing highlights pulse softly; slow push-in or gentle drift camera only, no rotation; no coastline morphing, no new text, no flicker, people only as small 3D toy figures; four corners kept clear for UI; 16:9, 24 fps.
```

## Workflow
1. Write the script with `MASTER-SCRIPT-PROMPT.md`.
2. Paste the script into Part A, with Part B pasted into its two placeholders.
3. Generate each image from its Image Prompt.
4. Animate each image with its Video Prompt, using the image as the start frame.
5. Trim each clip to its listed duration, lay the clips over the voiceover, and add the corner UI (chapter number, category badges, coin watermark) in the edit.
