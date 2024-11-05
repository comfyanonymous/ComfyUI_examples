# Mochi Video Model

[Mochi](https://huggingface.co/genmo/mochi-1-preview) is a state of the art video model.

You can find all the model files for the following workflow [here](https://huggingface.co/Comfy-Org/mochi_preview_repackaged/tree/main/split_files)

```
diffusion_models/mochi_preview_bf16.safetensors goes in: ComfyUI/models/diffusion_models/
text_encoders/t5xxl_fp16.safetensors goes in: ComfyUI/models/text_encoders/
vae/mochi_vae.safetensors goes in: ComfyUI/models/vae/
```

If you have memory issues you can pick the fp8 files instead of the bf16/fp16 ones.

![Example](mochi_text_to_video_example.webp)

You can download this webp animated image and load it or drag it on [ComfyUI](https://github.com/comfyanonymous/ComfyUI) to get the workflow.


There is also an all in one fp8 checkpoint [here](https://huggingface.co/Comfy-Org/mochi_preview_repackaged/blob/main/all_in_one/mochi_preview_fp8_scaled.safetensors) that contains the fp8 versions of the files in the above workflow packaged in a single checkpoint.

Note that using the fp8 files will give lower quality than using the 16 bit ones but might be faster especially if you have a GPU that supports fp8 ops.

Here is the workflow to use it:

![Example](mochi_simple_checkpoint.webp)

