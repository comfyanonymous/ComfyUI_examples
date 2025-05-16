# 🌌 Nvidia Cosmos Models for ComfyUI

[Nvidia Cosmos](https://www.nvidia.com/en-us/ai/cosmos/) is a powerful family of **"World Models"** for text-to-video and image-to-video generation.  
ComfyUI currently supports the **7B** and **14B** Cosmos models for both **Text2Video** and **Image2Video** diffusion workflows.

---

## 📦 Required Files & Setup

### 🧠 Text Encoder & VAE

Download the following files and place them in the specified directories:

| File | Destination Folder |
|------|---------------------|
| [`oldt5_xxl_fp8_e4m3fn_scaled.safetensors`](https://huggingface.co/comfyanonymous/cosmos_1.0_text_encoder_and_VAE_ComfyUI/tree/main/text_encoders) | `ComfyUI/models/text_encoders/` |
| [`cosmos_cv8x8x8_1.0.safetensors`](https://huggingface.co/comfyanonymous/cosmos_1.0_text_encoder_and_VAE_ComfyUI/blob/main/vae/cosmos_cv8x8x8_1.0.safetensors) | `ComfyUI/models/vae/` |

> ⚠️ `oldt5_xxl` is **not** the same as `t5xxl` used in models like Flux.  
> `oldt5_xxl` = T5XXL **1.0**, while Flux uses **1.1**.

---

### 🎥 Video Diffusion Models

All `.safetensors` models go into:  
`ComfyUI/models/diffusion_models/`

| Model | Download |
|-------|----------|
| Cosmos 7B - Text to Video | [Cosmos-1_0-Diffusion-7B-Text2World.safetensors](https://huggingface.co/mcmonkey/cosmos-1.0/blob/main/Cosmos-1_0-Diffusion-7B-Text2World.safetensors) |
| Cosmos 7B - Image/Video to Video | [Cosmos-1_0-Diffusion-7B-Video2World.safetensors](https://huggingface.co/mcmonkey/cosmos-1.0/blob/main/Cosmos-1_0-Diffusion-7B-Video2World.safetensors) |

> 💡 “Text to World” = **Text ➜ Video**  
> “Video to World” = **Image/Video ➜ Video**

#### 🔁 Optional: Original `.pt` Versions

- [7B - Text2World (.pt)](https://huggingface.co/nvidia/Cosmos-1.0-Diffusion-7B-Text2World)  
- [7B - Video2World (.pt)](https://huggingface.co/nvidia/Cosmos-1.0-Diffusion-7B-Video2World)  
- [14B - Text2World (.pt)](https://huggingface.co/nvidia/Cosmos-1.0-Diffusion-14B-Text2World)  
- [14B - Video2World (.pt)](https://huggingface.co/nvidia/Cosmos-1.0-Diffusion-14B-Video2World)

---

## 🧪 Example Workflows

### 📝 Text ➜ Video (7B)

Generate dynamic video scenes straight from your prompts.

![Text to Video Example](text_to_video_cosmos_7B.webp)  
📄 [Download JSON Workflow](text_to_video_cosmos_7B.json)

---

### 🖼️ Image(s) ➜ Video (7B)

- Feed in one or multiple images.
- Smoothly **interpolates motion** if `start_image` and `end_image` are similar.
- Trained on realistic video data, but also handles **anime** fairly well!

![Image to Video Example](image_to_video_cosmos_7B.webp)  
📄 [Download JSON Workflow](image_to_video_cosmos_7B.json)

---

✨ With the power of Cosmos + ComfyUI, you're not just prompting—you're animating entire **worlds**.
