# ControlNet Examples

### Scribble ControlNet

Here's a simple example of how to use controlnets, this example uses the scribble controlnet and the AnythingV3 model. You can load this image in [ComfyUI](https://github.com/comfyanonymous/ComfyUI) to get the full workflow.


![Example](controlnet_example.png)

Here is the input image I used for this workflow:

<img src="input_scribble_example.png" width="256" />

### Pose ControlNet

This is the input image that will be used in this example:

![Example](pose_worship.png)


Here is an example using a first pass with AnythingV3 with the controlnet and a second pass without the controlnet with AOM3A3 (abyss orange mix 3) and using their VAE.

![Example](2_pass_pose_worship.png)

You can load this image in [ComfyUI](https://github.com/comfyanonymous/ComfyUI) to get the full workflow.

### Mixing ControlNets

Multiple ControlNets can be applied like this with interesting results:

![Example](mixing_controlnets.png)

You can load this image in [ComfyUI](https://github.com/comfyanonymous/ComfyUI) to get the full workflow.

Input images:

<img src="pose_present.png" width="256" />   <img src="house_scribble.png" width="256" />

