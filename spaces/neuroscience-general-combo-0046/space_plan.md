# Space Plan - neuroscience-general-combo-0046

## Scientific Scope
- Domain: neuroscience
- Theme: general
- Base models: neuroscience-other-114654-114654-model, neuroscience-other-114655-114655-model, neuroscience-other-114665-114665-model

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
