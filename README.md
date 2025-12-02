# Causal Inference in Marketing: Panel Data and Machine Learning

[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/)
[![GitHub stars](https://img.shields.io/github/stars/shawcharles/Causal-Inference-in-Marketing?style=social)](https://github.com/shawcharles/Causal-Inference-in-Marketing/stargazers)
[![GitHub issues](https://img.shields.io/github/issues/shawcharles/Causal-Inference-in-Marketing)](https://github.com/shawcharles/Causal-Inference-in-Marketing/issues)
[![GitHub last commit](https://img.shields.io/github/last-commit/shawcharles/Causal-Inference-in-Marketing)](https://github.com/shawcharles/Causal-Inference-in-Marketing/commits/main)

**Author:** Charles Shaw  
**Website:** [shawcharles.github.io/Causal-Inference-in-Marketing](https://shawcharles.github.io/Causal-Inference-in-Marketing/)

---

## 🚧 Community Review Edition 🚧

**This is a working draft manuscript** shared for community review, feedback, and error correction.

- The core methods and theory are stable; some sections may have minor typos or incomplete references.
- **Issues and Pull Requests are welcome!** If you spot a typo, mathematical error, or unclear passage, please [open an issue](https://github.com/shawcharles/Causal-Inference-in-Marketing/issues) or submit a fix.
- Please do not distribute built PDF copies without permission.

📄 **[Download the PDF](book.pdf)** · 🌐 **[View the Website](https://shawcharles.github.io/Causal-Inference-in-Marketing/)**

---

## About the Book

This monograph bridges the gap between design-based causal inference (Difference-in-Differences, Synthetic Control) and modern machine learning methods for marketing applications. It focuses specifically on **panel data** structures common in marketing (customer-week, store-day, DMA-month).

### Key Topics

| Area | Methods |
|------|---------|
| **Design-Based Core** | DiD, Event Studies, Synthetic Control |
| **Modern Extensions** | Staggered adoption (Callaway–Sant'Anna, Sun–Abraham), Augmented SC, Synthetic DiD |
| **Matrix & Factor Methods** | Interactive Fixed Effects, Matrix Completion, Tensor Completion |
| **Machine Learning** | Double Machine Learning (DML), CATE estimation, Causal Forests, High-dimensional controls |
| **Marketing Applications** | Advertising effectiveness, pricing, loyalty programmes, platform interference, privacy-preserving measurement |

## How to Build

This project is built using standard LaTeX tools.

### Requirements
*   TeX Live (or equivalent LaTeX distribution)
*   `pdflatex`
*   `makeindex`

### Build Commands
To build the full book with index and bibliography:

```bash
pdflatex book.tex
makeindex book.idx
pdflatex book.tex
pdflatex book.tex
```

## Contributing

We welcome contributions from the community:

- **Typos and errors**: [Open an issue](https://github.com/shawcharles/Causal-Inference-in-Marketing/issues) or submit a pull request.
- **Methodological questions**: Start a [discussion](https://github.com/shawcharles/Causal-Inference-in-Marketing/discussions).
- **Suggestions**: We appreciate feedback on clarity, missing topics, or additional applications.

Please see the website's [About page](https://shawcharles.github.io/Causal-Inference-in-Marketing/about/) for more details.

## Citation

If you use this book in your research or teaching, please cite it:

```bibtex
@book{shaw2025causal,
  author    = {Shaw, Charles},
  title     = {Causal Inference in Marketing: Panel Data and Machine Learning},
  year      = {2025},
  publisher = {Self-published (Community Review Edition)},
  url       = {https://github.com/shawcharles/Causal-Inference-in-Marketing}
}
```

See the [Citation page](https://shawcharles.github.io/Causal-Inference-in-Marketing/citation/) for additional formats (APA, Chicago).

## License

This work is licensed under a **Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License (CC BY-NC-SA 4.0)**.

- **You are free to:** Share and adapt the material for non-commercial purposes.
- **You must:** Give appropriate credit and distribute your contributions under the same license.
- **You may not:** Use this material for commercial purposes without permission.

See the `LICENSE` file for full details.
