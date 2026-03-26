# Normalization Decisions

## Primary Terminology

### Layer naming

- Use **Agent Intelligence Layer** as the formal layer name.
- Use **Policy Orchestration Layer** as the formal name for the middle layer.
- Use **Execution Layer** as the formal logical layer name.
- Use **Execution Runtime** when referring to the runtime implementation of the execution layer.

### Deprecated or restricted terms

- Avoid `Contact Layer` in the paper body and figures.
- Avoid `Orchest.` except as a space-constrained figure label if absolutely necessary.
- Avoid switching between `AI Native` and `AI-Native`; use **AI-Native** consistently.

## Symbol Decisions

### System model

- Keep the logical model as `S = (A, P, E)`.
  - `A`: Agent Intelligence Layer
  - `P`: Policy Orchestration Layer
  - `E`: Execution Layer

### Capability tuple

- Change the pricing symbol from `P` to `\Pi` to avoid collision with orchestration `P`.
- Use `C = (I, O, \Sigma, Q, \Pi)`.
  - `I`: input schema
  - `O`: output schema
  - `\Sigma`: execution semantics
  - `Q`: quality telemetry schema
  - `\Pi`: pricing and billing schema

## Figure Labeling Rules

- Architecture figures may shorten labels, but only when semantics remain intact.
- Preferred short labels:
  - `Agent Layer`
  - `Orchestration Layer`
  - `Execution Runtime`
  - `Provider API`
- When a figure needs full names, use explicit line breaks rather than truncation.

## Citation and Formatting Rules

- Replace inline numeric references such as `[1]` with `\cite{...}`.
- Convert core formal definitions into equation environments.
- Convert Markdown tables into `booktabs` tables.
- Convert examples into `listings` environments rather than raw verbatim blocks.
