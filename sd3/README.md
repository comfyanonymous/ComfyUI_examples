# SD3 Examples

The SD3 checkpoints that contain text encoders: [sd3_medium_incl_clips.safetensors (5.5GB)](https://huggingface.co/stabilityai/stable-diffusion-3-medium/tree/main) and [sd3_medium_incl_clips_t5xxlfp8.safetensors (10.1GB)](https://huggingface.co/stabilityai/stable-diffusion-3-medium/tree/main) can be used like any regular checkpoint in ComfyUI. The difference between both these checkpoints is that the first contains only 2 text encoders: CLIP-L and CLIP-G while the other one contains 3: CLIP-L, CLIP-G and T5XXL. Make sure to put either sd3_medium_incl_clips.safetensors or sd3_medium_incl_clips_t5xxlfp8.safetensors in your ComfyUI/models/checkpoints/ directory.

Here is a very basic example how to use it:

![Example](sd3_simple_example.png)

The [sd3_medium.safetensors](https://huggingface.co/stabilityai/stable-diffusion-3-medium/tree/main) file does not contain text encoder/CLIP weights so you must load them separately to use that file. Download the text encoder weights from the [text_encoders directory](https://huggingface.co/stabilityai/stable-diffusion-3-medium/tree/main) and put them in your ComfyUI/models/clip/ directory. sd3_medium.safetensors should be put in your ComfyUI/models/checkpoints/ directory.

Here is a basic example how to use it:

![Example](sd3_text_encoders_example.png)

As a reminder you can save these image files and drag or load them into ComfyUI to get the workflow.

SD3 performs very well with the negative conditioning zeroed out like in the following example:

![Example](sd3_anime_example.png)

### SD3 Controlnet

SD3 Controlnets by [InstantX](https://huggingface.co/InstantX) are also supported. Download the canny controlnet model [here](https://huggingface.co/InstantX/SD3-Controlnet-Canny/blob/main/diffusion_pytorch_model.safetensors), and put it in your ComfyUI/models/controlnet directory. Be sure to rename it to something clear like sd3_controlnet_canny.safetensors.

Here is an example of how to use it:
![Example](sd3_controlnet_example.png)
