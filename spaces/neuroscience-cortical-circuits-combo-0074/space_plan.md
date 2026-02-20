# Space Plan - neuroscience-cortical-circuits-combo-0074

## Scientific Scope
- Domain: neuroscience
- Theme: cortical_circuits
- Base models: neuroscience-other-3d-model-of-the-olfactory-bulb-migliore-et-al-20-151681-model, neuroscience-other-3d-olfactory-bulb-operators-migliore-et-al-2015-168591-model, neuroscience-other-3d-population-midget-retinal-ganglion-cells-at-human-fovea-osb267391-model, neuroscience-other-45539-45539-model

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
