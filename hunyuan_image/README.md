# Hunyuan Image 2,1

[Hunyuan Image 2.1](https://huggingface.co/tencent/HunyuanImage-2.1) is a powerful diffusion model for image generation.

## Basic Workflow

Download the following models and place them in the appropriate ComfyUI directories:

### Text Encoders
Download and put in your ComfyUI/models/text_encoders directory:
- [byt5_small_glyphxl_fp16.safetensors](https://huggingface.co/Comfy-Org/HunyuanImage_2.1_ComfyUI/blob/main/split_files/text_encoders/byt5_small_glyphxl_fp16.safetensors)
- [qwen_2.5_vl_7b.safetensors](https://huggingface.co/Comfy-Org/HunyuanImage_2.1_ComfyUI/blob/main/split_files/text_encoders/qwen_2.5_vl_7b.safetensors)

### VAE Models
Download and put in your ComfyUI/models/vae directory:
- [hunyuan_image_2.1_vae_fp16.safetensors](https://huggingface.co/Comfy-Org/HunyuanImage_2.1_ComfyUI/blob/main/split_files/vae/hunyuan_image_2.1_vae_fp16.safetensors)
- **Optional (for refiner):** [hunyuan_image_refiner_vae_fp16.safetensors](https://huggingface.co/Comfy-Org/HunyuanImage_2.1_ComfyUI/blob/main/split_files/vae/hunyuan_image_refiner_vae_fp16.safetensors)

### Diffusion Models
Download and put in your ComfyUI/models/diffusion_models directory:
- [hunyuanimage2.1_bf16.safetensors](https://huggingface.co/Comfy-Org/HunyuanImage_2.1_ComfyUI/blob/main/split_files/diffusion_models/hunyuanimage2.1_bf16.safetensors)
- **Optional (for refiner):** [hunyuanimage2.1_refiner_bf16.safetensors](https://huggingface.co/Comfy-Org/HunyuanImage_2.1_ComfyUI/blob/main/split_files/diffusion_models/hunyuanimage2.1_refiner_bf16.safetensors)

You can then load up or drag the following image in ComfyUI to get the workflow:

![Example](hunyuan_image_example.png)
