# arXiv Conversion Execution Plan

## Goal

Convert `Paper1_AI_Execution_Layer_v1.2.md` into an arXiv-friendly LaTeX resource bundle with:

- consistent terminology and notation
- vector figures in PDF format
- booktabs-style tables
- equation-based formal definitions
- listings-based code examples
- BibTeX-based references

## Constraints

- target compiler: `pdflatex`
- no shell-escape requirement
- no `minted`
- no direct SVG dependency in the final upload bundle
- final figures should be PDF where possible

## Phase 1: Source Normalization

1. Unify layer names and short labels.
2. Resolve the `P` notation conflict in `S = (A, P, E)` vs. `C = (I, O, Σ, Q, P)`.
3. Standardize `AI-Native` spelling.
4. Clarify the distinction between `Execution Layer` and `Execution Runtime`.
5. Replace `Contact Layer` references with the chosen orchestration term.

## Phase 2: Project Scaffolding

1. Create `main.tex`.
2. Split content into per-section LaTeX files under `sections/`.
3. Create `figures/`, `bibliography/`, and `notes/`.
4. Add a build note for arXiv packaging.

## Phase 3: Core LaTeX Conversion

1. Convert title, abstract, keywords, and section hierarchy.
2. Rewrite formal definitions as equations:
   - `S = (A, P, E)`
   - `C = (I, O, Σ, Q, Π)`
   - `Invoke(C, Input) -> Output`
   - `Route(C, Context) -> Provider`
   - `G = (Capabilities, Dependencies)`
3. Convert the capability comparison table into `booktabs` format.
4. Add two new tables:
   - runtime responsibilities vs. exclusions
   - logical model vs. implementation mapping

## Phase 4: Figure Redevelopment

1. Redraw the layered architecture overview.
2. Redraw the five-layer implementation stack.
3. Redraw the capability graph as a DAG figure.
4. Rebuild Appendix A sequence diagrams as PlantUML and export PDF.

## Phase 5: Listings and Appendices

1. Convert YAML, JSON, and pseudocode blocks to `listings`.
2. Keep heavy examples in appendices.
3. Keep file-tree examples as monospaced listings.

## Phase 6: References and Packaging

1. Move references into `bibliography/refs.bib`.
2. Convert inline numeric citations to `\cite{...}`.
3. Verify labels, cross-references, and figure inclusion.
4. Assemble the final arXiv upload bundle.

## Immediate Next Actions

1. Write normalization decisions into a dedicated note.
2. Create a compilable `main.tex` skeleton.
3. Start a normalized working copy of the paper content.
4. Convert front matter and Sections 1--2 first.
