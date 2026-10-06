# 02 — Organize highlights on a metal product

[Korean](02_metal_highlights.md) | **English**

Status: **experimental / recipe comparison results not yet verified**. The failures below are anticipated checks, not recorded experimental observations.

## The problem

A request for "premium metal" can introduce arbitrary reflections, scratches, or color changes, or produce an object that looks like gray plastic. Describe the **structure of the reflection band** as well as the material, then compare results on the same shape.

## Input and preservation criteria

![AI-generated fictional metal product reference](../assets/metal_reference.png)

This fictional satin-silver product reference was created with the built-in image generation tool. It is not a real product photograph, a measurement of metallic properties, or a result from a comparison under the same conditions. The intended material is satin silver. Keep the shape, height-to-width ratio, top rim, and base position fixed. Do not mix chrome, painted, or brushed finishes into this comparison.

## Read the reflections

![Illustrative metal reflection plan](../assets/metal_lighting.png)

This explanatory image was made with a separate AI generation request. First check whether a broad, continuous bright band and a dark edge make the curvature readable. Keep the illustration separate from results of the prompt below. See [S2](../SOURCES.en.md) for background on roughness and metallic properties as distinct attributes. This does not mean a generation prompt implements physical shader values exactly.

## Run it

1. Read [the metal brief](../examples/02_metal_highlights.en.json) for the input and preservation criteria.
2. Compare `prompts/02_metal_baseline.txt` with `02_metal_controlled.txt` using the same input, model, and output size.
3. If the difference is large, record it as an exploratory result for the full instruction set. Do not attribute the change to one particular sentence.
4. Within the controlled condition, change only the width of the reflection band for a second comparison. Keep the metal type, color, and camera unchanged.

## Copyable prompt

```text
Use the attached fictional AI-generated product image as the reference for geometry, proportions, rim, and satin silver material. Change only the lighting and reflection structure. Show one unbranded cylindrical product made of silver satin metal. Preserve its silhouette, height-to-width ratio, top rim, and base position. Keep the surface color consistent. Describe the curved body through one broad, continuous vertical reflection that fades gently into a darker side. Keep the highlight below clipping so the surface transition remains visible. Use a quiet neutral background and a matte support surface with a coherent contact shadow. The surface has fine restrained texture, not deep scratches. Reflections should describe the cylinder's curvature rather than introduce new painted stripes or scenery. Keep the whole product in frame. Output a single 3:4 studio product image.
```

## Review and adjust

| Check | Failure | Next adjustment |
|---|---|---|
| Shape | Top rim, width, or height changes | Fix the reference input method and preserved regions first |
| Reflection continuity | The band breaks apart or directions conflict | Reduce the instruction to one band and remove decorative lighting or background props |
| Surface color | The bright band becomes a painted stripe or a color stain | Distinguish a consistent silver material from brightness changes caused by lighting |
| Metal appearance | Little reflection remains and the object reads as a gray block | Separate the bright area and dark edge. Changing metal type belongs in a later, separate experiment |
| Excessive grain | Scratches look like product damage | Weaken or remove the fine-grain instruction and record the change |

Do not claim to identify an actual metal type from a small still image alone. When exact product color or machining marks must survive, compare against real product photographs or a 3D material reference.

## When to move to post-production

Consider retouching when the product shape is stable and only reflection cleanup remains. Move to real photography or 3D when accurate shape, exact parts, or real metal behavior are delivery requirements. A longer prompt is not the only remedy.

## Record the experiment

No baseline/controlled comparisons under the same conditions have been run yet. The attached images are separately generated reference assets. Record all outputs, settings, shape/reflection/material checks, and the single variable changed in a follow-up experiment. Use [experiment_record.json](../templates/experiment_record.json).
