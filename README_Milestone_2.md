# Milestone 2: Text Encoder Integration and Conditional Generation Analysis

This document describes the work completed in Milestone 2 of the Generative AI Room Decorator project. The focus of this stage is to integrate a text encoder with the diffusion model, run baseline conditional generation, tune key hyperparameters such as classifier-free guidance and noise schedule, and record the first set of generated images. All code for this milestone is available in the notebook located at:

```
notebooks/Generative_Project_Milestone_2.ipynb
```

---

## Objectives

- Integrate CLIP/BERT text encoder with Stable Diffusion for explicit prompt embedding.
- Run baseline conditional generation using raw text prompts.
- Tune classifier-free guidance for prompt adherence and generation diversity.
- Compare diffusion schedulers and study their effects on image quality.
- Save and document early generated samples for evaluation.

---

## 1. Text Encoder Integration

The CLIP text encoder used internally by Stable Diffusion was extracted and used explicitly to generate:

- Prompt embeddings  
- Negative prompt embeddings  

Two helper functions were implemented:

- `encode_prompts()` for generating embeddings  
- `generate_images_from_embeds()` for using embeddings directly in the diffusion pipeline  

This enables fine-grained control over semantic conditioning, crucial for later fine-tuning stages.

---

## 2. Baseline Conditional Generation

Five baseline images were generated using the pretrained `runwayml/stable-diffusion-v1-5` model.  
Default settings:

- Scheduler: PNDM  
- Inference steps: 30  
- Classifier-free guidance: 7.5  

These results serve as reference outputs for comparison with tuned configurations.

Outputs saved in:

```
baseline_outputs/
```

---

## 3. Classifier-Free Guidance Tuning

Classifier-free guidance (CFG) values of 3, 5, 7.5, 10, and 12 were tested.

Observations:

- CFG 3–5: more variation, weaker alignment  
- CFG 7.5: balanced structure and realism  
- CFG 10–12: high adherence but visible artifacts  

Outputs saved in:

```
cfg_scheduler_outputs/
```


---

## 4. Noise Scheduler Evaluation

Four schedulers were evaluated:

- PNDM (default)
- DDIM
- Euler Ancestral
- LMSDiscrete

Findings:

- Euler Ancestral generated sharper indoor layouts and better lighting consistency.  
- DDIM produced faster but softer results.  
- LMS added smoothness but distorted room geometry.  
- PNDM remained stable but soft.  

Scheduler outputs saved in:
```
cfg_scheduler_outputs/
```

---

## 5. Early Sample Set

A collection of 5–10 images was recorded from:

- Baseline generation  
- CFG tuning  
- Scheduler experiments  

Image folders:

```
baseline_outputs/
cfg_scheduler_outputs/
milestone2_outputs/
```

These samples form the early benchmark set for assessing improvements in future fine-tuning stages.

---

## Summary of Findings

- Text encoder integration allows direct conditioning using embeddings (shape: batch × 77 × 768), enabling more advanced control in future milestones.
- Baseline generation validates the model’s alignment with indoor-scene prompts.
- CFG tuning demonstrates a clear trade-off between adherence and visual artifact formation.
- Euler Ancestral scheduler provides the best overall quality for indoor room generation.
- The collected image set establishes a strong baseline for future evaluation and fine-tuning.

---
