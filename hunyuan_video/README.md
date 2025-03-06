# Hunyuan Video Model

[Hunyuan Video](https://huggingface.co/tencent/HunyuanVideo) is a text to video model.


Download the clip_l.safetensors and llava_llama3_fp8_scaled.safetensors files from [here](https://huggingface.co/Comfy-Org/HunyuanVideo_repackaged/tree/main/split_files/text_encoders) and put them in your ComfyUI/models/text_encoders directory.

Download the [hunyuan_video_vae_bf16.safetensors](https://huggingface.co/Comfy-Org/HunyuanVideo_repackaged/tree/main/split_files/vae) file and put it in your ComfyUI/models/vae folder.

### Text to Video

Download the [hunyuan_video_t2v_720p_bf16.safetensors](https://huggingface.co/Comfy-Org/HunyuanVideo_repackaged/tree/main/split_files/diffusion_models) file and put it in your ComfyUI/models/diffusion_models folder.

This model can also generate still images by setting the video length to 1.

![Example](hunyuan_video_text_to_video.webp)

[Workflow in Json format](hunyuan_video_text_to_video.json)

You can download this webp animated image and load it or drag it on [ComfyUI](https://github.com/comfyanonymous/ComfyUI) to get the workflow.

### Image to Video

Download the [hunyuan_video_image_to_video_720p_bf16.safetensors](https://huggingface.co/Comfy-Org/HunyuanVideo_repackaged/tree/main/split_files/diffusion_models) file and put it in your ComfyUI/models/diffusion_models/ folder.

Download the [llava_llama3_vision.safetensors](https://huggingface.co/Comfy-Org/HunyuanVideo_repackaged/blob/main/split_files/clip_vision/llava_llama3_vision.safetensors) file and put it in your ComfyUI/models/clip_vision/ folder.

![Example](hunyuan_video_image_to_video.webp)

[Workflow in Json format](hunyuan_video_image_to_video.json)

You can download this webp animated image and load it or drag it on [ComfyUI](https://github.com/comfyanonymous/ComfyUI) to get the workflow. The input image can be found on the [flux](../flux) page.
