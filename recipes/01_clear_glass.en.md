# 01 — Preserve a clear container's outline and label

[Korean](01_clear_glass.md) | **English**

Status: **experimental / recipe comparison results not yet verified**. The failure cases below are things to check for, not observations from completed experiments in this collection.

## The problem

A transparent container can disappear into its background, while changes in mood can alter the bottle's proportions, cap, or label. First preserve the product's identity, then compare lighting choices.

## Preserve and vary

| Preserve | Try changing |
|---|---|
| Bottle silhouette, height-to-width ratio, cap size, label position, and front-facing composition | Light or dark background, reflection brightness and width, and separation from the background |
| Number and placement of the two label bars and the small mark | Background and lighting while keeping the glass material |

![AI-generated fictional glass bottle reference](../assets/bottle_reference.png)

This **fictional glass bottle reference** was created with the built-in image generation tool. It is not a real product photograph or a result from a comparison under the same conditions. Use it to test preservation of shape, glass material, and a label layout without lettering. Preserving real lettering requires a separate experiment with the original label artwork and a character-by-character check.

## Choose a lighting direction

![Illustrative clear glass lighting plan](../assets/glass_lighting.png)

- **Light background:** request dark edge contrast so the transparent object's boundary remains readable against a bright background.
- **Dark background:** request long, continuous bright edges that reveal the container's outline.
- These are different intentions. Do not ask for both backgrounds in one prompt.

See [S1](../SOURCES.en.md) for a glass photography example that treats the diffused background and strip lighting separately. The illustration and prompts here are this collection's comparison design, not a reproduction of that setup. The teaching image was made with a separate image generation request; it is not an output of the prompt below.

## Run it

1. Read [the glass brief](../examples/01_clear_glass.en.json) and attach the product PNG as a shape and material reference.
2. Generate a baseline using `prompts/01_glass_baseline.txt`.
3. Run `01_glass_bright.txt` and `01_glass_dark.txt` separately with the same input, model, and output size.
4. Use the same seed if supported, and retain every result and its settings. Light versus dark backgrounds compare two approaches; this is not a causal test of one lighting variable.
5. Within the selected approach, change only the requested edge width for a follow-up comparison. Keep everything else fixed.

## Copyable prompt — light background

```text
Use the attached fictional AI-generated product image as the reference for geometry, proportions, cap, label layout, and glass material. Change only the background and lighting. Show one clear glass bottle in the same front-facing pose. Preserve its silhouette, proportions, cap size, and the position of the plain white label with its two gray bars and small circular mark. Render a neutral studio product image on a softly illuminated light background. Define the glass boundary with restrained dark edge contrast. Keep the central label unobstructed and the cap clearly separated from the bottle. The bottle rests on a matte surface with one coherent contact shadow. Preserve the reference glass material while changing the lighting. Keep the full product inside the frame with comfortable margins. Output a single 3:4 image.
```

## Review and repair order

| Check | Failure | Next adjustment |
|---|---|---|
| Shape | The bottle stretches, the cap changes size, or the label moves | Pause the lighting experiment. Check reference strength, editing masks, and the input method first |
| Outline | One edge disappears or the bottle becomes asymmetric | Keep the chosen light/dark approach and adjust only edge contrast |
| Label | A reflection covers the center or the number of marks changes | Restate preservation of the central label area. Composite the original artwork when exactness matters |
| Refraction and contact | The container appears doubled or floats above the surface | Assess whether a local edit is enough. Move to 3D or real photography when shape and optical accuracy are essential |

Inspect the label at a larger scale. Numerous bright lines alone do not make the glass treatment pass. The bottle boundary, cap, and central information must all remain readable.

## Record the experiment

No baseline/bright/dark comparisons under the same conditions have been recorded yet. The attached product and teaching images are separately generated reference assets. Record every result and each pass, fail, or undetermined check in [experiment_record.json](../templates/experiment_record.json). If you use a new reference image, also record its source and role.
