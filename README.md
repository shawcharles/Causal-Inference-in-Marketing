# Causal Inference in Marketing: Panel Data and Machine Learning

**Author:** Charles Shaw

## 🚧 Working Draft - Community Review Edition 🚧

**This is a working draft manuscript.** It is currently being shared for community review, feedback, and error correction. 

**Please Note:**
*   This text is a work in progress. You will find typos, incomplete references, and sections under active revision.
*   **Issues and Pull Requests are welcome!** If you spot a typo, a mathematical error, or a repetitive section, please open an issue or submit a fix.
*   Please do not distribute built PDF copies of this manuscript without permission.

---

## About the Book

This monograph bridges the gap between design-based causal inference (Difference-in-Differences, Synthetic Control) and modern machine learning methods for marketing applications. It focuses specifically on **panel data** structures common in marketing (customer-week, store-day, DMA-month).

**Key Topics:**
*   **Design-Based Core:** DiD, Event Studies, Synthetic Control.
*   **Modern Extensions:** Staggered adoption, Augmented Synthetic Control, Synthetic DiD.
*   **Matrix & Factor Methods:** Interactive Fixed Effects, Matrix Completion, Tensor Completion.
*   **Machine Learning:** Double Machine Learning (DML), CATE estimation, High-dimensional controls.
*   **Marketing Applications:** Advertising effectiveness, pricing, loyalty programs, platform interference.

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

## License

This work is licensed under a **Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License (CC BY-NC-SA 4.0)**.

*   **You are free to:** Share and Adapt the material for non-commercial purposes.
*   **You must:** Give appropriate credit and distribute your contributions under the same license.
*   **You may not:** Use this material for commercial purposes (selling copies, including in paid training material without permission).

See the `LICENSE` file for full details.
