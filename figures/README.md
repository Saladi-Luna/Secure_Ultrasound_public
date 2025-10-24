# Visual Examples for Manuscript

This directory contains all visual examples and figures used in the manuscript on "Anatomical Plane Classification for Fetal Head Ultrasound - Addressing Class Imbalance with Deep Learning".

## Directory Structure

### 1. `architecture/`
Contains diagrams and visualizations of the neural network architecture and model design:
- Model architecture diagrams
- Layer visualizations
- Network topology illustrations
- Feature extraction pipeline diagrams

### 2. `data_examples/`
Contains sample ultrasound images and data visualization:
- Example fetal head ultrasound images by class
- Data distribution plots
- Class imbalance visualizations
- Augmentation examples (before/after)

### 3. `preprocessing/`
Contains visualizations of preprocessing steps:
- Image normalization examples
- Preprocessing pipeline diagrams
- Quality control visualizations
- Data augmentation techniques

### 4. `results/`
Contains experimental results and performance metrics:
- Training/validation curves
- Loss curves over epochs
- Accuracy plots
- Comparative performance charts
- Ablation study results

### 5. `confusion_matrices/`
Contains confusion matrix visualizations:
- Confusion matrices for different models
- Per-class performance heatmaps
- Error analysis visualizations

### 6. `roc_curves/`
Contains ROC curve and related diagnostic plots:
- ROC curves for multi-class classification
- Precision-Recall curves
- AUC comparisons across models
- Class-specific performance curves

## File Naming Convention

Please follow these naming conventions for consistency:

- `fig_XX_description.png` - Main figures (where XX is the figure number)
- `supp_XX_description.png` - Supplementary figures
- `table_XX_description.png` - Table visualizations
- Use lowercase with underscores
- Use descriptive names (e.g., `fig_01_model_architecture.png`)

## Image Format Guidelines

- **Primary format**: PNG (lossless, good for diagrams and plots)
- **Alternative**: PDF (vector graphics, good for publication)
- **Resolution**: Minimum 300 DPI for publication quality
- **Size**: Keep individual files under 10MB when possible

## Usage in Manuscript

When referencing figures in your manuscript:
- Use relative paths from the repository root
- Include figure captions in your manuscript
- Cross-reference with figure numbers
- Provide alt text for accessibility

Example reference in LaTeX:
```latex
\begin{figure}[h]
\centering
\includegraphics[width=0.8\textwidth]{figures/architecture/fig_01_model_architecture.png}
\caption{Deep learning model architecture for fetal head ultrasound classification.}
\label{fig:model_arch}
\end{figure}
```

## Contributing

When adding new figures:
1. Place them in the appropriate subdirectory
2. Follow the naming convention
3. Update this README if adding new categories
4. Ensure images are optimized for size
5. Include a brief description in commit messages

## Notes

- All figures should be publication-ready
- Ensure proper attribution if using external images
- Consider color-blind friendly palettes
- Maintain consistent styling across all figures
