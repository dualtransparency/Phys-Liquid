---
title: Phys-Liquid
---

# Phys-Liquid: A Physics-Informed Dataset for Estimating 3D Geometry and Volume of Transparent Deformable Liquids

**AAAI-26 (Oral)**

Ke Ma, et al.

---

## Overview

Phys-Liquid is a physics-informed simulation dataset of transparent deformable liquids in realistic laboratory scenes.  
It provides multi-view RGB images, high-quality liquid masks, metrically scaled 3D meshes, and rich physical metadata to support research on:

- 3D geometry and volume estimation of transparent liquids
- Physics-aware 3D reconstruction
- World models and scene graphs in laboratory environments
- Robotic perception and manipulation in wet lab settings

The dataset is accompanied by a four-stage reconstruction pipeline and benchmark results against strong baselines such as InstantMesh and TriPoSR.

---

## Resources

- **AAAI-26 paper**: (coming soon – official proceedings link)
- **Extended version (arXiv)**: (coming soon – arXiv link)

- **Code repository**: [Phys-Liquid-AAAI](https://github.com/dualtransparency/Phys-Liquid-AAAI)  
- **Dataset download**: [Phys-Liquid-AAAI](https://github.com/dualtransparency/Phys-Liquid-AAAI)

---

## Dataset

Phys-Liquid contains:

- Multi-view RGB images rendered from physics-based simulations of transparent liquids
- Diverse liquid states: different volumes, colors, viscosities, and container types
- Accurate per-pixel liquid masks for each view
- 3D liquid meshes with metric scaling
- Detailed metadata describing camera parameters, physical properties, and scene configuration

The GitHub repository provides:

- A **sample subset** for quick experiments
- Scripts to download or reconstruct the **full dataset**
- Data loaders and utilities for integrating Phys-Liquid into your own pipelines

---

## Method Overview

We propose a four-stage physics-informed reconstruction pipeline:

1. **Transparent-Liquid Segmentation**  
   Segment the transparent liquid region from RGB images using a specialized segmentation model.

2. **Multi-View Mask Diffusion**  
   Use a diffusion-based model to refine and complete liquid masks across multiple views, enforcing multi-view consistency.

3. **3D Reconstruction**  
   Reconstruct a coarse 3D shape from the multi-view masks using a standard reconstruction backbone (e.g., InstantMesh / TriPoSR).

4. **Mesh Scaling to Metric Dimensions**  
   Apply a physics-informed mesh scaling model to recover metric volume and geometry that match the underlying physical simulation.

The repository contains code for training and evaluating key components, as well as configurations to reproduce the main experiments.

---

## Results and Applications

Phys-Liquid enables quantitative evaluation of:

- 3D reconstruction quality for transparent, deformable liquids
- Volume estimation accuracy under different containers and views
- Robustness of models to changes in lighting, camera pose, and liquid state

We demonstrate that:

- Our pipeline significantly improves geometry and volume estimation over strong baselines.
- The dataset can serve as a testbed for world-model-based reasoning and robotic manipulation in lab environments.

---

## Citation

If you find Phys-Liquid useful in your research, please cite:

```bibtex
@inproceedings{ma2026physliquid,
  title     = {Phys-Liquid: A Physics-Informed Dataset for Estimating 3D Geometry and Volume of Transparent Deformable Liquids},
  author    = {Ma, Ke and others},
  booktitle = {Proceedings of the AAAI Conference on Artificial Intelligence},
  year      = {2026}
}
