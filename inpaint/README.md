# Inpaint Examples

In this example we will be using this image. Download it and place it in your input folder.

![Example](yosemite_inpaint_example.png)

This image has had part of it erased to alpha with gimp, the alpha channel is what we will be using as a mask for the inpainting. If using GIMP make sure you save the values of the transparent pixels for best results.


The following images can be loaded in [ComfyUI](https://github.com/comfyanonymous/ComfyUI) to get the full workflow.

Inpainting a cat with the v2 inpainting model:

![Example](inpain_model_cat.png)

Inpainting a woman with the v2 inpainting model:

![Example](inpain_model_woman.png)

It also works with non inpainting models. Here's an example with the anythingV3 model:

![Example](inpaint_anythingv3_woman.png)

### Outpainting

You can also use these exact workflows for outpainting, first expand the canvas of the image in your favorite image editor filling it with transparency like in this input image where I expanded the top and bottom:

![Example](yosemite_outpaint_example.png)


Using the v2 inpainting model the exact same way as the inpainting examples:

![Example](inpain_model_outpainting.png)

