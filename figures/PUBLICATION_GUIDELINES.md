# Publication-Quality Figure Guidelines

This guide provides best practices for creating high-quality figures for manuscript submission.

## General Requirements

### Resolution and File Format
- **Resolution**: Minimum 300 DPI (dots per inch) for print publication
- **Recommended formats**:
  - PNG: For plots, charts, and images with sharp edges
  - PDF: For vector graphics (scalable without quality loss)
  - TIFF: Alternative for high-quality images
  - JPEG: Avoid for publication (lossy compression)

### Size Specifications
- **Single column**: Width ≤ 3.5 inches (9 cm)
- **Double column**: Width ≤ 7 inches (18 cm)
- **Height**: Typically ≤ 9 inches (23 cm)
- **File size**: Keep under 10MB per figure when possible

## Color Guidelines

### Color Palette
- **Use color-blind friendly palettes**: Approximately 8% of males have color vision deficiency
- **Recommended palettes**:
  - Viridis, Plasma, Inferno (perceptually uniform)
  - ColorBrewer palettes (designed for accessibility)
  - Avoid red-green combinations alone

### Grayscale Compatibility
- Figures should be interpretable when printed in grayscale
- Test by converting to grayscale before finalizing
- Use different line styles (solid, dashed, dotted) in addition to colors

### Contrast
- Ensure sufficient contrast between elements
- Dark text on light background or vice versa
- Minimum contrast ratio of 4.5:1 for text

## Typography

### Font Requirements
- **Font family**: Sans-serif fonts (Arial, Helvetica, Calibri) preferred for clarity
- **Font size**:
  - Axis labels: 10-12 pt
  - Tick labels: 8-10 pt
  - Titles: 12-14 pt (if included)
  - Legend text: 8-10 pt
- **Consistency**: Use the same font family across all figures

### Text Guidelines
- Keep text horizontal when possible
- Avoid rotated text except for y-axis labels
- Use sentence case for labels
- Define abbreviations in captions

## Layout and Design

### White Space
- Adequate margins around figure elements
- Clear separation between subplots
- Not too cluttered or too sparse

### Axes and Grid
- **Axes**: Clearly labeled with units
- **Tick marks**: Point inward or outward consistently
- **Grid lines**: Optional, use sparingly (light gray, thin)
- **Axis limits**: Appropriate range to show data clearly

### Legends
- Place legends inside or outside plot area consistently
- Use clear, descriptive labels
- Order items logically
- Avoid covering data

### Multi-panel Figures
- Label panels with (A), (B), (C), etc.
- Use consistent sizing across panels
- Align panels properly
- Maintain consistent styles

## Specific Figure Types

### Plots and Charts

#### Line Plots
- Line width: 1.5-2 pt for main data
- Marker size: 4-6 pt if used
- Use different line styles for multiple series
- Include error bars/confidence intervals when appropriate

#### Bar Charts
- Bar width: Not too wide or narrow
- Gap between bars: Consistent
- Error bars: Clearly visible
- Use patterns/hatching for grayscale compatibility

#### Heatmaps
- Use perceptually uniform colormaps
- Include colorbar with scale
- Label rows and columns clearly
- Consider annotating cells with values

### Confusion Matrices
- Normalize (percentage) or show counts
- Use sequential colormap (light to dark)
- Include colorbar
- Label axes: "True Label" and "Predicted Label"
- Consider adding text annotations in cells

### ROC Curves
- Plot diagonal reference line (chance level)
- Include AUC values in legend
- Use different colors/styles for multiple curves
- Label axes: "False Positive Rate" and "True Positive Rate"
- Set axes limits to [0, 1]

### Medical Images
- Use appropriate medical image colormap (grayscale or specialty maps)
- Include scale bar when relevant
- Maintain aspect ratio
- Anonymize patient information
- Consider adding anatomical labels/arrows

### Architecture Diagrams
- Use clear, simple shapes
- Consistent style across all architecture figures
- Include dimensions/sizes of layers
- Use arrows to show data flow
- Add legends for different component types

## Python Matplotlib Example

```python
import matplotlib.pyplot as plt
import numpy as np

# Set publication-quality defaults
plt.rcParams['figure.dpi'] = 300
plt.rcParams['font.size'] = 10
plt.rcParams['font.family'] = 'sans-serif'
plt.rcParams['font.sans-serif'] = ['Arial']
plt.rcParams['axes.linewidth'] = 1.0
plt.rcParams['lines.linewidth'] = 1.5

# Create figure with appropriate size (in inches)
fig, ax = plt.subplots(figsize=(7, 5))

# Example plot
x = np.linspace(0, 10, 100)
y1 = np.sin(x)
y2 = np.cos(x)

ax.plot(x, y1, label='Model A', color='#1f77b4', linestyle='-')
ax.plot(x, y2, label='Model B', color='#ff7f0e', linestyle='--')

# Formatting
ax.set_xlabel('Epoch', fontsize=12)
ax.set_ylabel('Accuracy (%)', fontsize=12)
ax.legend(frameon=False, loc='best')
ax.grid(True, alpha=0.3)
ax.spines['top'].set_visible(False)
ax.spines['right'].set_visible(False)

# Save with high DPI
plt.tight_layout()
plt.savefig('figure.png', dpi=300, bbox_inches='tight')
plt.savefig('figure.pdf', bbox_inches='tight')  # Vector version
```

## Python Seaborn Example

```python
import seaborn as sns
import matplotlib.pyplot as plt
import numpy as np

# Set style
sns.set_style("whitegrid")
sns.set_context("paper", font_scale=1.2)

# Create confusion matrix heatmap
cm = np.random.rand(5, 5) * 100  # Example data
fig, ax = plt.subplots(figsize=(8, 6))

sns.heatmap(cm, annot=True, fmt='.1f', cmap='Blues', 
            xticklabels=['Class A', 'Class B', 'Class C', 'Class D', 'Class E'],
            yticklabels=['Class A', 'Class B', 'Class C', 'Class D', 'Class E'],
            cbar_kws={'label': 'Percentage (%)'})

ax.set_xlabel('Predicted Label', fontsize=12)
ax.set_ylabel('True Label', fontsize=12)

plt.tight_layout()
plt.savefig('confusion_matrix.png', dpi=300, bbox_inches='tight')
```

## Checklist Before Submission

- [ ] Resolution is at least 300 DPI
- [ ] File format is appropriate (PNG, PDF, or TIFF)
- [ ] Figure size fits journal requirements
- [ ] Colors are color-blind friendly
- [ ] Figure is readable in grayscale
- [ ] Font sizes are appropriate and consistent
- [ ] Axes are labeled with units
- [ ] Legend is clear and well-placed
- [ ] No unnecessary elements (remove clutter)
- [ ] Multi-panel figures are properly labeled
- [ ] Image files are optimized for size
- [ ] All text is legible at final size
- [ ] Caption is complete and informative
- [ ] Figure matches description in manuscript text

## Journal-Specific Requirements

Always check your target journal's specific requirements for:
- Figure dimensions
- File format preferences
- Color space (RGB vs CMYK)
- Font specifications
- Supplementary material guidelines

Common journals in medical imaging:
- **IEEE Transactions on Medical Imaging**: 300 DPI, TIFF/PNG/PDF
- **Medical Image Analysis**: 300 DPI, vector formats preferred
- **Radiology**: High-resolution TIFF or EPS
- **Nature/Science**: Very specific guidelines, check carefully

## Resources

- **ColorBrewer**: https://colorbrewer2.org/
- **Color blindness simulator**: https://www.color-blindness.com/coblis-color-blindness-simulator/
- **Matplotlib documentation**: https://matplotlib.org/
- **Seaborn documentation**: https://seaborn.pydata.org/

## Common Mistakes to Avoid

1. **Low resolution**: Using 72 DPI screen resolution for print
2. **Small fonts**: Text too small to read at final size
3. **Poor contrast**: Light colors on white background
4. **Cluttered plots**: Too many elements competing for attention
5. **Inconsistent style**: Different fonts or colors across figures
6. **Missing labels**: Unlabeled axes or unclear legends
7. **Pixelated images**: Raster images scaled beyond original resolution
8. **No colorbar**: Heatmaps without scale reference
9. **Truncated labels**: Text cut off at edges
10. **Incorrect aspect ratio**: Distorted images or plots
