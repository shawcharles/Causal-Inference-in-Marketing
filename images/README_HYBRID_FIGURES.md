# Hybrid Method Figures for Chapter 7

This directory contains Python scripts to generate figures for Chapter 7 (Generalized and Augmented Synthetic Control).

## Figures

### 1. `fig_hybrid_fit.pdf` - Pre-Treatment Fit Comparison
**Script**: `fig_hybrid_fit.py`  
**Label**: `fig:hybrid-fit`

**Description**: Two-panel diagram comparing standard synthetic control (SC) and augmented synthetic control (ASCM).

**Panel A**: Shows trajectories over time
- Treated unit (solid blue line with circles)
- Standard SC (dashed purple line with squares)
- Augmented SC/ASCM (dotted orange line with triangles)
- Vertical line marks intervention time
- Shaded regions indicate pre/post treatment periods

**Panel B**: Shows gaps (treated minus synthetic) over time
- SC gap with 95% confidence interval (purple)
- ASCM gap with 95% confidence interval (orange)
- Demonstrates that ASCM achieves better pre-treatment fit (smaller RMSPE)
- Both methods show treatment effects in post-treatment period

**Key Features**:
- ASCM fits pre-treatment trajectory more closely than SC
- Pre-treatment RMSPE values displayed
- Confidence intervals show uncertainty
- Clear visualization of treatment effect emergence

---

### 2. `fig_hybrid_sdid.pdf` - SDID Unit and Time Weights
**Script**: `fig_hybrid_sdid.py`  
**Label**: `fig:hybrid-sdid`

**Description**: Two-panel diagram showing SDID weight distributions.

**Panel A**: Unit weights distribution
- Bar chart of donor unit weights (sorted by magnitude)
- Red bars indicate donors with weights > 0.1 (high influence)
- Blue bars indicate donors with weights ≤ 0.1
- Dashed line shows uniform weight (1/N)
- Effective number of donors (N_eff) displayed
- Shows weight concentration on few key donors

**Panel B**: Time weights distribution
- Bar chart of pre-treatment period weights
- Green bars indicate periods with above-average weights
- Blue bars indicate periods with below-average weights
- Dashed line shows uniform weight (1/T)
- Effective number of periods (T_eff) displayed
- Shows how SDID down-weights volatile periods

**Key Features**:
- Demonstrates sparse unit weights (few donors dominate)
- Shows moderate time weight dispersion
- Effective numbers quantify concentration
- Annotations explain interpretation

---

### 3. `fig_hybrid_ridge.pdf` - Ridge Regularization Path
**Script**: `fig_hybrid_ridge.py`  
**Label**: `fig:hybrid-ridge`

**Description**: Two-panel diagram showing ridge regularization effects.

**Panel A**: Ridge path for donor weights
- Multiple lines, each representing one donor's weight trajectory
- X-axis: Ridge penalty η (log scale)
- Y-axis: Donor weights
- Shows how weights shrink toward uniform (1/N) as η increases
- Orange vertical line marks CV-optimal η
- Red dashed line shows uniform weight target
- Colorful lines show individual donor paths

**Panel B**: Effective number of donors vs η
- Shows N_eff as function of ridge penalty
- Orange point marks CV-optimal choice
- Demonstrates trade-off: low η = sparse, high η = diffuse
- Shaded regions indicate under/over-regularization

**Key Features**:
- Visualizes bias-variance trade-off
- Shows shrinkage toward uniform weights
- CV-optimal η balances fit and stability
- Clear interpretation of regularization effects

---

## Generating the Figures

### Quick Start
```bash
cd figures
python generate_hybrid_figures.py
```

This will generate all three figures in both PDF and PNG formats.

### Individual Figures
```bash
python fig_hybrid_fit.py
python fig_hybrid_sdid.py
python fig_hybrid_ridge.py
```

### Requirements
```bash
pip install numpy matplotlib seaborn
```

**Versions used**:
- numpy >= 1.20.0
- matplotlib >= 3.5.0
- seaborn >= 0.12.0

---

## Output Files

Each script generates two files:
- **PDF**: High-resolution vector graphics for LaTeX inclusion
- **PNG**: Raster graphics for preview/presentations

**Generated files**:
- `fig_hybrid_fit.pdf` and `fig_hybrid_fit.png`
- `fig_hybrid_sdid.pdf` and `fig_hybrid_sdid.png`
- `fig_hybrid_ridge.pdf` and `fig_hybrid_ridge.png`

---

## Figure Specifications

### Design Principles
1. **Publication quality**: 300 DPI, clean layouts
2. **Colorblind friendly**: Distinct colors and line styles
3. **Clear annotations**: Labels, legends, and explanatory text
4. **Consistent style**: Unified aesthetic across all figures

### Color Schemes
- **Treated unit**: Blue (#2E86AB)
- **Standard SC**: Purple (#A23B72)
- **ASCM**: Orange (#F18F01)
- **Emphasis**: Red for high-weight items, green for stable periods

### Typography
- **Titles**: 14pt, bold
- **Axis labels**: 12pt, bold
- **Annotations**: 9-10pt
- **Legends**: 10pt

---

## Customization

### Modifying Data Generation
Each script uses `np.random.seed(42)` for reproducibility. To generate different patterns:
1. Change the seed value
2. Adjust distribution parameters (e.g., `scale` in `np.random.exponential`)
3. Modify time series parameters (trends, seasonality)

### Styling
- Color schemes: Modify color definitions at top of each script
- Figure size: Adjust `figsize` parameter in `plt.subplots()`
- DPI: Change `dpi` parameter in `plt.savefig()`

### Adding Elements
- Additional annotations: Use `ax.annotate()` or `ax.text()`
- More data: Increase `n_donors`, `n_periods`, or `T` parameters
- Different layouts: Modify `gridspec_kw` in subplot creation

---

## Integration with LaTeX

The figures are referenced in Chapter 7 as:

```latex
\begin{figure}[htbp]
\centering
\includegraphics[width=0.95\textwidth]{images/fig_hybrid_fit.pdf}
\caption{Pre-Treatment Fit Comparison: SC vs ASCM with Gap Trajectories}
\label{fig:hybrid-fit}
\end{figure}
```

Similar for `fig:hybrid-sdid` and `fig:hybrid-ridge`.

---

## Troubleshooting

### Common Issues

**1. Module not found errors**
```bash
pip install numpy matplotlib seaborn
```

**2. Figures directory doesn't exist**
```bash
mkdir -p figures
```

**3. Permission errors**
```bash
chmod +x generate_hybrid_figures.py
```

**4. Font warnings**
- These are usually harmless
- To suppress: Set `plt.rcParams['font.family'] = 'DejaVu Sans'`

---

## Notes

- **Simulated data**: All figures use simulated data for illustration
- **Reproducible**: Fixed random seeds ensure consistent output
- **Scalable**: Vector PDFs scale to any size without quality loss
- **Fast**: All three figures generate in < 10 seconds

---

## Contact

For questions about these figures or to request modifications, refer to Chapter 7 of the manuscript.

**Last updated**: 2024
**Chapter**: 7 - Generalized and Augmented Synthetic Control
