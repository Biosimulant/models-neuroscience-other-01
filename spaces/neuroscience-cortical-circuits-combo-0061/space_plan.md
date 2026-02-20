# Space Plan - neuroscience-cortical-circuits-combo-0061

## Scientific Scope
- Domain: neuroscience
- Theme: cortical_circuits
- Base models: neuroscience-other-2-distinct-classes-of-l2-and-l3-pyramidal-neuron-236429-model, neuroscience-other-20014-20014-model, neuroscience-other-20756-20756-model, neuroscience-other-21984-21984-model

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
