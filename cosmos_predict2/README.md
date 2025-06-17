# Nvidia Cosmos Predict2

These are a family of text to image and image to video models from Nvidia.

## Files to Download

You will first need:

#### Text encoder and VAE:

[oldt5_xxl_fp8_e4m3fn_scaled.safetensors](https://huggingface.co/comfyanonymous/cosmos_1.0_text_encoder_and_VAE_ComfyUI/tree/main/text_encoders) goes in: ComfyUI/models/text_encoders/

[wan_2.1_vae.safetensors](https://huggingface.co/Comfy-Org/Wan_2.1_ComfyUI_repackaged/blob/main/split_files/vae/wan_2.1_vae.safetensors) goes in: ComfyUI/models/vae/


Note: oldt5_xxl is not the same as the t5xxl used in flux and other models. 
oldt5_xxl is t5xxl 1.0 while the one used in flux and others is t5xxl 1.1


You can find all the diffusion models (go in ComfyUI/models/diffusion_models/) here: [Repackaged safetensors files](https://huggingface.co/Comfy-Org/Cosmos_Predict2_repackaged/tree/main) or [Official Nvidia Model Files](https://huggingface.co/collections/nvidia/cosmos-predict2-68028efc052239369a0f2959)


## Workflows

### Text to Image

This workflow uses the 2B text to image cosmos predict2 model. The file used in the workflow is [cosmos_predict2_2B_t2i.safetensors](https://huggingface.co/Comfy-Org/Cosmos_Predict2_repackaged/blob/main/cosmos_predict2_2B_t2i.safetensors) this file goes in: ComfyUI/models/diffusion_models/

![Example](cosmos_predict2_2b_t2i_example.png)

You can load this image in [ComfyUI](https://github.com/comfyanonymous/ComfyUI) to get the full workflow.

I think the 2B model is the most interesting one but you can find the bigger 14B model here: [cosmos_predict2_14B_t2i.safetensors](https://huggingface.co/Comfy-Org/Cosmos_Predict2_repackaged/blob/main/cosmos_predict2_14B_t2i.safetensors) and use it in the workflow above.


### Image to Video

These models are pretty picky about the resolution/length of the videos. This workflow is for the 480p models, for the 720p models you will have to set the resolution to 720p or your results might be bad.

This workflow uses the 2B image to video cosmos predict2 model. The file used in the workflow is [cosmos_predict2_2B_video2world_480p_16fps.safetensors](https://huggingface.co/Comfy-Org/Cosmos_Predict2_repackaged/blob/main/cosmos_predict2_2B_video2world_480p_16fps.safetensors) this file goes in: ComfyUI/models/diffusion_models/

![Example](cosmos_predict2_2b_i2v_example.webp)

[Workflow in Json format](cosmos_predict2_2b_i2v_example.json)


