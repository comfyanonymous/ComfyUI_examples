# HiDream

[HiDream I1](https://github.com/HiDream-ai/HiDream-I1) is a state of the art image diffusion model.

## Files to Download

Download the clip_l_hidream.safetensors, clip_g_hidream.safetensors, t5xxl_fp8_e4m3fn_scaled.safetensors and llama_3.1_8b_instruct_fp8_scaled.safetensors files from [here](https://huggingface.co/Comfy-Org/HiDream-I1_ComfyUI/tree/main/split_files/text_encoders and put them in your ComfyUI/models/text_encoders directory. You might already have t5xxl downloaded.

The VAE can be found [here](https://huggingface.co/Comfy-Org/HiDream-I1_ComfyUI/blob/main/split_files/vae/ae.safetensors) and should go in your ComfyUI/models/vae/ folder. This is the Flux VAE so you might already have it.

The diffusion models can be found in this [folder](https://huggingface.co/Comfy-Org/HiDream-I1_ComfyUI/tree/main/split_files/diffusion_models)

## HiDream dev Workflow

Download [hidream_i1_dev_bf16.safetensors](https://huggingface.co/Comfy-Org/HiDream-I1_ComfyUI/blob/main/split_files/diffusion_models/hidream_i1_dev_bf16.safetensors) and put it in your ComfyUI/models/diffusion_models/ directory.

You can then load up or drag the following image in ComfyUI to get the workflow:

![Example](hidream_dev_example.png)
