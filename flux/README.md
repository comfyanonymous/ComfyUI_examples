# Flux Examples

Flux is a family of diffusion models by [black forest labs](https://blackforestlabs.ai/announcing-black-forest-labs/)

For the easy to use single file versions that you can easily use in [ComfyUI](https://github.com/comfyanonymous/ComfyUI) see below: [FP8 Checkpoint Version](#simple-to-use-fp8-checkpoint-version)

## Regular Full Version

### Files to download for the regular version

If you don't have t5xxl_fp16.safetensors or clip_l.safetensors already in your ComfyUI/models/clip/ directory you can find them on: [this link.](https://huggingface.co/comfyanonymous/flux_text_encoders/tree/main) You can use t5xxl_fp8_e4m3fn.safetensors instead for lower memory usage but the fp16 one is recommended if you have more than 32GB ram.

The VAE can be found [here](https://huggingface.co/black-forest-labs/FLUX.1-schnell/blob/main/ae.safetensors) and should go in your ComfyUI/models/vae/ folder.

### Tips if you are running out of memory:

Use the single file fp8 version that you can find by looking [Below](#simple-to-use-fp8-checkpoint-version)

You can set the weight_dtype in the "Load Diffusion Model" node to fp8 which will lower the memory usage by half but might reduce quality a tiny bit. You can also download the example.

### Flux Dev

You can find the Flux Dev diffusion model weights [here](https://huggingface.co/black-forest-labs/FLUX.1-dev). Put the flux1-dev.safetensors file in your: ComfyUI/models/unet/ folder.

You can then load or drag the following image in ComfyUI to get the workflow:

![Example](flux_dev_example.png)

### Flux Schnell

Flux Schnell is a distilled 4 step model.

You can find the Flux Schnell diffusion model weights [here](https://huggingface.co/black-forest-labs/FLUX.1-schnell/blob/main/flux1-schnell.safetensors) this file should go in your: ComfyUI/models/unet/ folder.


You can then load or drag the following image in ComfyUI to get the workflow:

![Example](flux_schnell_example.png)


## Simple to use FP8 Checkpoint version

### Flux Dev

You can find an easy to use checkpoint for the Flux dev [here](https://huggingface.co/Comfy-Org/flux1-dev/blob/main/flux1-dev-fp8.safetensors) that you can put in your: ComfyUI/models/checkpoints/ directory.

This file can be loaded with the regular "Load Checkpoint" node. Make sure you set CFG to 1.0 when using it.

Note that fp8 degrades the quality a bit so if you have the resources the official full 16 bit version is recommended.

You can then load or drag the following image in ComfyUI to get the workflow:

![Example](flux_dev_checkpoint_example.png)

### Flux Schnell

For Flux schnell you can get the checkpoint [here](https://huggingface.co/Comfy-Org/flux1-schnell/blob/main/flux1-schnell-fp8.safetensors) that you can put in your: ComfyUI/models/checkpoints/ directory.

You can then load or drag the following image in ComfyUI to get the workflow:

![Example](flux_schnell_checkpoint_example.png)
