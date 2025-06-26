# Omnigen 2

[Omnigen 2](https://github.com/VectorSpaceLab/OmniGen2) is a model that can be used to edit images with text prompts.

## Files to Download

You will first need:

[omnigen2_fp16.safetensors](https://huggingface.co/Comfy-Org/Omnigen2_ComfyUI_repackaged/blob/main/split_files/diffusion_models/omnigen2_fp16.safetensors) goes in: ComfyUI/models/diffusion_models/

[qwen_2.5_vl_fp16.safetensors](https://huggingface.co/Comfy-Org/Omnigen2_ComfyUI_repackaged/blob/main/split_files/text_encoders/qwen_2.5_vl_fp16.safetensors) goes in: ComfyUI/models/text_encoders/

[ae.safetensors](https://huggingface.co/Comfy-Org/Omnigen2_ComfyUI_repackaged/blob/main/split_files/vae/ae.safetensors), this is the flux VAE that you might already have, it goes in: ComfyUI/models/vae/

## Workflows

This is a basic workflow using an image as a character reference. For multiple image inputs chain ReferenceLatent nodes together

![Example](omnigen2_example.png)

You can load this image in [ComfyUI](https://github.com/comfyanonymous/ComfyUI) to get the full workflow.

You can find the input image [here](../chroma/fennec_girl_sing.png)

