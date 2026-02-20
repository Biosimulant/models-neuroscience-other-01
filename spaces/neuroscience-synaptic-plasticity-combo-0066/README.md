# COMBO_0066 - Neuroscience Synaptic Plasticity

## Scientific Question
How do synaptic changes influence network-level outcomes?

## Biological Context
Neuronal dynamics, network signaling, and emergent circuit behavior.

## Mechanistic Assumptions
- Model implementations are used as published in their curated manifests without biological reinterpretation.
- Time integration uses a shared global tick compatible with model min_dt constraints.
- Comparative (non-causal) mode is used because full deterministic IO coverage for causal coupling was not satisfied.

## Why These Models Belong Together
The combination was selected from a shared domain/theme bucket with deterministic compatibility checks.
- `neuroscience-other-108459-108459-model`: Neuroscience: Model108459108459Model
- `neuroscience-other-113426-113426-model`: Neuroscience: Model113426113426Model
- `neuroscience-other-113649-113649-model`: Neuroscience: Model113649113649Model
- `neuroscience-other-113949-113949-model`: Neuroscience: Model113949113949Model

## Wiring Rationale
- Comparative (non-causal) mode: no direct causal links were created.

## Visualization Strategy
- Monitor-driven visualization is required for this space.
- State streams are routed into explicit monitor ports (`state_a..state_d`) to avoid signal overwrite.
- At minimum, monitor visuals include one timeseries panel and one summary table.
- Rationale: A dedicated monitor model receives all participating model state streams (`state_a..state_d`) so trajectories can be compared in one place without claiming causal coupling when IO semantics are incomplete.

## Expected Behaviors
- Model output trajectories under shared runtime settings.
- Cross-model agreement/divergence in key state or metric signals.
- Relative behavior comparison without causal linkage claims.

## Known Limitations
- No new biology is introduced beyond what upstream models encode.
- Cross-model semantic matching is rule-based and may under-connect uncertain routes.

## Source Provenance
- neuroscience-other-108459-108459-model :: opensourcebrain:108459 :: https://github.com/OpenSourceBrain/108459
- neuroscience-other-113426-113426-model :: opensourcebrain:113426 :: https://github.com/OpenSourceBrain/113426
- neuroscience-other-113649-113649-model :: opensourcebrain:113649 :: https://github.com/OpenSourceBrain/113649
- neuroscience-other-113949-113949-model :: opensourcebrain:113949 :: https://github.com/OpenSourceBrain/113949

## How to Run
```bash
python run_local.py --duration auto --tick-dt auto
```

## How to Interpret Outputs
Use output trajectories and summary metrics to compare mechanistic consistency across constituent models.
Interpret comparative spaces as non-causal side-by-side simulation views.
