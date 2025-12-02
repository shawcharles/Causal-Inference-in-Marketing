# PlantUML Diagrams

This directory contains PlantUML source files for conceptual diagrams in the book. PlantUML is preferred over Python-generated PNGs for:

- **Architectural diagrams** (method relationships, workflows)
- **Decision trees** (method selection guides)
- **Timelines** (methodological evolution)
- **Process flows** (estimation pipelines)

Python/Matplotlib remains preferred for:
- **Data visualizations** (scatter plots, time series, coefficient plots)
- **Statistical graphics** (distributions, confidence bands)
- **Simulation results** (gap plots, weight distributions)

## Generating Images

### Prerequisites
```bash
# Install PlantUML (requires Java)
# macOS
brew install plantuml

# Ubuntu/Debian
sudo apt-get install plantuml

# Or use the JAR directly
wget https://github.com/plantuml/plantuml/releases/download/v1.2024.0/plantuml-1.2024.0.jar
```

### Generate All Diagrams
```bash
cd images/puml
plantuml -tsvg *.puml      # SVG (vector, recommended for LaTeX)
plantuml -tpdf *.puml      # PDF (vector, direct LaTeX inclusion)
plantuml -tpng -Sdpi=300 *.puml  # PNG (raster, 300 DPI)
```

### Generate Single Diagram
```bash
plantuml -tsvg ecosystem.puml
```

## Output Formats

| Format | Use Case | LaTeX Command |
|--------|----------|---------------|
| SVG | Web, scalable | Requires `svg` package |
| PDF | Print, LaTeX | `\includegraphics{file.pdf}` |
| PNG | Fallback, preview | `\includegraphics{file.png}` |

**Recommendation:** Generate PDF for direct LaTeX inclusion.

## Diagrams in This Directory

### `ecosystem.puml`
**Figure 1.1** — The Marketing Analytics Ecosystem

Four-pillar diagram showing relationships between:
- Randomised Experiments (days–weeks)
- Panel Methods (months–years)  
- Marketing Mix Models (weeks–quarters)
- Attribution Models (real-time)

Central concept: **Triangulation** — multiple methods with different assumptions yield robust conclusions.

## Style Guide

### Colors (consistent with book figures)
```
Experiments:  #E3F2FD (light blue),  border #1565C0
Panels:       #E8F5E9 (light green), border #2E7D32
MMM:          #FFF3E0 (light orange), border #EF6C00
Attribution:  #F3E5F5 (light purple), border #7B1FA2
Center/Key:   #FFECB3 (light amber),  border #F57C00
```

### Typography
- **Titles:** Bold, 12pt
- **Body text:** 10-11pt
- **Captions:** 9pt, gray
- **Font:** DejaVu Sans (cross-platform)

### Layout Principles
1. Use `skinparam shadowing false` for clean look
2. Use `skinparam roundCorner 15` for softer boxes
3. Prefer rectangles/cards over complex shapes
4. Use hidden links for positioning control
5. Keep diagrams simple — one concept per figure

## Integration with LaTeX

```latex
\begin{figure}[htbp]
\centering
\includegraphics[width=\textwidth]{images/puml/ecosystem.pdf}
\caption{The Marketing Analytics Ecosystem: Experiments, Panels, MMM, and Attribution}
\label{fig:ecosystem}
\end{figure}
```

## Candidates for PlantUML Conversion

Other figures that would benefit from PlantUML:

| Current File | Description | Priority |
|--------------|-------------|----------|
| `timeline.png` | Methodological evolution | High |
| `fig_method_decision_tree.png` | Method selection guide | High |
| `fig_data_lineage.png` | Data pipeline | Medium |
| `fig_exposure_construction.png` | Exposure mapping | Medium |

## Troubleshooting

**"Java not found"**
```bash
# Install Java Runtime
sudo apt-get install default-jre  # Linux
brew install openjdk              # macOS
```

**"Font not found"**
```bash
# Install DejaVu fonts
sudo apt-get install fonts-dejavu  # Linux
```

**Diagram too large/small**
```
' Add at top of .puml file
scale 0.8   ' Shrink to 80%
scale 1.5   ' Enlarge to 150%
```
