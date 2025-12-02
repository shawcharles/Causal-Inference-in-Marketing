# Synthetic Control Figures for Chapter 6

This directory contains the figure generation scripts and output files for Chapter 6: Synthetic Control.

## Generated Figures

### Figure 6.1: Pre-Treatment Fit and Post-Treatment Gap Plot
- **Files**: `fig_sc_gap.pdf`, `fig_sc_gap.png`
- **Script**: `fig_sc_gap.py`
- **Description**: Two-panel diagram showing:
  - Panel A: Treated unit (solid line) vs synthetic control (dashed line) over full sample period
  - Panel B: Gap (treated minus synthetic) over time with pre/post-treatment shading
- **Key features**:
  - 36 pre-treatment periods, 12 post-treatment periods
  - Vertical line marks intervention time
  - Demonstrates good pre-treatment fit and clear post-treatment divergence
  - Shows ramp-up effect pattern

### Figure 6.2: Donor Weight Distribution and Support
- **Files**: `fig_sc_weights.pdf`, `fig_sc_weights.png`
- **Script**: `fig_sc_weights.py`
- **Description**: Two-panel diagram showing:
  - Panel A: Bar chart of donor weights (sorted by magnitude)
  - Panel B: Predictor balance table comparing treated unit, synthetic control, and top donors
- **Key features**:
  - 40 donor units with realistic sparse weight distribution
  - Highlights top donors (weight > 0.05) in red
  - Shows uniform weight reference line
  - Demonstrates predictor balance across 5 key variables

### Figure 6.3: Placebo (In-Space) Gap Distribution and RMSPE Ratio
- **Files**: `fig_sc_placebo.pdf`, `fig_sc_placebo.png`
- **Script**: `fig_sc_placebo.py`
- **Description**: Two-panel diagram showing:
  - Panel A: Post-treatment gaps for treated unit vs all placebo units
  - Panel B: RMSPE ratio distribution with treated unit highlighted
- **Key features**:
  - 40 placebo units (grey lines) vs treated unit (bold red line)
  - Treated unit gap is clear outlier in post-treatment period
  - RMSPE ratio distribution shows treated unit in extreme tail
  - Includes p-value calculation and rank statistics

## Regenerating Figures

To regenerate all figures, run:

```bash
cd /home/user/Documents/MONOGRAPH/Causal_panel_data_book_Template/figures
python generate_sc_figures.py
```

Or run individual scripts:

```bash
python fig_sc_gap.py
python fig_sc_weights.py
python fig_sc_placebo.py
```

## Requirements

- Python 3.x
- numpy
- matplotlib

## Figure Specifications

All figures are generated with:
- **Format**: PDF (for LaTeX) and PNG (for preview)
- **DPI**: 300 (high resolution)
- **Style**: Academic publication quality
- **Font**: Serif (matching book style)
- **Color scheme**: Professional with red highlights for key elements

## LaTeX Integration

Figures are referenced in the LaTeX file as:

```latex
\begin{figure}[htbp]
\centering
\includegraphics[width=0.95\textwidth]{images/fig_sc_gap.pdf}
\caption{Pre-Treatment Fit and Post-Treatment Gap Plot}
\label{fig:sc-gap}
...
\end{figure}
```

## Notes

- All figures use reproducible random seeds for consistency
- Data is simulated to illustrate synthetic control concepts
- Figures follow the design specifications from the original LaTeX placeholders
- Panel layouts and annotations match academic standards for econometric methods
