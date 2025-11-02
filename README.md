# Generative AI Room Decorator

> A text-to-image generation project using Transformer-based text embeddings (CLIP) and Diffusion models to create realistic interior room designs from textual prompts.

---

## Overview
This project aims to **generate and visualize room interiors** (like kitchens, bedrooms, or living rooms) based on descriptive text inputs such as:
> “A cozy modern kitchen with wooden cabinets and warm lighting.”

Using the **COCO dataset** for object categories and annotations, the model learns semantic relationships between text and visual features. The ultimate goal is to extend this concept into a generative room-decorating system that can visualize layouts dynamically based on size and object constraints.

---

## Key Objectives
- Implement a **text-to-image pipeline** combining:
  - CLIP for text embeddings  
  - Stable Diffusion / Diffusers for image generation  
- Use the **COCO dataset** to identify relevant visual elements (furniture, electronics, kitchen items, etc.)  
- Develop an interface for generating room images based on custom prompts.  
- Prepare for fine-tuning on room-specific categories in later milestones.  

---

## Project  Folder Structure
```bash
generative-ai-room-decorator/
│
├── data/                     # COCO dataset subset (annotations + captions)
├── notebooks/                # Colab notebooks for each milestone
│   └── generative_project_milestone_1.py
├── src/                      # Source code (CLIP, Diffusion, preprocessing)
├── outputs/                  # Generated images, logs
├── configs/                  # Environment and setup files
└── README.md                 # Project documentation
