# 2 Pass Txt2Img (Hires fix) Examples

These are examples demonstrating how you can achieve the "Hires Fix" feature.

You can Load these images in [ComfyUI](https://github.com/comfyanonymous/ComfyUI) to get the full workflow.

Hires fix is just creating an image at a lower resolution, upscaling it and then sending it through img2img. Note that in ComfyUI txt2img and img2img are the same node. Txt2Img is achieved by passing an empty image to the sampler node with maximum denoise.

Here's a simple workflow in ComfyUI to do this:

![Example](hiresfix_latent_workflow.png)

Here is an image generated with this workflow:

![Example](sd1.5_latent_upscale.png)

Here is an example of a more complex 2 pass workflow, This image is first generated with the Anything-V3.0 model, latent upscaled and then a second pass is done with AbyssOrangeMix2_hard:

![Example](latent_upscale_different_prompt_model.png)

![Example](latent_upscale_different_prompt_model_2.png)
