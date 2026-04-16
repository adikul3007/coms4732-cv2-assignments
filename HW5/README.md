# Diffusion Models & Flow Matching

**COMS 4732W — Computer Vision II (Homework 5)**

This project explores modern generative modeling techniques through diffusion models and flow matching. It combines theoretical foundations with hands-on implementations, covering both pretrained pipelines and models built from scratch.

---

## Overview

The project is divided into two main parts:

### **Part A — The Power of Diffusion Models**

* Implementation and analysis of the forward diffusion process
* Classical vs learned denoising (Gaussian blur vs UNet)
* Iterative denoising and sampling from noise
* Classifier-Free Guidance (CFG) for improved generation
* Image-to-image translation (SDEdit) and inpainting
* Creative applications including:

  * Visual anagrams
  * Hybrid images

### **Part B — Flow Matching from Scratch**

* Implementation of a UNet-based denoiser
* Training on noisy data distributions
* Time-conditioned models
* Sampling using learned flow-based methods
* Exploration of class-conditioned generation

---

## Project Structure

```
.
├── code
│   ├── ash2285_coms4732_hw5a.ipynb
│   ├── ash2285_coms4732_hw5a.pdf
│   ├── ash2285_coms4732_hw5b.ipynb
│   └── ash2285_coms4732_hw5b.pdf
└── web
    ├── assets
    │   ├── alma.jpg
    │   ├── ...
    ├── index.html
    └── web.pdf
```

---

## Getting Started

### Running the Code

All implementations are provided as Jupyter notebooks.

1. Open the notebooks in **Google Colab**:

   * `ash2285_coms4732_hw5a.ipynb` (Part A)
   * `ash2285_coms4732_hw5b.ipynb` (Part B)

2. Run all cells **from top to bottom** without skipping steps

3. Enable GPU runtime in Colab for better performance (T4 GPUs will suffice):

   * Runtime → Change runtime type → GPU

---

## Accessing DeepFloyd IF

This project uses **DeepFloyd IF**, a two-stage diffusion model by Stability AI.

* Stage I generates 64×64 images
* Stage II upsamples them to 256×256

### Setup Steps

1. Create and log in to a Hugging Face account
2. Accept the license for `DeepFloyd/IF-I-XL-v1.0` (this grants access to all IF stages)
3. Generate a Hugging Face access token (read access is sufficient)
4. Authenticate in your notebook using the token

### Prompt Embeddings

DeepFloyd operates on **prompt embeddings**, not raw text. These are 4096-dimensional vector representations of prompts.

To generate them:

* Use the provided Hugging Face embedding tools (Cluster A or B)
* Download the generated `.pth` file
* Load it into your Colab notebook

Note:

* The embedding tools have daily usage limits, so generate embeddings early
* Precomputed embeddings can be used if needed, but generating your own allows more flexibility

---

## Website

You can open `index.html` locally in a browser or deploy it using a static hosting service. The `web/` directory contains a fully designed project showcase:

* `index.html` presents results, visualizations, and explanations
* `assets/` contains generated images and media
* `web.pdf` is a static export of the webpage

---

## Acknowledgements

Made by Aditya Handur-Kulkarni(UNI: ash2285) for COMS4732 Spring 2026