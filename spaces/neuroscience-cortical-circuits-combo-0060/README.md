# COMBO_0060 - Neuroscience Cortical Circuits

## Scientific Question
How do cortical circuit motifs transform and propagate activity?

## Biological Context
Neuronal dynamics, network signaling, and emergent circuit behavior.

## Mechanistic Assumptions
- Model implementations are used as published in their curated manifests without biological reinterpretation.
- Time integration uses a shared global tick compatible with model min_dt constraints.
- Comparative (non-causal) mode is used because full deterministic IO coverage for causal coupling was not satisfied.

## Why These Models Belong Together
The combination was selected from a shared domain/theme bucket with deterministic compatibility checks.
- `neuroscience-other-124043-124043-model`: Neuroscience: Model124043124043Model
- `neuroscience-other-135787-135787-model`: Neuroscience: Model135787135787Model
- `neuroscience-other-135898-135898-model`: Neuroscience: Model135898135898Model
- `neuroscience-other-136095-136095-model`: Neuroscience: Model136095136095Model

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
- neuroscience-other-124043-124043-model :: opensourcebrain:124043 :: https://github.com/OpenSourceBrain/124043
- neuroscience-other-135787-135787-model :: opensourcebrain:135787 :: https://github.com/OpenSourceBrain/135787
- neuroscience-other-135898-135898-model :: opensourcebrain:135898 :: https://github.com/OpenSourceBrain/135898
- neuroscience-other-136095-136095-model :: opensourcebrain:136095 :: https://github.com/OpenSourceBrain/136095

## How to Run
```bash
python run_local.py --duration auto --tick-dt auto
```

## How to Interpret Outputs
Use output trajectories and summary metrics to compare mechanistic consistency across constituent models.
Interpret comparative spaces as non-causal side-by-side simulation views.
