# Hunyuan DiT Examples

Hunyuan DiT is a diffusion model that understands both english and chinese.

## Hunyuan DiT 1.2

### text2image
Download [hunyuan_dit_1.2.safetensors](https://huggingface.co/comfyanonymous/hunyuan_dit_comfyui/blob/main/hunyuan_dit_1.2.safetensors) and put it in your `ComfyUI/models/checkpoints` directory.

You can then load up the following image in ComfyUI to get the workflow:

![Example](hunyuan_dit_1.2_example.png)

### ControlNet
Download the [ControlNet model weight files here](https://huggingface.co/Tencent-Hunyuan/HYDiT-ControlNet-v1.2/tree/main) and put them in your `ComfyUI/models/controlnet/hunyuandit` directory.

You can then load up the following image in ComfyUI to get a canny ControlNet workflow:

![Example](hunyuan_dit_1.2_controlnet_canny_example.png)
