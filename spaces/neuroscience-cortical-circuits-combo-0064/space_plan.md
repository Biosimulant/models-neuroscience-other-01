# Space Plan - neuroscience-cortical-circuits-combo-0064

## Scientific Scope
- Domain: neuroscience
- Theme: cortical_circuits
- Base models: neuroscience-other-29942-29942-model, neuroscience-other-2d-model-of-olfactory-bulb-gamma-oscillations-li-232097-model, neuroscience-other-2d-olfactory-bulb-gamma-oscillations-osb232097-model, neuroscience-other-3264-3264-model

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
