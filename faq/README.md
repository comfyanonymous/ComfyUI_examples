# Frequently Asked Questions

## Why do I get different images from the a1111 UI even when I use the same seed?

In ComfyUI the noise is generated on the CPU. Generating noise on the CPU gives ComfyUI the advantage that seeds will be much more reproducible across different hardware configurations but also means they will generate completely different noise than UIs like a1111 that generate the noise on the GPU. Generating noise on the GPU vs CPU does not affect performance in any way.

In ComfyUI the prompt strengths are also more sensitive because they are not normalized. A very short example is that when doing

```(masterpiece:1.2) (best:1.3) (quality:1.4) girl```

The a1111 ui is actually doing something like (but across all the tokens): 

```(masterpiece:0.98) (best:1.06) (quality:1.14) (girl:0.81)```

In ComfyUI the strengths are not averaged out like this so it will use the strengths exactly as you prompt them.

There are also many other differences but these two are the ones that have most impact.


## Why do I get incoherent images with some checkpoints that are less than 1.9GB?

Some rare checkpoints like ProtoGen_X3.4 don't come with CLIP weights. The CLIPLoader node in ComfyUI can be used to load CLIP model weights like [these SD1.5 ones](https://huggingface.co/runwayml/stable-diffusion-v1-5/blob/main/text_encoder/model.safetensors).


## What is the difference between strength_model and strength_clip in the "Load LoRA" node?

These separate values control the strength that the LoRA is applied separately to the CLIP model and the main MODEL. In most UIs adjusting the LoRA strength is only one number and setting the lora strength to 0.8 for example is the same as setting both strength_model and strength_clip to 0.8.

The reason you can tune both in ComfyUI is because the CLIP and MODEL/UNET part of the LoRA will most likely have learned different concepts so tweaking them separately can give you better images.
