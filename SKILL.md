---
name: photo-now-playing
description: "Turn a user-supplied everyday photo into a standardized portrait ‘now playing’ music-memory poster: prefer a verified real Chinese song unless the user requests another language, pair it with one very short verified lyric, crop a real photo detail as album art, and compose a visually prominent fixed-proportion music player with an atmosphere-matched palette and mandatory source-native foreground overlap. Use when users ask to turn a photo into a music player, song card, album-memory poster, ‘this photo is a song’ image, or a photographic music collage."
---

# Photo Now Playing

Create one original shareable poster that makes a photograph feel like it is playing a song. Treat the supplied photo as the memory; do not replace it with a newly invented scene.

## Workflow

1. Inspect the source photo and identify every essential subject and environmental anchor. Unless the user requests another format, create a standardized **3:4 portrait canvas at 1536 × 2048**. Reframe or uniformly scale the source without stretching it; crop expendable edges or extend only simple sky, snow, wall, water, or ground when needed. Preserve the source ratio only when essential content spans both horizontal edges and cannot survive a safe portrait conversion.
2. Identify two different visual anchors:
   - **Foreground subject:** the person, pet, object, or coherent object group that can overlap the player. A chair cluster, bicycle, plant, table setting, or similar group may be the subject even when no person exists.
   - **Album-art anchor:** a distinct environmental detail from the same photo, such as sky, leaves, food, a reflection, a table, a building detail, or a shadow.
   Do not use the foreground subject in the album art when it is also enlarged in front of the player.
3. Select music mode:
   - If the user specifies a song, use it.
   - If the user specifies a language, honor it. Otherwise, prefer one real **Chinese-language song** that matches the photo’s setting, light, palette, and mood.
   - Ask whether the user prefers Chinese or English only when language is genuinely decision-critical or when establishing a first-time preference. Do not make this a mandatory question for every generation; default to Chinese when no preference is available.
   - Verify the exact song title and artist before placing them.
   - Use at most one short lyric excerpt, ideally 3–8 words and never more than 10 words. If a fitting verified lyric is unavailable, use a short original mood caption instead and label it as a caption, not a lyric.
4. Compose the complete player as one stable design object. Use a deterministic template, image editor, or fixed layout layer for its geometry. Lock every internal component before creating depth; do not ask an image model to redraw the player after its proportion and layout have been selected.
5. Build mandatory depth in this exact layer order: background photo → complete player card with all components → source-native foreground subject or near-field detail. Make that real photo element **physically occlude** the player. Use 10–20% edge coverage for portraits and 20–35% lower-corner or side coverage for suitable object groups. Allow the foreground mask to cover text, waveform, progress, time, controls, or part of the cover when composition calls for it. Never move, squeeze, reorder, or resize player components to avoid the overlap. The card must visibly disappear behind a real photo detail; mere touching, a gap, or a neighboring shadow does not count.
6. Do not add hand-drawn accents, stickers, wind lines, doodles, or decorative marks by default. Add them only when the user explicitly asks; then read [references/visual-language.md](references/visual-language.md) and keep them on an independent layer that never changes the player silhouette. Read [references/layout-spec.md](references/layout-spec.md) before placing layers.
7. Inspect the final image at full size. Correct composition, text, aspect ratio, and over-decoration before delivery.

## Fixed Player Rules

- Use an original generic player; never reproduce the identifiable UI, branding, or logos of a music service.
- Preserve the selected player’s outer ratio, corner radius, cover frame, information zones, controls, and internal spacing through later iterations. Its position may adapt to the photograph.
- Lock the player outer frame to the measured reference ratio **473:835 width-to-height (0.5665)**. This is a non-negotiable invariant. Scale the complete player uniformly; never change its width or height independently.
- Lock the album cover to an exact **1:1 square**. Set its side to approximately **82.5% of the player width**. At the 473 × 835 reference size, use a 390 × 390 cover, about 43 px from the left edge, 40 px from the right edge, and 45 px from the top.
- Choose the player’s absolute size once from the canvas and composition, then keep that scale through later iterations. After selection, only move, recolor, or update its content unless the whole player is uniformly rescaled.
- Keep player content in this order: square photo crop, title, artist, optional short lyric/caption, progress/waveform, times, controls.
- Treat this internal layout as immutable after placement. Foreground overlap may hide any component; partial occlusion is intentional depth, not a layout error. Keep enough of the player visible to remain recognizable, but never relocate components around the subject.
- If a title is long, wrap or reduce its text size. Never widen the player to accommodate text.
- Render the card as borderless **frosted glass with a visible low-saturation tint**. Choose one base hue from the photograph, usually the nearby background hue or a close analogous hue, and carry it through the glass surface. The card must not read as pure white, neutral gray, or completely colorless glass. Use soft background diffusion, gentle local color bleed, low-contrast cloudy variation, and restrained depth. Preserve the exact outer silhouette and crisp rounded boundary even when the interior is softly blurred. Do not use an opaque flat slab when the background can plausibly show through.
- Keep the glass tint subtle: communicate the photograph's temperature and hue without turning the player into a saturated color block. Use cool low-saturation tints for quiet snow, fog, water, sky, or overcast scenes, and warm low-saturation tints for sun, wood, food, or intimate interiors.
- Keep player components nearly monochrome. Choose one readable neutral foreground color—warm white on dark glass or deep ink on light glass—and use it consistently for title, artist, lyric or caption, progress, times, and controls. Vary hierarchy mainly through size, weight, and opacity rather than assigning different hues to individual components.
- Allow at most one small source-derived accent only when it materially improves hierarchy. Limit it to one minor role, such as the played progress, progress knob, or play button; do not color several component groups at once. The accent is optional, should occupy little visual area, and must never compete with the subject or album cover.
- Preserve the album cover in the source photograph's natural colors; do not wash it with the glass tint or component color.
- Separate the atmosphere-matched card from its background through frosted-glass opacity, local blur, and a related value shift of about 12–20% before changing hue. Prefer a restrained internal gradient over a complementary-color block. Lock the chosen glass tint, neutral component color, and optional accent after placement; later movement, text updates, and foreground overlap must not trigger recoloring.
- Use a high-chroma tint across the whole card only as a last resort when value, opacity, blur, gradient, and placement still fail to separate it. Do not sacrifice the source mood merely to make the player louder.
- **Never add an outline, stroke, keyline, double border, rim, halo, or outer glow around the player.** If the borderless card lacks separation, adjust frosted-glass opacity, backdrop blur, local value, internal gradient, or placement instead.

## Subject and Cover Rules

- Preserve the original person, pet, or object’s recognizable appearance, pose, and photographic texture.
- Do not duplicate the foreground subject or make a new AI version of it.
- Do not shrink or move a centered person when their body touches or exits a canvas edge; doing so requires invented body or background. Adapt the player first.
- For a fully visible object or coherent object group, allow a restrained **1.05–1.12×** uniform enlargement anchored to its original ground/contact points when stronger foreground hierarchy is needed. Preserve the exact item count and structure.
- Require a visible foreground/midground boundary in every output: keep the player behind the exact original subject, coherent object group, foliage edge, tree trunk, furniture edge, or another source-native near-field detail. If one candidate cannot be extracted cleanly, choose another source-native foreground element or revise the layout. Do not deliver a non-overlapping card unless the user explicitly waives this rule.
- Allow a subtle shadow, glow, or 2–3 short motion marks near hair, fabric, or an accessory. Never trace the whole body with a sticker outline.
- Make album art a direct crop from the original photo. It must feel like a smaller memory from the same moment, not generated cover art.

## Composition Rules

- Start from the subject, then place the player in the least information-dense nearby region: wall, sky, pavement, water, shadow, plain fabric, or open architectural surface.
- Preserve a clear visual path from an image edge to the foreground subject. Do not block every roofline, road, gaze direction, or natural leading line.
- Prefer a three-point imbalance over strict centering: player near the visual middle, foreground subject offset to one side, and a small counterweight in the opposite open area.
- Make the player the primary graphic focus without forcing exact centering. Keep its centroid inside the central safe zone: approximately **30–70% of canvas width** and **28–68% of canvas height**. Keep every unoccluded card edge at least about **8% of the canvas** away from the corresponding outer edge. Never park a small player in a corner.
- Target roughly **22–25% of the canvas area** for the player; **18–30%** is the full adaptive range. Use 18–21% for a large centered person, 20–24% for a small object group, and 22–30% when broad low-information space exists. Reject an accidental player below 18%: restrained must not mean visually timid.
- On the default 3:4 portrait canvas, start near **41.5% of canvas width** and adapt within roughly **38–46%**. On an explicitly requested landscape canvas, start near **57.7% of canvas height** and adapt within roughly **52–64%**. Always derive the other dimension from 473:835.
- Use the smaller end of the range when the subject is already large or the scene is dense. Use the larger end when the subject is small and a broad low-information region is available. Choose once, then preserve the uniform scale.
- When the preferred subject is too small, crowded, or unreliable to extract, use another real near-field edge from the photograph and reposition the player. Never replace mandatory overlap with mere adjacency.
- Make the player and foreground subject read as one interlocked composition. For object groups, let two real edges or items cross the player boundary when possible instead of allowing a single weak corner touch.

## Final Checks

- Final output is exactly **1536 × 2048, 3:4 portrait**, unless the user explicitly requests another format or essential source content requires the documented original-ratio exception.
- Song title, artist, times, and lyric/caption are legible and correctly spelled.
- Album art is a real crop from the input photo and does not repeat the foreground subject.
- A clearly recognizable strip of a source-native foreground element covers the player edge; reject outputs where the player merely sits adjacent to the subject.
- Foreground overlap is applied after the complete player layout and may cover player text or controls. Reject outputs that shift, squeeze, or reorder components to create a clear area around the subject.
- At 25% thumbnail size, the player is the first graphic element noticed after the photographic subject. Reject a card that feels timid, peripheral, or parked in a corner.
- Player geometry is exactly 473:835, the cover is exactly square at about 82.5% of player width, and neither has been stretched since the layout was selected.
- No hand-drawn or sticker-like accents appear unless the user explicitly requested them.
- The player reads as borderless frosted glass with no visible outline or glow.
- The glass carries one perceptible low-saturation source hue, while player components remain nearly monochrome; any accent is optional, small, and confined to one role.
- Do not add watermarks, real app logos, extra people, or made-up text.
