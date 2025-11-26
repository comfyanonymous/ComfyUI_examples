# Z Image

[Z Image Turbo](https://huggingface.co/Tongyi-MAI/Z-Image-Turbo) is a fast distilled diffusion model.

## Files to Download

Text encoder file: [qwen_3_4b.safetensors](https://huggingface.co/Comfy-Org/z_image_turbo/blob/main/split_files/text_encoders/qwen_3_4b.safetensors) (goes in ComfyUI/models/text_encoders/).

diffusion model file: [z_image_turbo_bf16.safetensors](https://huggingface.co/Comfy-Org/z_image_turbo/blob/main/split_files/diffusion_models/z_image_turbo_bf16.safetensors) (goes in ComfyUI/models/diffusion_models/).

VAE: [ae.safetensors](https://huggingface.co/Comfy-Org/z_image_turbo/blob/main/split_files/vae/ae.safetensors) the Flux 1 VAE if you don't have it already (goes in ComfyUI/models/vae/)

## Basic Example Workflow

You can then load up or drag the following image in ComfyUI to get the workflow:

![Example](z_image_turbo_example.png)
