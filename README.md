Here’s a modified version of the **README** file with input/output image examples, as requested:

---

# Enhancing Control in Stable Diffusion Through Example-Based Fine-Tuning and Prompt Engineering

This project focuses on enhancing the control and output quality of the Stable Diffusion model through example-based fine-tuning and prompt engineering. The goal is to generate high-quality images by refining prompts, applying negative prompts to avoid undesirable outputs, and fine-tuning model parameters like guidance scale and inference steps.

## Table of Contents

- [Introduction](#introduction)
- [Installation](#installation)
- [Usage](#usage)
- [Parameters](#parameters)
- [Prompt Lists](#prompt-lists)
- [Example Code](#example-code)
- [Results](#results)
- [License](#license)

## Introduction

Stable Diffusion is a state-of-the-art text-to-image generation model. This project leverages prompt engineering and fine-tuning techniques to improve the model's control over the generated images. We use both positive and negative prompts to direct the model towards desired characteristics and away from undesirable ones.

### Key Features:
- Fine-tuning Stable Diffusion for more precise image generation.
- Prompt and negative prompt engineering.
- Dynamic image generation with varying styles (e.g., Van Gogh painting, oil painting).
- Image quality improvements through custom parameters like `guidance_scale` and `num_inference_steps`.

## Installation

### Prerequisites:
- Python 3.8+
- CUDA-enabled GPU
- PyTorch
- Required Python libraries:

```bash
pip install torch torchvision torchaudio
pip install transformers diffusers
```

### Clone the Repository:
```bash
git clone https://github.com/Takshi18/Enhancing-Control-in-Stable-Diffusion-Through-Example-Based-Fine-Tuning-and-Prompt-Engineering
cd Enhancing-Control-in-Stable-Diffusion-Through-Example-Based-Fine-Tuning-and-Prompt-Engineering
```

## Usage

The project generates images based on a list of prompts and avoids generating unwanted elements using negative prompts. Below are input/output image examples.

### Input Image:
https://drive.google.com/file/d/1s8Qx1Ez7BEnVhoneQUBPehAn1Bx66Y7W/view?usp=sharing

### Generated Output:
https://drive.google.com/file/d/1oNxMnbcDcBMcZycMUsN8pgMelcLvlSTm/view?usp=sharing
https://drive.google.com/file/d/1E2Ff_tO1s182Mh22AGm84FTxAvmEyyWQ/view?usp=sharing


The project allows you to modify the prompt lists and fine-tuning parameters as needed. Once set, you can run the Python script or notebook to generate images.

## Parameters

- `prompt_list`: A list of positive prompts used to direct the model in generating desired images.
- `negative_prompt_list`: A list of negative prompts to avoid generating unwanted features.
- `num_samples`: Number of images to generate for each prompt.
- `guidance_scale`: Controls the adherence to the text prompt (higher values mean the model follows the prompt more strictly).
- `num_inference_steps`: Number of diffusion steps for generating the image (higher values produce more detailed images).
- `height` and `width`: Dimensions of the output image.
- `seed`: Ensures reproducibility by controlling random initialization.

## Prompt Lists

### Positive Prompts:

```python
prompt_list = [
    "photo of road",
    "van gogh painting of zwx road",
    "photo of zwx in autumn in new york with orange trees",
    "oil painting of zwx road in snow"
]
```

### Negative Prompts:

```python
negative_prompt_list = [
    "cartoon", "unrealistic", "blurry", "low quality", "low definition",
    "lowres", "out of frame", "out of focus", "tilted", "distorted", "painting",
    "sketch", "drawing", "water", "people", "animals", "vehicles", "traffic lights",
    "signs", "buildings", "sky", "grass", "sunset", "sunrise", "night", "indoors", "blurred motion"
]
```

## Results

The project outputs a set of generated images based on the prompts provided. The negative prompts help in refining the generated images by avoiding undesirable characteristics like blurriness, low quality, and distortion.

### Input Image (Snowy Landscape):
![Input Image](./mnt/data/Screenshot%202024-10-01%20at%206.34.02%20PM.png)

### Generated Output:
*Apply styles like Van Gogh, oil painting, etc., based on prompt configurations.*

---
