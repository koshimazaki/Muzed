# MUZED

**Unfair Studio x Koshi Mazaki**

AI dance film exploring motion transfer, generative video, and fabric simulation through custom-trained models and multi-tool pipelines.

Digital garments, inherited gestures, synthetic sound. Through all three elements the dancer embodies vibration as ritual aesthetics.

[The pipeline](https://muzed.pages.dev/) | [Motion LoRA on HuggingFace](https://huggingface.co/KoshiMazaki/muzed-motion-lora)

---

## Process

Real choreography by Amanda, sliced into 5s, 14s and 11s clips, captioned with movement vocabulary, and used to train a custom Motion LoRA on LTX-2. The trained model captures her specific movement quality, gestures, weight shifts, and camera dynamics, things the base model doesn't know.

The Motion LoRA was used for exploration and motion transfer with LTX-2, allowing generated footage to carry Amanda's choreographic signature into new visual worlds.

Main footage was produced using Kling 3.0 Motion for its temporal coherence and character consistency across longer sequences.

Fabric sequences were generated with LTX-2.3, which handles flowing material and texture particularly well.

Transitions and particle effects were built using ComfyCloud workflows on LTX-2.3, giving precise control over timing and visual transitions.

All still images were generated with Flux.2 Pro. Midjourney was used for early visual exploration and mood boarding.

---

## Tools

| Tool | Role |
|------|------|
| **LTX-2 and LTX-2.3** | Motion LoRA training, motion transfer, fabric sequences, transitions, particle effects |
| **Kling 3.0 Motion** | Main footage, long-form dance sequences |
| **Flux.2 Pro** | Still image generation |
| **Midjourney** | Visual exploration, mood boards |
| **ComfyCloud** | Workflow orchestration for transitions and effects |
| **LTX Trainer** | Custom Motion LoRA training (125 clips, 1x H200, rank 64) |

---

## Motion LoRA

Custom model trained on Amanda's choreography to capture her movement language.

- **Model:** [KoshiMazaki/muzed-motion-lora](https://huggingface.co/KoshiMazaki/muzed-motion-lora)
- **Base:** LTX-2 19B
- **Dataset:** 125 clips at 1536x864, 161 frames (5.4s each), 30fps
- **Source:** 3 real dancer videos (2 upper-body, 1 full-body)
- **Training:** 1x H200, rank 64, 2000 steps
- **Trigger token:** `DNCMOV`

Used for exploration and LTX-2 motion transfer throughout the project.

---

## Credits

| | |
|---|---|
| **Dance** | Amanda |
| **Production** | [Unfair Studio](https://www.unfairstudio.ai/en) x [Koshi Mazaki](https://github.com/koshimazaki) |
