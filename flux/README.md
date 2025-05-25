# Flux Examples

Flux is a family of diffusion models by [black forest labs](https://blackforestlabs.ai/announcing-black-forest-labs/)

For the easy to use single file versions that you can easily use in [ComfyUI](https://github.com/comfyanonymous/ComfyUI) see below: [FP8 Checkpoint Version](#simple-to-use-fp8-checkpoint-version)

## Regular Full Version

### Files to download for the regular version

If you don't have t5xxl_fp16.safetensors or clip_l.safetensors already in your ComfyUI/models/text_encoders/ directory you can find them on: [this link.](https://huggingface.co/comfyanonymous/flux_text_encoders/tree/main) You can use t5xxl_fp8_e4m3fn.safetensors instead for lower memory usage but the fp16 one is recommended if you have more than 32GB ram.

The VAE can be found [here](https://huggingface.co/Comfy-Org/Lumina_Image_2.0_Repackaged/blob/main/split_files/vae/ae.safetensors) and should go in your ComfyUI/models/vae/ folder.

### Tips if you are running out of memory:

Use the single file fp8 version that you can find by looking [Below](#simple-to-use-fp8-checkpoint-version)

You can set the weight_dtype in the "Load Diffusion Model" node to fp8 which will lower the memory usage by half but might reduce quality a tiny bit. You can also download the example.

### Flux Dev

You can find the Flux Dev diffusion model weights [here](https://huggingface.co/black-forest-labs/FLUX.1-dev). Put the flux1-dev.safetensors file in your: ComfyUI/models/diffusion_models/ folder.

You can then load or drag the following image in ComfyUI to get the workflow:

![Example](flux_dev_example.png)

### Flux Schnell

Flux Schnell is a distilled 4 step model.

You can find the Flux Schnell diffusion model weights [here](https://huggingface.co/black-forest-labs/FLUX.1-schnell) the flux1-schnell.safetensors file should go in your: ComfyUI/models/unet/ folder.


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

## Flux Extras

The following examples might require that you have some of the regular flux files that you can find links to at the top of this page.

### Fill (Inpainting) model

Download the [flux1-fill-dev.safetensors](https://huggingface.co/black-forest-labs/FLUX.1-Fill-dev) model file and put it in your ComfyUI/models/diffusion_models/ folder.

Here is an example you can drag in ComfyUI for inpainting, a reminder that you can right click images in the "Load Image" node and "Open in MaskEditor".

![Example](flux_fill_inpaint_example.png)

Here is an example for outpainting:

![Example](flux_fill_outpaint_example.png)


### Redux

The Redux model is a model that can be used to prompt flux dev or flux schnell with one or more images.

Download the [sigclip_vision_patch14_384.safetensors](https://huggingface.co/Comfy-Org/sigclip_vision_384/blob/main/sigclip_vision_patch14_384.safetensors) model and put it in your ComfyUI/models/clip_vision folder and download the [flux1-redux-dev.safetensors](https://huggingface.co/black-forest-labs/FLUX.1-Redux-dev) and put it in your ComfyUI/models/style_models folder.

You can then load or drag the following image in ComfyUI to get the workflow:

![Example](flux_redux_model_example.png)

### Canny and Depth

They are published in two versions, full model format: [flux1-canny-dev.safetensors](https://huggingface.co/black-forest-labs/FLUX.1-Canny-dev) and [flux1-depth-dev.safetensors](https://huggingface.co/black-forest-labs/FLUX.1-Depth-dev), put them in your ComfyUI/models/diffusion_models/ folder

Here is an example for the full canny model:

![Example](flux_canny_model_example.png)

They are also published in lora format that can be applied to the flux dev model: [flux1-canny-dev-lora.safetensors](https://huggingface.co/black-forest-labs/FLUX.1-Canny-dev-lora) and [flux1-depth-dev-lora.safetensors](https://huggingface.co/black-forest-labs/FLUX.1-Depth-dev-lora), put them in your ComfyUI/models/loras/ folder

Here is an example for the depth lora.

![Example](flux_depth_lora_example.png)


### Community Flux Controlnets

XLab and InstantX + Shakker Labs have released Controlnets for Flux. You can find the InstantX Canny model file [here](https://huggingface.co/InstantX/FLUX.1-dev-Controlnet-Canny/blob/main/diffusion_pytorch_model.safetensors) (rename to instantx_flux_canny.safetensors for the example below), the Depth controlnet [here](https://huggingface.co/Shakker-Labs/FLUX.1-dev-ControlNet-Depth/blob/main/diffusion_pytorch_model.safetensors) and the Union Controlnet [here](https://huggingface.co/Shakker-Labs/FLUX.1-dev-ControlNet-Union-Pro/blob/main/diffusion_pytorch_model.safetensors). 

The XLab controlnets can be found here [here](https://huggingface.co/XLabs-AI/flux-controlnet-collections).

Put these files under `ComfyUI/models/controlnet` directory.

Try an example Canny Controlnet workflow by dragging in this image into ComfyUI.

![Example](flux_controlnet_example.png)

If you need an example input image for the canny, use [this](girl_in_field.png). Put it under `ComfyUI/input`.
