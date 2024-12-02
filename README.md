# ComfyUI-MVAdapter

This extension integrates [MV-Adapter](https://github.com/huanngzh/MV-Adapter) into ComfyUI, allowing users to generate multi-view consistent images from text prompts or single images directly within the ComfyUI interface.

## Features

* Generate multi-view consistent images from text prompts
* Generate multi-view consistent images from a single image
* More features are coming...

## Installation

### From Source

* Clone or download this repository into your `ComfyUI/custom_nodes/` directory.
* Install the required dependencies by running `pip install -r requirements.txt`.

## Usage

We provide the example workflows in `workflows` directory.

Note that our code depends on diffusers, and will automatically download the model weights from huggingface to the hf cache path at the first time. The `ckpt_name` in the node corresponds to the model name in huggingface, such as `stabilityai/stable-diffusion-xl-base-1.0`.

We also provide the nodes `Ldm**Loader` to support loading text-to-image models in `ldm` format. Please see the workflow files with the suffix `_ldm.json`.

### Text to Multi-view Images

![comfyui_t2mv](assets/comfyui_t2mv.png)

* `workflows/t2mv_sdxl_diffusers.json` for loading diffusers-format models
* `workflows/t2mv_sdxl_ldm.json` for loading ldm-format models

### Image to Multi-view Images

![comfyui_i2mv](assets/comfyui_i2mv.png)

* `workflows/i2mv_sdxl_diffusers.json` for loading diffusers-format models
* `workflows/i2mv_sdxl_ldm.json` for loading ldm-format models