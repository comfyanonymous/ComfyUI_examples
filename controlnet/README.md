# ControlNet and T2I-Adapter Examples

Note that in these examples the raw image is passed to the ControlNet/T2I adapter without any preprocessing. When passing images directly to the controlnet it should be the type of image that the ControlNet expects to get the best results.

If you are looking for nodes to preprocess your images you can find some: [Here](https://github.com/Fannovel16/comfy_controlnet_preprocessors)


### Scribble ControlNet

Here's a simple example of how to use controlnets, this example uses the scribble controlnet and the AnythingV3 model. You can load this image in [ComfyUI](https://github.com/comfyanonymous/ComfyUI) to get the full workflow.


![Example](controlnet_example.png)

Here is the input image I used for this workflow:

<img src="input_scribble_example.png" width="256" />

### T2I-Adapter vs ControlNets

T2I-Adapters are much much more efficient than ControlNets so I highly recommend them. ControlNets will slow down generation speed by a significant amount while T2I-Adapters have almost zero negative impact on generation speed.

In ControlNets the ControlNet model is run once every iteration. For the T2I-Adapter the model runs once in total.

T2I-Adapters are used the same way as ControlNets in ComfyUI, the only thing that changes is that there is a T2IAdapterLoader node to load them.

This is the input image that will be used in this example [source](https://commons.wikimedia.org/wiki/File:Stereogram_Tut_Shark_Depthmap.png):

<img src="shark_depthmap.png" width="512" />

Here is how you use the depth T2I-Adapter:

![Example](depth_t2i_adapter.png)

Here is how you use the depth Controlnet. Note that this example uses the DiffControlNetLoader node because the controlnet used is a diff control net. Diff controlnets need the weights of a model to be loaded correctly. The DiffControlNetLoader node can also be used to load regular controlnet models. When loading regular controlnet models it will behave the same as the ControlNetLoader node.

![Example](depth_controlnet.png)

You can load these images in [ComfyUI](https://github.com/comfyanonymous/ComfyUI) to get the full workflow.

### Pose ControlNet

This is the input image that will be used in this example:

![Example](pose_worship.png)


Here is an example using a first pass with AnythingV3 with the controlnet and a second pass without the controlnet with AOM3A3 (abyss orange mix 3) and using their VAE.

![Example](2_pass_pose_worship.png)

You can load this image in [ComfyUI](https://github.com/comfyanonymous/ComfyUI) to get the full workflow.


### Mixing ControlNets

Multiple ControlNets and T2I-Adapters can be applied like this with interesting results:

![Example](mixing_controlnets.png)

You can load this image in [ComfyUI](https://github.com/comfyanonymous/ComfyUI) to get the full workflow.

Input images:

<img src="pose_present.png" width="256" /><span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><img src="house_scribble.png" width="256" />

