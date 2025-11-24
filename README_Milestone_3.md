# Generative AI Room Decorator – Milestone 3

## Overview

Milestone 3 focuses on **model evaluation, results analysis, and experiment tracking** for the Generative AI Room Decorator project. The main goal is to analyze how different hyperparameters and model configurations impact the quality of generated room images.

---

## Main Objective

The objective of Milestone 3 is to:

- Evaluate the performance of the generative model using quantitative metrics and qualitative analysis.  
- Compare different configurations and hyperparameters.  
- Document results in structured tables and plots.  
- Provide insights for improving model outputs in future iterations.

---

## Contents

The Milestone 3 folder contains the following key items:

```
notebooks/
Generative_Project_Milestone3.ipynb # Main evaluation notebook
outputs/
milestone3_results.csv # Quantitative results (e.g., CLIP scores, metrics)
milestone3_generated/ # Generated room images
milestone3_cfg/ # Configuration files used for experiments
milestone3_embeddings/ # Embeddings or intermediate representations
README.md # Project-level README
```


---

## Methods

1. **Evaluation Notebook**  
   - Loads the trained generative model.  
   - Runs evaluation on validation/test images.  
   - Computes metrics such as CLIP score, FID, or any task-specific metrics.

2. **Data Handling**  
   - Input datasets are loaded from `data/` (COCO subset or custom room images).  
   - Results are stored in `outputs/` for reproducibility.

3. **Visualization**  
   - Generated images and results are plotted for visual inspection.  
   - Metrics are tabulated to summarize performance across different settings.

---

## Results

- `milestone3_results.csv` contains the final metrics for all experiments.  
- Generated images are stored in `outputs/milestone3_generated/`.  
- Configuration details for reproducibility are in `milestone3_cfg/`.  

Plots and tables in the notebook provide a clear comparison of model performance under different settings.

---

## Usage

1. Open `notebooks/Generative_Project_Milestone3.ipynb` in Colab or Jupyter.  
2. Run the cells sequentially to reproduce evaluation metrics and visualizations.  
3. Adjust configuration files in `milestone3_cfg/` to experiment with new parameters.  

---

## Notes

- Large datasets and outputs (e.g., COCO images, generated images) are not tracked in Git and should be downloaded separately if needed.  
- Ensure the appropriate Python environment with required packages is available to run the notebook.
