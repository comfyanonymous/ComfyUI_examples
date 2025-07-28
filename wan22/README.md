# Wan 2.2 Models

[Wan 2.2](https://github.com/Wan-Video/Wan2.2) is a family of video models and the version after [Wan 2.1](../wan)

Wan2.2 is initially released with 3 different models, a 5B model that can do both text and image to video and two 14B models, one for text to video and the other for video to video.

See also the [Comfy Docs Wan 2.2 page for more workflow examples.](https://docs.comfy.org/tutorials/video/wan/wan2_2)

## Files to Download

You will first need:

#### Text encoder and VAE:

[umt5_xxl_fp8_e4m3fn_scaled.safetensors](https://huggingface.co/Comfy-Org/Wan_2.2_ComfyUI_Repackaged/tree/main/split_files/text_encoders) goes in: ComfyUI/models/text_encoders/

Needed for the 14B models: [wan_2.1_vae.safetensors](https://huggingface.co/Comfy-Org/Wan_2.2_ComfyUI_Repackaged/blob/main/split_files/vae/wan_2.1_vae.safetensors) goes in: ComfyUI/models/vae/

Needed for the 5B model (NEW): [wan2.2_vae.safetensors](https://huggingface.co/Comfy-Org/Wan_2.2_ComfyUI_Repackaged/blob/main/split_files/vae/wan2.2_vae.safetensors) goes in: ComfyUI/models/vae/

#### Video Models

The diffusion models can be found [here](https://huggingface.co/Comfy-Org/Wan_2.2_ComfyUI_Repackaged/tree/main/split_files/diffusion_models)

These files go in: ComfyUI/models/diffusion_models/

## Workflows

### 5B Model

This workflow requires the [wan2.2_ti2v_5B_fp16.safetensors](https://huggingface.co/Comfy-Org/Wan_2.2_ComfyUI_Repackaged/blob/main/split_files/diffusion_models/wan2.2_ti2v_5B_fp16.safetensors) file (put it in: ComfyUI/models/diffusion_models/).

Make sure you have the [wan2.2 VAE](https://huggingface.co/Comfy-Org/Wan_2.2_ComfyUI_Repackaged/blob/main/split_files/vae/wan2.2_vae.safetensors) (goes in: ComfyUI/models/vae/)

#### Text to video

![Example](text_to_video_wan22_5B.webp)

[Workflow in Json format](text_to_video_wan22_5B.json)


#### Image to Video

![Example](image_to_video_wan22_5B.webp)

[Workflow in Json format](image_to_video_wan22_5B.json)

You can find the input image [here](../chroma/fennec_girl_hug.png)

### 14B Model

Make sure you have the [wan2.1 VAE](https://huggingface.co/Comfy-Org/Wan_2.2_ComfyUI_Repackaged/blob/main/split_files/vae/wan_2.1_vae.safetensors) (goes in: ComfyUI/models/vae/)

#### Text to video

This workflow requires both the [wan2.2_t2v_high_noise_14B_fp8_scaled.safetensors](https://huggingface.co/Comfy-Org/Wan_2.2_ComfyUI_Repackaged/blob/main/split_files/diffusion_models/wan2.2_t2v_high_noise_14B_fp8_scaled.safetensors) and the [wan2.2_t2v_low_noise_14B_fp8_scaled.safetensors](https://huggingface.co/Comfy-Org/Wan_2.2_ComfyUI_Repackaged/blob/main/split_files/diffusion_models/wan2.2_t2v_low_noise_14B_fp8_scaled.safetensors) file (put it in: ComfyUI/models/diffusion_models/).

![Example](text_to_video_wan22_14B.webp)

[Workflow in Json format](text_to_video_wan22_14B.json)

#### Image to Video

This workflow requires both the [wan2.2_i2v_high_noise_14B_fp8_scaled.safetensors](https://huggingface.co/Comfy-Org/Wan_2.2_ComfyUI_Repackaged/blob/main/split_files/diffusion_models/wan2.2_i2v_high_noise_14B_fp8_scaled.safetensors) and the [wan2.2_i2v_low_noise_14B_fp8_scaled.safetensors](https://huggingface.co/Comfy-Org/Wan_2.2_ComfyUI_Repackaged/blob/main/split_files/diffusion_models/wan2.2_i2v_low_noise_14B_fp8_scaled.safetensors) file (put it in: ComfyUI/models/diffusion_models/).

![Example](image_to_video_wan22_14B.webp)

[Workflow in Json format](image_to_video_wan22_14B.json)

You can find the input image [here](../chroma/fennec_girl_flowers.png)
