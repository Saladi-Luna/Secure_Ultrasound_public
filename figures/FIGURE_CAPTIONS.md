# Figure Captions Template

This document provides a template for writing figure captions for the manuscript.

## Main Figures

### Figure 1: Model Architecture
**File:** `architecture/fig_01_overall_architecture.png`

**Caption:** Deep learning model architecture for fetal head ultrasound anatomical plane classification. The network consists of [describe layers], designed to handle class imbalance through [describe approach].

---

### Figure 2: Data Distribution
**File:** `data_examples/fig_04_class_distribution.png`

**Caption:** Distribution of fetal head ultrasound images across anatomical plane classes in the training dataset, illustrating the class imbalance problem. [Add specific numbers and classes].

---

### Figure 3: Sample Ultrasound Images
**File:** `data_examples/fig_05_sample_images_per_class.png`

**Caption:** Representative examples of fetal head ultrasound images for each anatomical plane class: [list classes]. Images demonstrate the visual variability within and between classes.

---

### Figure 4: Training Performance
**File:** `results/fig_09_training_curves.png`

**Caption:** Training and validation accuracy and loss curves over epochs. The model demonstrates [describe convergence behavior] with final validation accuracy of [X]%.

---

### Figure 5: Model Comparison
**File:** `results/fig_10_model_comparison.png`

**Caption:** Comparison of classification performance across different approaches: [list approaches]. Metrics include overall accuracy, per-class precision, recall, and F1-scores.

---

### Figure 6: Confusion Matrix
**File:** `confusion_matrices/fig_13_confusion_matrix_best_model.png`

**Caption:** Confusion matrix for the best-performing model on the test set. Rows represent true classes and columns represent predicted classes. The matrix is [normalized/not normalized] to show [percentage/count].

---

### Figure 7: ROC Curves
**File:** `roc_curves/fig_16_roc_curves_all_classes.png`

**Caption:** Receiver Operating Characteristic (ROC) curves for all anatomical plane classes using one-vs-rest approach. The area under the curve (AUC) values are: [list AUCs per class].

---

## Supplementary Figures

### Supplementary Figure 1: Preprocessing Pipeline
**File:** `preprocessing/fig_07_preprocessing_pipeline.png`

**Caption:** Complete preprocessing pipeline showing steps from raw ultrasound image to model-ready input, including [list preprocessing steps].

---

### Supplementary Figure 2: Data Augmentation
**File:** `data_examples/fig_06_augmentation_examples.png`

**Caption:** Examples of data augmentation techniques applied to address class imbalance, including [list augmentation methods]. Each row shows the original image followed by augmented variations.

---

### Supplementary Figure 3: Ablation Study
**File:** `results/fig_12_ablation_results.png`

**Caption:** Ablation study results showing the contribution of different model components: [list components]. Performance is measured using [metric].

---

### Supplementary Figure 4: Precision-Recall Curves
**File:** `roc_curves/fig_17_precision_recall_curves.png`

**Caption:** Precision-Recall curves for each anatomical plane class. Average precision (AP) scores are: [list APs per class].

---

## Guidelines for Caption Writing

1. **Be specific**: Include actual values, class names, and metrics
2. **Be concise**: Keep captions focused and informative
3. **Define abbreviations**: First use should include full term
4. **Explain axes**: Clarify what x and y axes represent
5. **Highlight key findings**: Draw attention to important observations
6. **Use consistent terminology**: Match terms used in the manuscript text
7. **Include units**: Always specify units for measurements
8. **Maintain objectivity**: Present findings without over-interpretation

## Example of a Complete Caption

"**Figure 1: Deep Learning Model Architecture.** Convolutional neural network architecture for anatomical plane classification of fetal head ultrasound images. The model consists of five convolutional blocks (Conv1-Conv5) with batch normalization and max pooling, followed by three fully connected layers (FC1-FC3). Input images are 224×224 pixels grayscale. The network employs focal loss to address class imbalance, with focal parameter γ=2. Feature maps at each convolutional layer are shown above the corresponding block. The final softmax layer outputs probabilities for N classes representing different anatomical planes. Total trainable parameters: X million."
