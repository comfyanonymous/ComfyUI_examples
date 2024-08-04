# Flux Examples

Flux is a family of diffusion models by [black forest labs](https://blackforestlabs.ai/announcing-black-forest-labs/)

For the easy to use single file version see below: [FP8 Checkpoint Version](#simple-to-use-fp8-checkpoint-version)

### Files to download for the regular version

If you don't have t5xxl_fp16.safetensors or clip_l.safetensors already in your ComfyUI/models/clip/ directory you can find them on: [this link.](https://huggingface.co/comfyanonymous/flux_text_encoders/tree/main) You can use t5xxl_fp8_e4m3fn.safetensors instead for lower memory usage but the fp16 one is recommended if you have more than 32GB ram.

The VAE can be found [here](https://huggingface.co/black-forest-labs/FLUX.1-schnell/blob/main/ae.sft) and should go in your ComfyUI/models/vae/ folder.

### Tips if you are running out of memory:

Use the single file version that you can find by looking [Below](#simple-to-use-fp8-checkpoint-version)

You can set the weight_dtype in the "Load Diffusion Model" node to fp8 which will lower the memory usage by half but might reduce quality a tiny bit. You can also download the example.

## Flux Dev

You can find the Flux Dev diffusion model weights [here](https://huggingface.co/black-forest-labs/FLUX.1-dev). Put the flux1-dev.sft file in your: ComfyUI/models/unet/ folder.

You can then load or drag the following image in ComfyUI to get the workflow:

![Example](flux_dev_example.png)

### Simple to use FP8 Checkpoint version

You can find an easy to use checkpoint for the Flux dev [here](https://huggingface.co/Comfy-Org/flux1-dev/blob/main/flux1-dev-fp8.safetensors) that you can put in your: ComfyUI/models/checkpoints/ directory.

Note that fp8 degrades the quality a bit so if you have the resources the full version above is recommended.

You can then load or drag the following image in ComfyUI to get the workflow:

![Example](flux_dev_checkpoint_example.png)


## Flux Schnell

Flux Schnell is a distilled 4 step model.

You can find the Flux Schnell diffusion model weights [here](https://huggingface.co/black-forest-labs/FLUX.1-schnell/blob/main/flux1-schnell.sft) this file should go in your: ComfyUI/models/unet/ folder.


You can then load or drag the following image in ComfyUI to get the workflow:

![Example](flux_schnell_example.png)