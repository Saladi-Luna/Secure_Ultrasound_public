# Quick Start Guide

Welcome to the visual examples directory for your manuscript on fetal head ultrasound classification!

## 🚀 Getting Started

This repository is now structured to help you organize all visual materials for your manuscript. Here's how to use it:

## 📁 Where to Put Your Figures

1. **Model Architecture Diagrams** → `figures/architecture/`
   - Network topology, layer visualizations, model design

2. **Sample Data & Images** → `figures/data_examples/`
   - Example ultrasound images, class distribution charts, augmentation examples

3. **Preprocessing Visualizations** → `figures/preprocessing/`
   - Normalization effects, preprocessing pipeline diagrams

4. **Experimental Results** → `figures/results/`
   - Training curves, performance comparisons, ablation studies

5. **Confusion Matrices** → `figures/confusion_matrices/`
   - Classification results, error analysis

6. **Diagnostic Plots** → `figures/roc_curves/`
   - ROC curves, precision-recall curves, AUC comparisons

## 📝 File Naming Convention

Use this pattern: `fig_XX_descriptive_name.png`

Examples:
- `fig_01_model_architecture.png`
- `fig_02_class_distribution.png`
- `fig_03_training_curves.png`
- `supp_01_additional_results.png` (for supplementary figures)

## ✅ Before Adding a Figure

1. Check the subdirectory README for specific guidelines
2. Ensure resolution is at least 300 DPI
3. Use color-blind friendly colors (see PUBLICATION_GUIDELINES.md)
4. Test readability in grayscale
5. Follow consistent styling across all figures

## 📚 Helpful Resources

- **`README.md`** - Overview of directory structure
- **`FIGURE_CAPTIONS.md`** - Templates for writing captions
- **`PUBLICATION_GUIDELINES.md`** - Detailed guide for publication-quality figures
- **Subdirectory READMEs** - Specific guidance for each figure type

## 🎨 Creating Figures with Python

### Quick Example (Matplotlib)

```python
import matplotlib.pyplot as plt

# Set publication quality
plt.rcParams['figure.dpi'] = 300
plt.rcParams['font.size'] = 10

# Create your plot
fig, ax = plt.subplots(figsize=(7, 5))
# ... your plotting code ...

# Save
plt.savefig('figures/results/fig_09_training_curves.png', 
            dpi=300, bbox_inches='tight')
```

### Quick Example (Confusion Matrix)

```python
import seaborn as sns
import matplotlib.pyplot as plt

fig, ax = plt.subplots(figsize=(8, 6))
sns.heatmap(confusion_matrix, annot=True, fmt='.1f', 
            cmap='Blues', ax=ax)
ax.set_xlabel('Predicted Label')
ax.set_ylabel('True Label')
plt.savefig('figures/confusion_matrices/fig_13_confusion_matrix.png',
            dpi=300, bbox_inches='tight')
```

## 📊 Typical Manuscript Figure Set

A typical manuscript might include:

**Main Figures (5-7):**
1. Model architecture
2. Data distribution showing class imbalance
3. Sample images from each class
4. Training/validation curves
5. Performance comparison across models
6. Confusion matrix
7. ROC curves

**Supplementary Figures:**
- Additional sample images
- Preprocessing examples
- Ablation study details
- Per-class performance breakdowns
- Additional diagnostic plots

## ✨ Pro Tips

1. **Create figures early**: Generate all figures as you complete experiments
2. **Version control**: Use meaningful commit messages when adding figures
3. **Consistent style**: Set up a matplotlib style file for consistency
4. **Backup**: Keep raw data/scripts to regenerate figures if needed
5. **Organize**: Put each figure in the correct subdirectory from the start

## 🔄 Workflow Example

1. Run experiment and generate results
2. Create visualization with appropriate script
3. Save to correct subdirectory with proper naming
4. Write caption in FIGURE_CAPTIONS.md
5. Review figure against PUBLICATION_GUIDELINES.md
6. Commit to repository

## 💡 Next Steps

1. Start adding your figures to the appropriate directories
2. Fill in the FIGURE_CAPTIONS.md template
3. Ensure all figures meet publication guidelines
4. Update this README with any project-specific conventions

## ❓ Need Help?

- Check subdirectory READMEs for specific guidance
- Refer to PUBLICATION_GUIDELINES.md for technical details
- Review FIGURE_CAPTIONS.md for caption examples

---

Happy figure making! 🎉
