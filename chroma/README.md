# Chroma

This is a model that is modified from [flux](../flux/) and has had some changes in the architecture.

To use it you will need one of the t5xxl text encoder model files that you can find in: [this repo](https://huggingface.co/comfyanonymous/flux_text_encoders/tree/main), fp16 is recommended, if you don't have that much memory fp8_scaled are recommended. Put it in the ComfyUI/models/text_encoders/ folder.

You can then download the latest chroma checkpoint from the [official huggingface page](https://huggingface.co/lodestones/Chroma1-HD), It goes in the ComfyUI/models/diffusion_models/ folder.

Load or drag this image on ComfyUI to get the example workflow:

![Example](chroma_example.png)
