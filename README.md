# ComfyUI FashionNova Workflow

This repository contains the **Fooocus_FashionNova_RunDiffusion_UI.json** workflow designed for the [ComfyUI](https://github.com/comfyanonymous/ComfyUI) image generation tool. The workflow loads several models and expects two reference images to guide the generation process.

## Installing ComfyUI

1. Clone the ComfyUI repository and install its requirements:

   ```bash
   git clone https://github.com/comfyanonymous/ComfyUI.git
   cd ComfyUI
   pip install -r requirements.txt
   ```

2. Launch ComfyUI:

   ```bash
   python main.py
   ```

## Importing the Workflow

With ComfyUI running, use the **Load** button in the top left of the interface and select `Fooocus_FashionNova_RunDiffusion_UI.json` from this repository. The nodes will be created automatically.

## Required Model Files

Place the following files in the specified directories inside your `ComfyUI/models` folder:

| File | Destination |
| ---- | ----------- |
| `lustifyXL.safetensors` | `models/checkpoints/` |
| `Demiv3.safetensors` | `models/loras/` |
| `stylebooster.safetensors` | `models/loras/` |
| `ipadapter_full_sdxl.bin` | `models/ipadapter/` |
| `4x-ultrasharp.pth` | `models/upscale_models/` |

## Input Images

The workflow expects two reference images named `body_shape_ref.png` and `outfit_ref.png`. Place them in an `input` directory inside your ComfyUI folder:

```
ComfyUI/
├── input/
│   ├── body_shape_ref.png
│   └── outfit_ref.png
```

## Recommended Folder Structure

An example directory layout after copying the workflow and models might look like:

```
ComfyUI/
├── Fooocus_FashionNova_RunDiffusion_UI.json
├── input/
│   ├── body_shape_ref.png
│   └── outfit_ref.png
└── models/
    ├── checkpoints/
    │   └── lustifyXL.safetensors
    ├── loras/
    │   ├── Demiv3.safetensors
    │   └── stylebooster.safetensors
    ├── ipadapter/
    │   └── ipadapter_full_sdxl.bin
    └── upscale_models/
        └── 4x-ultrasharp.pth
```

After the files are in place, launch ComfyUI and load the workflow JSON as described above. You can then run the workflow and experiment with the prompts to generate fashion designs.

