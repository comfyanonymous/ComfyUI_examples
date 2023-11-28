# SDXL Turbo Examples

SDXL Turbo is a SDXL model that can generate consistent images in a single step. You can use more steps to increase the quality. The proper way to use it is with the new SDTurboScheduler node but it might also work with the regular schedulers.

Here is the link to [download the official SDXL turbo checkpoint](https://huggingface.co/stabilityai/sdxl-turbo/blob/main/sd_xl_turbo_1.0_fp16.safetensors)

Here is a workflow for using it:

![Example](sdxlturbo_example.png)

Save this image then load it or drag it on ComfyUI to get the workflow. I then recommend enabling Extra Options -> Auto Queue in the interface. Then press "Queue Prompt" once and start writing your prompt.
