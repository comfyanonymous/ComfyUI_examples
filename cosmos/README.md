# Nvidia Cosmos Models

[Nvidia Cosmos](https://www.nvidia.com/en-us/ai/cosmos/) is a family of "World Models". ComfyUI currently supports specifically the 7B and 14B text to video diffusion models and the 7B and 14B image to video diffusion models.

## Files to Download

You will first need:

#### Text encoder and VAE:

[oldt5_xxl_fp8_e4m3fn_scaled.safetensors](https://huggingface.co/comfyanonymous/cosmos_1.0_text_encoder_and_VAE_ComfyUI/tree/main/text_encoders) goes in: ComfyUI/models/text_encoders/

[cosmos_cv8x8x8_1.0.safetensors](https://huggingface.co/comfyanonymous/cosmos_1.0_text_encoder_and_VAE_ComfyUI/blob/main/vae/cosmos_cv8x8x8_1.0.safetensors) goes in: ComfyUI/models/vae/

Note: oldt5_xxl is not the same as the t5xxl used in flux and other models. 
oldt5_xxl is t5xxl 1.0 while the one used in flux and others is t5xxl 1.1

#### Video Models

The video models can be found [in safetensors format here.](https://huggingface.co/mcmonkey/cosmos-1.0/tree/main)

The workflows on this page use [Cosmos-1_0-Diffusion-7B-Text2World.safetensors](https://huggingface.co/mcmonkey/cosmos-1.0/blob/main/Cosmos-1_0-Diffusion-7B-Text2World.safetensors) and [Cosmos-1_0-Diffusion-7B-Video2World.safetensors](https://huggingface.co/mcmonkey/cosmos-1.0/blob/main/Cosmos-1_0-Diffusion-7B-Video2World.safetensors)

These files go in: ComfyUI/models/diffusion_models

Note: "Text to World" means Text to video and "Video to World" means image/video to video.

If you want the original diffusion models in .pt format instead of the repacked safetensors the official links are: [7B-Text2World](https://huggingface.co/nvidia/Cosmos-1.0-Diffusion-7B-Text2World) [7B-Video2World](https://huggingface.co/nvidia/Cosmos-1.0-Diffusion-7B-Video2World) [14B-Text2World](https://huggingface.co/nvidia/Cosmos-1.0-Diffusion-14B-Text2World) [14B-Video2World](https://huggingface.co/nvidia/Cosmos-1.0-Diffusion-14B-Video2World)

## Workflows

### Text to Video

This workflow requires the 7B text to video model that you can download above.

![Example](text_to_video_cosmos_7B.webp)

[Workflow in Json format](text_to_video_cosmos_7B.json)

### Image to Video

This model supports generating a video from 1 or more images. If more than one image is fed it will use them all as a guide and continue the motion. You can also do basic interpolation by setting one or more start_image and end_image which works best if those images are similar to each other.

This workflow requires the 7B image to video model that you can download above.

This model is trained primarily on realistic videos but in this example you can see that it also works decently on anime.

![Example](image_to_video_cosmos_7B.webp)

[Workflow in Json format](image_to_video_cosmos_7B.json)
