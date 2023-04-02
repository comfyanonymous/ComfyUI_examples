# Frequently Asked Questions

### Why do I get different images from the a1111 UI even when I use the same seed?

In ComfyUI the noise is generated on the CPU. Generating noise on the CPU gives ComfyUI the advantage that seeds will be much more reproducible across different hardware configurations but also means they will generate completely different noise than UIs like a1111 that generate the noise on the GPU. Generating noise on the GPU vs CPU does not affect performance in any way.

In ComfyUI the prompt strengths are also more sensitive because they are not normalized. A very short example is that when doing

```(masterpiece:1.2) (best:1.3) (quality:1.4) girl```

The a1111 ui is actually doing something like (but across all the tokens): 

```(masterpiece:0.98) (best:1.06) (quality:1.14) (girl:0.81)```

In ComfyUI the strengths are not averaged out like this so it will use the strengths exactly as you prompt them.

There are also many other differences but these two are the ones that have most impact.


