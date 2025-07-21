# HiDream

[HiDream I1](https://github.com/HiDream-ai/HiDream-I1) is a state of the art image diffusion model.

## Files to Download

Download the text encoder files:

* [clip_l_hidream.safetensors](https://huggingface.co/Comfy-Org/HiDream-I1_ComfyUI/blob/main/split_files/text_encoders/clip_l_hidream.safetensors)
* [clip_g_hidream.safetensors](https://huggingface.co/Comfy-Org/HiDream-I1_ComfyUI/blob/main/split_files/text_encoders/clip_g_hidream.safetensors)
* [t5xxl_fp8_e4m3fn_scaled.safetensors](https://huggingface.co/Comfy-Org/HiDream-I1_ComfyUI/blob/main/split_files/text_encoders/t5xxl_fp8_e4m3fn_scaled.safetensors)
* [llama_3.1_8b_instruct_fp8_scaled.safetensors](https://huggingface.co/Comfy-Org/HiDream-I1_ComfyUI/blob/main/split_files/text_encoders/llama_3.1_8b_instruct_fp8_scaled.safetensors)

Put these 4 files in your ComfyUI/models/text_encoders directory.

You can find them all: [here](https://huggingface.co/Comfy-Org/HiDream-I1_ComfyUI/tree/main/split_files/text_encoders). You might already have t5xxl downloaded.

The VAE can be found [here](https://huggingface.co/Comfy-Org/HiDream-I1_ComfyUI/blob/main/split_files/vae/ae.safetensors) and should go in your ComfyUI/models/vae/ folder. This is the Flux VAE so you might already have it.

The diffusion models can be found in this [folder](https://huggingface.co/Comfy-Org/HiDream-I1_ComfyUI/tree/main/split_files/diffusion_models)

## HiDream dev Workflow

Download [hidream_i1_dev_bf16.safetensors](https://huggingface.co/Comfy-Org/HiDream-I1_ComfyUI/blob/main/split_files/diffusion_models/hidream_i1_dev_bf16.safetensors) and put it in your ComfyUI/models/diffusion_models/ directory.

You can then load up or drag the following image in ComfyUI to get the workflow:

![Example](hidream_dev_example.png)

## HiDream full Workflow

Download [hidream_i1_full_fp16.safetensors](https://huggingface.co/Comfy-Org/HiDream-I1_ComfyUI/blob/main/split_files/diffusion_models/hidream_i1_full_fp16.safetensors) and put it in your ComfyUI/models/diffusion_models/ directory.

You can then load up or drag the following image in ComfyUI to get the workflow:

![Example](hidream_full_example.png)

## HiDream e1.1

This is an edit model, download [hidream_e1_1_bf16.safetensors](https://huggingface.co/Comfy-Org/HiDream-I1_ComfyUI/blob/main/split_files/diffusion_models/hidream_e1_1_bf16.safetensors) and put it in your ComfyUI/models/diffusion_models/ directory.

You can then load up or drag the following image in ComfyUI to get the workflow:

![Example](hidream_e1.1_example.png)


<details>
<summary>Old hidream 1.0 edit model.</summary>
## HiDream e1

This is an experimental edit model, download [hidream_e1_full_bf16.safetensors](https://huggingface.co/Comfy-Org/HiDream-I1_ComfyUI/blob/main/split_files/diffusion_models/hidream_e1_full_bf16.safetensors) and put it in your ComfyUI/models/diffusion_models/ directory.

You can then load up or drag the following image in ComfyUI to get the workflow:

![Example](hidream_e1_example.png)
</details>
