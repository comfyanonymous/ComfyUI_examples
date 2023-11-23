# Noisy Latent Composition Examples

You can Load these images in [ComfyUI](https://github.com/comfyanonymous/ComfyUI) to get the full workflow.

Here are examples of Noisy Latent Composition. Noisy latent composition is when latents are composited together while still noisy before the image is fully denoised. Since general shapes like poses and subjects are denoised in the first sampling steps this lets us for example position subjects with specific poses anywhere on the image while keeping a great amount of consistency.

Here is an example. This example contains 4 images composited together. 1 background image and 3 subjects.
The total steps is 16. The latents are sampled for 4 steps with a different prompt for each. The background is 1920x1088 and the subjects are 384x768 each. After these 4 steps the images are still extremely noisy. The subjects are then composited (pasted) onto the background with some feathering applied. The rest of the sampling steps are then run on this composited image.


These examples are done with the WD1.5 beta 3 illusion model.

![Example](noisy_latents_3_subjects.png)

With the positions of the subjects changed:

![Example](noisy_latents_3_subjects_.png)

You can see that the subjects that were composited from different noisy latent images actually interact with each other because I put "holding hands" in the prompt. You'll also notice how consistent the background is which shows how powerful this method is.

This technique has some limitations in that it can't control details on subjects like eye color for example but it seems to work extremely well for subject position, pose and general color.
