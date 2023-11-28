# Video Examples

## Image to Video

As of writing this there are two image to video checkpoints. Here are the official checkpoints for [the one tuned to generate 14 frame videos](https://huggingface.co/stabilityai/stable-video-diffusion-img2vid/blob/main/svd.safetensors) and [the one for 25 frame videos](https://huggingface.co/stabilityai/stable-video-diffusion-img2vid-xt/blob/main/svd_xt.safetensors). Put them in the ComfyUI/models/checkpoints folder.


The most basic way of using the image to video model is by giving it an init image like in the following workflow that uses the 14 frame model.
You can download this webp animated image and load it or drag it on [ComfyUI](https://github.com/comfyanonymous/ComfyUI) to get the workflow.

![Example](image_to_video.webp)
[Workflow in Json format](workflow_image_to_video.json)

If you want the exact input image you can find it on the [unCLIP example page](../unclip)

You can also use them like in this workflow that uses SDXL to generate an initial image that is then passed to the 25 frame model:

![Example](txt_to_image_to_video.webp)
[Workflow in Json format](workflow_txt_to_img_to_video.json)

#### Some explanations for the parameters:

video_frames: The number of video frames to generate.

motion_bucket_id: The higher the number the more motion will be in the video.

fps: The higher the fps the less choppy the video will be.

augmentation level: The amount of noise added to the init image, the higher it is the less the video will look like the init image. Increase it for more motion.

VideoLinearCFGGuidance: This node improves sampling for these video models a bit, what it does is linearly scale the cfg across the different frames. In the above example the first frame will be cfg 1.0 (the min_cfg in the node) the middle frame 1.75 and the last frame 2.5. (the cfg set in the sampler). This way frames further away from the init frame get a gradually higher cfg.
