# Flux Examples

Flux is a family of diffusion models by [black forest labs](https://blackforestlabs.ai/announcing-black-forest-labs/)

If you don't have t5xxl_fp16.safetensors or clip_l.safetensors already in your ComfyUI/models/clip/ directory you can find them on: [this link.](https://huggingface.co/comfyanonymous/flux_text_encoders/tree/main) You can use t5xxl_fp8_e4m3fn.safetensors instead for lower memory usage but the fp16 one is recommended if you have more than 32GB ram.

The VAE can be found [here](https://huggingface.co/black-forest-labs/FLUX.1-schnell/blob/main/ae.sft) and should go in your ComfyUI/models/vae/ folder.

#### Tips if you are running out of memory:

You can set the weight_dtype in the "Load Diffusion Model" node to fp8 which will lower the memory usage by half but might reduce quality a tiny bit.

## Flux Dev

You can find the Flux Dev diffusion model weights [here](https://huggingface.co/black-forest-labs/FLUX.1-dev). Put the flux1-dev.sft file in your: ComfyUI/models/unet/ folder.

You can then load or drag the following image in ComfyUI to get the workflow:

![Example](flux_dev_example.png)

## Flux Schnell

Flux Schnell is a distilled 4 step model.

You can find the Flux Schnell diffusion model weights [here](https://huggingface.co/black-forest-labs/FLUX.1-schnell/blob/main/flux1-schnell.sft) this file should go in your: ComfyUI/models/unet/ folder.


You can then load or drag the following image in ComfyUI to get the workflow:

![Example](flux_schnell_example.png)