# Characterization of the Interaction Between DDX3X and Influenza B Virus Genomic RNA (LaTeX Beamer)

[![LaTeX](https://img.shields.io/badge/Format-LaTeX%20(16%3A9)-008080.svg?logo=latex&logoColor=white)](final_report_presentation.tex)
[![Compiled PDF](https://img.shields.io/badge/Output-PDF%20Document-red.svg?logo=adobe-acrobat-reader&logoColor=white)](final_report_presentation.pdf)
[![Theme](https://img.shields.io/badge/Design-Custom%20Madrid%20%2B%20Biotech-143058.svg)](#)

This repository contains the publication-grade **LaTeX** source code, compiled presentation PDF, optimized vector/raster figures, and comprehensive compilation instructions for the research internship project presented by **Aradhya Gupta** (South Asian University) under the mentorship of **Prof. Arindam Mondal** (Molecular Virology Laboratory, Department of Bioscience and Biotechnology, Indian Institute of Technology Kharagpur).

---

## Project Summary

The study investigates how the host cellular RNA helicase **DDX3X** interacts with **Influenza B virus (IBV)** genomic RNA segments:
- **Expression & IMAC / SEC Purification**: Full-length human DDX3X (~73 kDa) recombinantly expressed in *E. coli* BL21(DE3) and purified to homogeneity.
- **In Vitro Transcription**: Generation of precise mini-viral RNA segments (HA, PA, NS).
- **EMSA Gel Mobility Shift Characterization**: Direct quantitative binding analysis between recombinant DDX3X and viral segments (PB1, PB2) across titrating concentrations (0–20 µM).

The slide deck is built from scratch in modern LaTeX Beamer using custom palettes (Academic Navy, Biotech Teal, Amber Accent), vectorized TikZ node diagrams, structured scientific cards, and optimized high-resolution gel figures.

---

## Repository Structure

```text
├── final_report_presentation.tex  # Master LaTeX Beamer source document (835 lines)
├── final_report_presentation.pdf  # Fully compiled presentation PDF (16:9 widescreen)
├── .gitignore                     # Git ignore rules for LaTeX auxiliary & build files
├── README.md                      # Repository documentation and compilation guide
└── figures_opt/                   # High-resolution optimized graphics used in the slides
    ├── image2.png                 # South Asian University crest
    ├── image3.png                 # IIT Kharagpur crest
    ├── image26.png                # SDS-PAGE: DDX3X expression (Uninduced vs Induced)
    ├── image27.png                # SDS-PAGE: Ni-NTA elution fractions
    ├── image29.png                # Size Exclusion Chromatography gel
    ├── image42.png                # EMSA gel titration: PB1 segment
    ├── image43.png                # EMSA gel titration: PB2 segment
    └── ...                        # Additional structural, pathway, and gel figures
```

---

## Compilation Guide

### Recommended: TeX Live / MacTeX / MiKTeX

You can compile the presentation using `pdflatex`, `lualatex`, or `latexmk`. Because Beamer computes references, totals, and navigation across frames, run two passes:

```bash
# Using pdflatex (run twice for page numbering & cross-references):
pdflatex -interaction=nonstopmode final_report_presentation.tex
pdflatex -interaction=nonstopmode final_report_presentation.tex
```

Or using `latexmk` (automatic multi-pass build):

```bash
latexmk -pdf final_report_presentation.tex
```

### Overleaf / Cloud LaTeX Setup
1. Create a **New Project** -> **Upload Project**.
2. Upload the files: `final_report_presentation.tex` and the `figures_opt/` directory.
3. Set the compiler to **pdfLaTeX** and set `final_report_presentation.tex` as the main document.
4. Click **Recompile**.

---

## Theme & Typography Specifications

- **Aspect Ratio**: 16:9 widescreen (`\documentclass[aspectratio=169, 10pt]{beamer}`)
- **Base Theme**: `Madrid` with custom academic color configurations
- **Color Palette**:
  - `navyprimary`: `#143058` (RGB: 20, 48, 88) - Dominant structural & title tone
  - `steelsecondary`: `#2666A3` (RGB: 38, 102, 163) - Secondary accents & item markers
  - `biotechteal`: `#107C78` (RGB: 16, 124, 120) - Example blocks & highlighted callouts
  - `amberaccent`: `#C47A18` (RGB: 196, 122, 24) - Alert banners, underlines & dividers
  - `cardbg`: `#F4F7FC` (RGB: 244, 247, 252) - Clean background fill for content blocks
- **Packages Required**: `graphicx`, `tikz`, `amsmath`, `amssymb`, `booktabs`, `tabularx`, `xcolor`, `hyperref`

---

## 👥 Academic Credits & Affiliations

- **Student Author**: Aradhya Gupta (1st Year BS-MS, South Asian University, New Delhi)
- **Host Lab & PI**: Prof. Arindam Mondal, Molecular Virology Laboratory, Department of Bioscience and Biotechnology, IIT Kharagpur
- **Contributor**: Mr. Soumik Dey (Lab Member, preliminary promoter downregulation findings)
