# SD3 Examples

## SD3.5

The first step is downloading the text encoder files if you don't have them already from SD3, Flux or other models: ([clip_l.safetensors](https://huggingface.co/Comfy-Org/stable-diffusion-3.5-fp8/blob/main/text_encoders/clip_l.safetensors), [clip_g.safetensors](https://huggingface.co/Comfy-Org/stable-diffusion-3.5-fp8/blob/main/text_encoders/clip_g.safetensors) and t5xxl) if you don't have them already in your ComfyUI/models/clip/ folder. For the t5xxl I recommend [t5xxl_fp16.safetensors](https://huggingface.co/Comfy-Org/stable-diffusion-3.5-fp8/blob/main/text_encoders/t5xxl_fp16.safetensors) if you have more than 32GB ram or [t5xxl_fp8_e4m3fn_scaled.safetensors](https://huggingface.co/Comfy-Org/stable-diffusion-3.5-fp8/blob/main/text_encoders/t5xxl_fp8_e4m3fn_scaled.safetensors) if you don't.

The SD3.5 model family contains a large 8B model and a medium 2.5B model. The medium model will be faster and take less memory but might have less complex understanding of some concepts. I recommend downloading both and experimenting with how each of them respond to your prompts.

The [sd3.5_large.safetensors](https://huggingface.co/stabilityai/stable-diffusion-3.5-large/tree/main) and [sd3.5_medium.safetensors](https://huggingface.co/stabilityai/stable-diffusion-3.5-medium/tree/main) files (pick the one you want and put it in your ComfyUI/models/checkpoints/ directory) do not contain text encoder/CLIP weights so you must load them separately to use that file just like in the following example:

![Example](sd3.5_text_encoders_example.png)

To use the [sd3.5_large_turbo.safetensors](https://huggingface.co/stabilityai/stable-diffusion-3.5-large-turbo/tree/main) file (put it in your ComfyUI/models/checkpoints/ directory) you can use the above example and set steps to 4 and cfg to 1.2.

For convenience there is an easy to use all in one checkpoint file [sd3.5_large_fp8_scaled.safetensors](https://huggingface.co/Comfy-Org/stable-diffusion-3.5-fp8/blob/main/sd3.5_large_fp8_scaled.safetensors) (put it in your ComfyUI/models/checkpoints/ directory) that can be used in the default workflow like any other checkpoint files. There is also one for SD3.5 medium: [sd3.5_medium_incl_clips_t5xxlfp8scaled.safetensors](https://huggingface.co/Comfy-Org/stable-diffusion-3.5-fp8/blob/main/sd3.5_medium_incl_clips_t5xxlfp8scaled.safetensors)

See this workflow for an example.

![Example](sd3.5_simple_example.png)

As a reminder you can save these image files and drag or load them into ComfyUI to get the workflow.

### SD3.5 Controlnets

Stability has released some official SD3.5 controlnets that you can find [here](https://huggingface.co/stabilityai/stable-diffusion-3.5-controlnets) these files (sd3.5_large_controlnet_canny.safetensors, sd3.5_large_controlnet_depth.safetensors, sd3.5_large_controlnet_blur.safetensors) go in your ComfyUI/models/controlnet directory and are meant to be used with SD3.5 large.

See this workflow for an example with the canny ([sd3.5_large_controlnet_canny.safetensors](https://huggingface.co/stabilityai/stable-diffusion-3.5-controlnets/tree/main)) controlnet:

![Example](sd3.5_large_canny_controlnet_example.png)


[Old SD3 medium examples](README_old.md)


