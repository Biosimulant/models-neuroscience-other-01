# COMBO_0059 - Neuroscience Cortical Circuits

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
- `neuroscience-other-116871-116871-model`: Neuroscience: Model116871116871Model
- `neuroscience-other-118759-118759-model`: Neuroscience: Model118759118759Model
- `neuroscience-other-123623-123623-model`: Neuroscience: Model123623123623Model
- `neuroscience-other-123897-123897-model`: Neuroscience: Model123897123897Model

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
- neuroscience-other-116871-116871-model :: opensourcebrain:116871 :: https://github.com/OpenSourceBrain/116871
- neuroscience-other-118759-118759-model :: opensourcebrain:118759 :: https://github.com/OpenSourceBrain/118759
- neuroscience-other-123623-123623-model :: opensourcebrain:123623 :: https://github.com/OpenSourceBrain/123623
- neuroscience-other-123897-123897-model :: opensourcebrain:123897 :: https://github.com/OpenSourceBrain/123897

## How to Run
```bash
python run_local.py --duration auto --tick-dt auto
```

## How to Interpret Outputs
Use output trajectories and summary metrics to compare mechanistic consistency across constituent models.
Interpret comparative spaces as non-causal side-by-side simulation views.
