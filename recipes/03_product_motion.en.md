# 03 — Separate product movement from camera movement

[Korean](03_product_motion.md) | **English**

Status: **experimental / actual video generation and frame review not yet performed**.

## The problem

When the product rotates, the camera moves, and the lights shift in the same request, it is difficult to distinguish the causes of the result. Compare **a fixed camera with partial product rotation** and **a fixed product with a camera approach** separately.

![Illustrative plan for two kinds of movement](../assets/motion_plan.png)

This image was created with the built-in image generation tool to explain planned product and camera motion. It does not show the beginning, middle, or end of an actual video. The circular arrow on the left indicates the direction of a partial rotation, not an instruction for a full 360-degree spin.

## Prepare the starting image

1. The default input is the fictional AI-generated product in `assets/metal_reference.png`. If you generated an additional image with recipe 02, you may substitute one whose shape passes review. Record the selected file and settings. See [the motion brief](../examples/03_product_motion.en.json).
2. Use the same starting image for both video conditions. A small stationary block beside the base and a larger stationary block behind it make parallax easier to inspect. If you add them, use the same modified image for both conditions.
3. Do not use the entire `motion_plan.png` teaching board as the product identity input. Start from the product PNG. A front-facing reference cannot validate the accuracy of unseen surfaces.
4. If the model does not support four seconds, choose a supported duration and match both conditions. Four seconds is a design choice, not a claim of an optimal duration.

See [S3 and S4](../SOURCES.en.md) for photography and 3D examples of camera movement along a path. Testing one kind of motion at a time is this collection's review approach.

## Condition A — fixed camera, partial product rotation

```text
Use the attached approved image as the exact first-frame reference. Make a four-second continuous product shot. The camera position, framing, focal length, background, and studio lights remain fixed. Only the cylindrical product rotates gently in place by approximately fifteen degrees around its own vertical center axis, then settles. Preserve the product's proportions, top rim, base, and surface identity throughout. The support surface and all background objects remain stationary. Let reflections respond to the product's rotation rather than adding moving lights. End with a brief stable hold. This is a partial reveal, not a full 360-degree spin. Use a silent shot when the tool supports audio controls.
```

Begin with a small rotation that keeps the front prominent because no reference is available to verify unseen surfaces. Fifteen degrees is a comparison design choice, not a guaranteed preservation threshold.

## Condition B — fixed product, camera approach

```text
Use the same approved image as the exact first-frame reference. Make a four-second continuous product shot. The cylindrical product, support surface, background objects, and studio lights remain stationary. Only the camera moves gently forward toward the product along a straight path, without orbiting or tilting. Keep the focal length constant. Maintain focus on the product and preserve its proportions, top rim, base, and surface identity. The product becomes slightly larger in frame, while near and far objects show coherent perspective change. End with a brief stable hold. Use a silent shot when the tool supports audio controls.
```

A model can produce simple enlargement even when camera movement was requested. Without cues at different depths, there is insufficient evidence to distinguish translation from zooming or scaling; mark that check as undetermined.

## Comparison order

`prompts/03_motion_baseline.txt` is the baseline containing a combined request. Baseline versus A/B is an exploratory comparison that changes several instructions. Do not rank A universally above B. First check whether each follows its intended motion, then change only rotation amount or camera travel within the same condition.

## Review the entire video

| Check | Expected in A | Expected in B |
|---|---|---|
| Background | Position stays fixed in the frame | A stationary scene changes its projection as the camera approaches |
| Product | Partial rotation around a stable center axis | Stays in place without rotating |
| Shape | Rim, base, and proportions survive every frame | Rim, base, and proportions survive every frame |
| Reflections | May change with rotation under fixed lighting | May change with camera viewpoint |
| Ending | Rotation finishes with a stable hold | Approach finishes with a stable hold |

Check the beginning, middle, and end, then play the whole video continuously. Correct representative frames do not make the shot pass if the product melts or the background drifts between them. Record both frame samples and whether full playback was reviewed.

## What to do after a failure

- If the background flows as the product rotates, check the fixed-camera condition first.
- If the product stretches or gains new parts, check the starting image and preservation criteria before reducing motion.
- If the camera approach is just enlargement, record it as `zoom-like`. Add depth cues or verify with 3D using an actual camera path.
- Use 3D or real photography when exact rotation or parallax is required. If you substitute 2D scaling animation, label it as digital enlargement.

## Record the experiment

None of the three video conditions has been run yet. Record the model, duration, seed, starting image, motion strength, and audio settings, and attach the outputs using [experiment_record.json](../templates/experiment_record.json). Do not count videos with different input conditions as the same reproducibility experiment.
