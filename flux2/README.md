# Flux 2

[Flux 2](https://github.com/black-forest-labs/flux2) is a state of the art image diffusion model.

## Files to Download

Text encoder file: [mistral_3_small_flux2_fp8.safetensors](https://huggingface.co/Comfy-Org/flux2-dev/blob/main/split_files/text_encoders/mistral_3_small_flux2_fp8.safetensors) (goes in ComfyUI/models/text_encoders/).


Fp8 diffusion model file: [flux2_dev_fp8mixed.safetensors](https://huggingface.co/Comfy-Org/flux2-dev/blob/main/split_files/diffusion_models/flux2_dev_fp8mixed.safetensors) (goes in ComfyUI/models/diffusion_models/). If you want the full sized diffusion model you can find the flux2-dev.safetensors on the official repo [here](https://huggingface.co/black-forest-labs/FLUX.2-dev)

VAE: [flux2-vae.safetensors](https://huggingface.co/Comfy-Org/flux2-dev/blob/main/split_files/vae/flux2-vae.safetensors) (goes in ComfyUI/models/vae/)

## Basic Example Workflow

You can then load up or drag the following image in ComfyUI to get the workflow:

![Example](flux2_example.png)

This model supports multiple reference images as optional inputs. This example workflow has two of them bypassed out but you can add more.
