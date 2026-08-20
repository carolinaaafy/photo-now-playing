# Layout Spec

Use this as the default arrangement; adapt placement to the source photo but preserve the relationships.

## Layer Order

1. Background: the source photo intelligently reframed into the default 3:4 portrait canvas without stretching; extend only simple low-detail regions when necessary.
2. Midground: a fixed-proportion portrait player.
3. Foreground: one extracted subject, coherent object group, or near-field photo detail. Place it above the player so a real part visibly hides the card boundary.
4. Do not add a decoration layer unless the user explicitly requests it. If requested, keep it independent from the locked player silhouette and foreground mask.

## Default Geometry

- Default to a **1536 × 2048, 3:4 portrait canvas** for consistent sharing. Reframe and uniformly scale rather than stretch. Preserve the source ratio only when essential content spans both horizontal edges and cannot survive portrait conversion.
- Use a tall player at the measured reference ratio **473:835 width:height (0.5665)**. Treat this as fixed template geometry across all output formats; only scale the entire card proportionally.
- Use an exact **1:1 album cover** whose side is approximately **82.5% of player width**. Normalized to the 473 × 835 player, the cover is 390 × 390 with approximate insets of 43 px left, 40 px right, and 45 px top.
- Target **22–25% of total canvas area** for the card. Use **18–21%** for a large centered person, **20–24%** for a small object group, and up to **30%** only when broad low-information space supports it. Do not accept an accidental card below 18%.
- For portrait or square canvases, begin with a card width near **43.5% of canvas width** and adapt within approximately **38–46%**. For landscape canvases, begin with a card height near **57.7% of canvas height** and adapt within approximately **52–64%**. Derive the remaining dimension from 473:835.
- Make the player smaller when the foreground subject is large or the background is visually dense. Make it larger when the subject is small and there is a broad low-information region. Once selected, preserve that scale unless the whole player is uniformly resized.
- Place the card near the visual middle, shifted toward the best low-information region.
- Keep the card centroid within approximately **30–70% of canvas width** and **28–68% of canvas height**, with about **8% minimum outer-edge clearance** wherever the card is not intentionally occluded. Reject corner parking.
- Keep a centered or edge-cropped person at the original scale and position. For a fully visible object group, permit a **1.05–1.12×** uniform enlargement anchored to the original ground/contact points.
- Treat overlap as a layer-mask requirement, not a proximity cue. Use 10–20% edge coverage for portraits and 20–35% lower-corner or side coverage for suitable object groups. Prefer two crossing subject edges or two group members over one weak corner touch.
- Give the frosted glass one perceptible low-saturation tint derived from the nearby background or a close analogous photo color; do not let it become pure white, neutral gray, or colorless. Keep the player components nearly monochrome in one readable warm-white or deep-ink foreground color. Allow at most one optional, small source-derived accent confined to a single role.
- Preserve atmosphere before pursuing hue contrast. When the player is close to the background color, first separate it through a 12–20% value shift, opacity, local blur, restrained gradient, and placement. Use a high-chroma tint across the entire player only if those measures still produce camouflage.
- Never add an outline, stroke, keyline, rim, halo, or outer glow. Keep the silhouette readable through the tinted glass surface and value separation alone.
- Use one small counterweight in the open side of the frame rather than centering all elements.

## Choosing Album Art

Choose a square crop with one clear environmental memory: framed sky, leaves, cup, signage, a window reflection, tabletop shadow, flower, animal detail, or architectural corner. Exclude the enlarged foreground subject from the crop.

## Avoid

- A player whose outer frame is not 473:835, whose cover is not square, or whose width is changed independently from its height.
- Card centered exactly over the main photo subject.
- Card parked in a corner or outside the central safe zone.
- A foreground cutout that floats without contact with the original ground.
- A subject merely touching the player, sitting beside it, or separated only by a shadow.
- Any output without a source-native foreground element visibly covering part of the card edge, unless the user explicitly waived overlap.
- Reusing the same person or object as both giant foreground subject and album cover.
- A timid player below 18% of canvas area without an explicit compositional reason.
