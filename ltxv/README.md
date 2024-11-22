# Lightricks LTX-Video Model

[LTX-Video](https://huggingface.co/Lightricks/LTX-Video) is a very efficient video model by lightricks.

The important thing with this model is to give it long descriptive prompts.

Download the [ltx-video-2b-v0.9.safetensors](https://huggingface.co/Lightricks/LTX-Video/blob/main/ltx-video-2b-v0.9.safetensors) file and put it in your ComfyUI/models/checkpoints folder.

If you don't have it already downloaded you can download the [t5xxl_fp16.safetensors](https://huggingface.co/Comfy-Org/mochi_preview_repackaged/blob/main/split_files/text_encoders/t5xxl_fp16.safetensors) file and put it in your ComfyUI/models/text_encoders/ folder.

### Text to Video

![Example](ltxv_text_to_video.webp)

[Workflow in Json format](ltxv_text_to_video.json)

You can download this webp animated image and load it or drag it on [ComfyUI](https://github.com/comfyanonymous/ComfyUI) to get the workflow.

### Image to Video

[Input image](https://commons.wikimedia.org/wiki/File:Havelock_Island,_Mangrove_tree_on_the_beach,_Andaman_Islands.jpg):
<img src="island.jpg" width="256" />

Workflow:

![Example](ltxv_image_to_video.webp)

[Workflow in Json format](ltxv_image_to_video.json)

You can download this webp animated image and load it or drag it on [ComfyUI](https://github.com/comfyanonymous/ComfyUI) to get the workflow.

