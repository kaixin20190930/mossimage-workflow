# MOSS-Image ComfyUI Workflow

Ready-to-use ComfyUI workflow for [MOSS-Image](https://arxiv.org/abs/2610.23374) — the 5B open-source diffusion model with JSON layout control and Chinese/English text rendering (Apache 2.0).

## Quick Start

1. Install [ComfyUI](https://github.com/comfyanonymous/ComfyUI)
2. Install the MOSS-Image custom node via ComfyUI Manager (search "MOSS-Image")
3. Download `moss-image-workflow.json` from this repo
4. Drag it into ComfyUI
5. Load MOSS-Image-SFT model, enter your prompt, hit Queue

## Model Versions

| | Base | SFT |
|---|---|---|
| License | Apache 2.0 | — |
| Best for | General generation | Text rendering, JSON layout |
| Deploy | Self-host | Self-host or [fal.ai API](https://fal.ai/models/fal-ai/moss-image) |
| Download | [HuggingFace](https://huggingface.co/OpenMOSS/MOSS-Image-Base) | — |

## JSON Layout — Why This Matters

MOSS-Image is the first open-source model that lets you control object placement with JSON. Instead of hoping the model understands "red ball on the left, blue cube on the right":

```json
{
  "canvas": {"width": 1024, "height": 1024},
  "objects": [
    {"label": "red ball", "position": [0.2, 0.5], "size": [0.3, 0.3]},
    {"label": "blue cube", "position": [0.8, 0.5], "size": [0.3, 0.3]}
  ],
  "style": "white background, studio lighting"
}
```

The model places each object exactly where specified. JSON layout is ~80% accurate vs ~40% with natural language alone.

## Workflow Includes

- Text-to-image with MOSS-Image-SFT
- JSON layout control node
- Prompt enhancer (auto-improves short prompts)
- Resolution presets: 512×512 / 768×768 / 1024×1024
- Batch generation support

## Try Online (No Setup)

👉 **[mossimage.run](https://mossimage.run)** — Free MOSS-Image Generator, 3 images/day, no sign-up

## More Resources

- [MOSS-Image paper (arXiv)](https://arxiv.org/abs/2610.23374)
- [MOSS-Image on HuggingFace](https://huggingface.co/OpenMOSS/MOSS-Image-Base)
- [OpenMOSS GitHub](https://github.com/OpenMOSS)
- [ComfyUI setup guide](https://mossimage.run/comfyui/)
- [API access via fal.ai](https://mossimage.run/api/)

## License

Workflow JSON — MIT. MOSS-Image model — Apache 2.0.
