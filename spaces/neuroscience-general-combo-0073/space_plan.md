# Space Plan - neuroscience-general-combo-0073

## Scientific Scope
- Domain: neuroscience
- Theme: general
- Base models: neuroscience-other-117810-117810-model, neuroscience-other-117966-117966-model, neuroscience-other-118020-118020-model, neuroscience-other-118092-118092-model

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
