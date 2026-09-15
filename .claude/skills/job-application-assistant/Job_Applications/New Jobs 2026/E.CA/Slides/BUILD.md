# Building the Slides

This document contains the commands needed to compile the LaTeX slides with bibliography.

## Compilation Sequence

When using **biblatex** with **biber**, you need to run the following sequence of commands:

### 1. Initial LaTeX compilation
```bash
pdflatex slides.tex
```
This generates the auxiliary files including `slides.bcf` (bibliography control file).

### 2. Process bibliography
```bash
biber slides
```
This reads `ref.bib` and generates `slides.bbl` with formatted bibliography entries.

### 3. Second LaTeX compilation
```bash
pdflatex slides.tex
```
This incorporates the bibliography and citations into the document.

### 4. Final LaTeX compilation
```bash
pdflatex slides.tex
```
This resolves all cross-references and ensures everything is properly formatted.

## Quick Reference

Complete build sequence:
```bash
pdflatex slides.tex
biber slides
pdflatex slides.tex
pdflatex slides.tex
```

## Notes

- If you modify the bibliography file (`ref.bib`), you need to re-run the full sequence starting from step 2.
- If you only modify slide content without changing citations, running `pdflatex slides.tex` once is sufficient.
- The final output is `slides.pdf`.
