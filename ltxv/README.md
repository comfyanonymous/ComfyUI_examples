# Lightricks LTX-Video Model

[LTX-Video](https://huggingface.co/Lightricks/LTX-Video) is a very efficient video model by lightricks.

The important thing with this model is to give it long descriptive prompts.

Download the [ltx-video-2b-v0.9.5.safetensors](https://huggingface.co/Lightricks/LTX-Video/blob/main/ltx-video-2b-v0.9.5.safetensors) file and put it in your ComfyUI/models/checkpoints folder.

If you don't have it already downloaded you can download the [t5xxl_fp16.safetensors](https://huggingface.co/Comfy-Org/mochi_preview_repackaged/blob/main/split_files/text_encoders/t5xxl_fp16.safetensors) file and put it in your ComfyUI/models/text_encoders/ folder.

### Image to Video

Input image:
<img src="fox.jpg" width="256" />

#### Simple img2vid workflow with start image only:

![Example](ltxv_image_to_video_simple.0.9.5.webp)

[Workflow in Json format](ltxv_image_to_video_simple.0.9.5.json)


#### More complex img2vid workflow with multiple guiding images:

![Example](ltxv_image_to_video.0.9.5.webp)

[Workflow in Json format](ltxv_image_to_video.0.9.5.json)

You can download this webp animated image and load it or drag it on [ComfyUI](https://github.com/comfyanonymous/ComfyUI) to get the workflow.

### Text to Video

![Example](ltxv_text_to_video_0.9.5.webp)

[Workflow in Json format](ltxv_text_to_video_0.9.5.json)

You can download this webp animated image and load it or drag it on [ComfyUI](https://github.com/comfyanonymous/ComfyUI) to get the workflow.


[Old ltxv examples](README_old.md)


