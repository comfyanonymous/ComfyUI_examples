# LCM Examples

LCM models are special models that are meant to be sampled in very few steps.

### LCM Lora

LCM loras are loras that can be used to convert a regular model to a LCM model.

The LCM SDXL lora can be downloaded from [here](https://huggingface.co/latent-consistency/lcm-lora-sdxl/blob/main/pytorch_lora_weights.safetensors)

Download it, rename it to: lcm_lora_sdxl.safetensors and put it in your ComfyUI/models/loras directory.

Then you can load this image in ComfyUI to get the workflow that shows how to use the LCM SDXL lora with the SDXL base model:

![Example](lcm_basic_example.png)

The important parts are to use a low cfg, use the "lcm" sampler and the "sgm_uniform" or "simple" scheduler. The ModelSamplingDiscrete node with lcm set as the sampling option will slightly improve results so it's also recommended but not always necessary.

The other LCM loras can be used the exact same way on their respective models.
