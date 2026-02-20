# Space Plan - neuroscience-cortical-circuits-combo-0065

## Scientific Scope
- Domain: neuroscience
- Theme: cortical_circuits
- Base models: neuroscience-other-3343-3343-model, neuroscience-other-3660-3660-model, neuroscience-other-37819-37819-model, neuroscience-other-3d-model-of-the-olfactory-bulb-migliore-et-al-20-151681-model

## Wiring Plan
- Comparative mode with monitor-only routing.
- Each base model state-like output connects to monitor ports `state_a..state_d`.
- No direct causal links among base models unless explicitly upgraded later.

## Visualization Plan
- Include `StateComparisonMonitor` and `StateMetricsMonitor`.
- Require at least:
  - one timeseries visual,
  - one summary table visual.

## Validation Gates
- space schema validity
- wiring endpoint validity
- smoke run success
- repo manifest/entrypoint validators pass
