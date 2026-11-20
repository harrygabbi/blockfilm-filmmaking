---
name: blockfilm-filmmaking
description: Create and improve narrative Roblox-style shorts in BlockFilm Studio using its approved rounded cast, supplied narration, expressive animation, colorful town and camera coverage. Use for this user's BlockFilm films, character and town previews, and reference-driven production improvements.
---

# BlockFilm filmmaking

Resolve BlockFilm Studio relative to the user's workspace and inspect its current code and requested deliverable before editing.

## Approved project choices

The user approved the Town and Cast preview with Liam, Mom, Skye and Ash as the reusable cast. Their presets live in src/project.ts and their shapes in src/rig.ts, src/rig-form.ts and src/rig-hair.ts. Reuse these presets and preserve identity across shots and age changes. Rounded heads, beveled limbs, curved grips and layered hair are established preferences. When asked to improve appearance, change the underlying shape as needed. Check hair from the front, profile, back and above, including the film's tightest angles. The scalp shell should cover gaps beneath the locks without obscuring the face.

Oakridge's approved town uses colorful façades, terracotta and slate roofs, greenery and details informed by real streetscapes. src/liam-town.ts builds it. The Clear Day preset in src/look.ts reduces aerial haze while retaining depth. Check street-level color and the establishing view. Gastown and Columbia Street are recorded architecture references for proportions, materials and details.

The preview is public/demo/afraid-to-love-town-preview.blockfilm and the full narrated film is public/demo/afraid-to-love.blockfilm. A request for a short visual example should produce a separate editable preview and matching MP4. Infer audio needs from the request and supplied material.

## Reference review

Read [references/youtube-compilation.md](references/youtube-compilation.md) when applying the user's YouTube reference to acting, framing, hair, lighting or captions. It distinguishes observed samples from suggested production values.

Inspect linked or uploaded sources before drawing conclusions. Record player timestamps and visible changes. Consecutive frames help judge speed, while a single image can establish appearance. Describe the coverage actually reviewed. Retain approved cast and setting decisions when combining references. A compilation may contain several incompatible art directions.

## Acting and timing

Map narration to observable events such as a hand landing on a sleeve, a card breaking, eyes opening or a foot kicking a ball. Use supplied audio as the timing source and retain natural pauses.

The user repeatedly requested quicker character movement. Build a short anticipation, decisive movement, readable end pose and small settling motion for each action. Starting values for this project's brisk reactions are 0.15–0.35 seconds of anticipation and 0.2–0.5 seconds to execute a gesture or recoil, followed by a hold appropriate to the narration. These are adjustable production values. Emotional holds can last longer after an action lands.

Change root travel and limb timing together for walks and runs. Increasing a clip's speed alone can leave the character sliding slowly across the scene. Match footsteps to distance covered, end locomotion near arrival and use a planted pose during a pause. Avoid interpolating one gesture gradually across an entire sentence. Explicit duplicate hold keys followed by closely spaced action keys in src/liam.ts control that distinction.

Give faces different silhouettes through lids, brow angle and mouth shape. Pair a face change with a head turn, weight shift, elbow position or hand gesture. Maintain eye direction toward the person or prop that matters. Stagger starts and poses for crowds.

## Staging and coverage

Place actors and props, define contact and end positions, then frame them. Use existing director guidance when the user invokes it.

Use establishing views to explain location and travel, full or medium shots to show action, inserts to show contact or effects, and close reactions to show the consequence. Change framing when the information changes.

For a drone opening, choose a continuous route through the built town toward an identifiable destination. Review intermediate positions for roof collisions, abrupt speed changes and empty map edges. Carry a landmark such as the café awning or crosswalk through the descent. End with enough screen time at street level to judge the characters.

During hugs and exchanges, inspect actual hand and elbow positions in world space. Keep faces and the contact point visible. Root motion, forearm motion and camera framing must agree on the contact. Effects should originate from the visible surface and progress through contact, surface change, fragments and reaction.

## Color and lighting

Use material color, light direction, exposure and fog together. Check whether exposure is clipping cream trim or washing out façades. Give surfaces material-appropriate roughness and use sRGB for painted color textures. Keep faces readable against saturated backgrounds and separate dark hair from dark interiors.

Select environmental props that explain the place or action. Proportioned doors, window depth, cornices, awnings, pavement joints and believable setbacks contribute more than indiscriminate detail. Review the largest establishing frame and closest storefront frame.

## Delivery and verification

Reuse src/stage.ts, src/animation.ts, src/audio.ts and src/export.ts for editable playback and export. Keep permanent production logic in the repository. Inspect temporary render harnesses before reuse.

Before a full render, inspect contact sheets around important audio cues and sample motion during a fast action. Verify geometry coverage and framing after the latest changes. Decode the final MP4 and check requested dimensions, frame rate, frame count and duration with ffprobe. The current exporter targets 30 fps.

Verify supplied narration in the encoded delivery across early, middle and late cues. This project previously exhibited a 44 ms AAC offset in browser export. When replacing video, reusing a previously verified audio stream can preserve alignment. Check final duration and sync after muxing or re-encoding.

Run npm run build for TypeScript and production validation. Verify the editable project opens through the normal studio menu or import flow with the intended cast, shot coverage and duration. Return direct local video and editable-project links when requested. Disclose meaningful assumptions and unverified work.
