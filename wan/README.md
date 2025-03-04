# Wan 2.1 Models

[Wan 2.1](https://github.com/Wan-Video/Wan2.1) is a family of video models.

## Update ComfyUI

Update ComfyUI to the latest version. Or, download the ComfyUI App. 

## Files to Download

You will first need:

#### Text encoder and VAE:

[umt5_xxl_fp8_e4m3fn_scaled.safetensors](https://huggingface.co/Comfy-Org/Wan_2.1_ComfyUI_repackaged/tree/main/split_files/text_encoders) goes in: ComfyUI/models/text_encoders/

[wan_2.1_vae.safetensors](https://huggingface.co/Comfy-Org/Wan_2.1_ComfyUI_repackaged/blob/main/split_files/vae/wan_2.1_vae.safetensors) goes in: ComfyUI/models/vae/


#### Video Models

The diffusion models can be found [here](https://huggingface.co/Comfy-Org/Wan_2.1_ComfyUI_repackaged/tree/main/split_files/diffusion_models)


These files go in: ComfyUI/models/diffusion_models/

These examples use the 16 bit files but you can use the fp8 ones instead if you don't have enough memory.

## Workflows

### Text to Video

This workflow requires the [wan2.1_t2v_1.3B_fp16.safetensors](https://huggingface.co/Comfy-Org/Wan_2.1_ComfyUI_repackaged/blob/main/split_files/diffusion_models/wan2.1_t2v_1.3B_fp16.safetensors) file (put it in: ComfyUI/models/diffusion_models/). You can also use it with the 14B model.

![Example](text_to_video_wan.webp)

[Workflow in Json format](text_to_video_wan.json)

### Image to Video

This workflow requires the [wan2.1_i2v_480p_14B_bf16.safetensors](https://huggingface.co/Comfy-Org/Wan_2.1_ComfyUI_repackaged/blob/main/split_files/diffusion_models/wan2.1_i2v_480p_14B_bf16.safetensors) file (put it in: ComfyUI/models/diffusion_models/) and 
[clip_vision_h.safetensors](https://huggingface.co/Comfy-Org/Wan_2.1_ComfyUI_repackaged/blob/main/split_files/clip_vision/clip_vision_h.safetensors) which goes in: ComfyUI/models/clip_vision/

Note this example only generates 33 frames at 512x512 because I wanted it to be accessible, the model can do more than that. The 720p model is pretty good if you have the hardware/patience to run it.

<img src="image_to_video_wan_example.webp" width="512" />

[Workflow in Json format](image_to_video_wan_example.json)

The input image can be found on the [flux](../flux) page.

Here's the same example with the 720p model:

<img src="image_to_video_wan_720p_example.webp" width="768" />
