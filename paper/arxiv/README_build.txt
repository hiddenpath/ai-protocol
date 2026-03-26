Build target: arXiv-friendly pdfLaTeX project

Recommended build sequence:

1. pdflatex main.tex
2. bibtex main
3. pdflatex main.tex
4. pdflatex main.tex

Notes:

- This project avoids shell-escape and minted.
- Final figures should be committed as PDF under figures/.
- Replace placeholder figure boxes in the section files with final PDF figures before packaging.
- For arXiv submission, include all .tex files, bibliography sources, generated .bbl if needed, and all referenced figure files.
