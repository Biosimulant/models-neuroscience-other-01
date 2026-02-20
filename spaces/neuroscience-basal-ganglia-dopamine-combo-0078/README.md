# COMBO_0078 - Neuroscience Basal Ganglia Dopamine

## Scientific Question
How do basal ganglia dopamine mechanisms compare across these models?

## Biological Context
Neuronal dynamics, network signaling, and emergent circuit behavior.

## Mechanistic Assumptions
- Model implementations are used as published in their curated manifests without biological reinterpretation.
- Time integration uses a shared global tick compatible with model min_dt constraints.
- Comparative (non-causal) mode is used because full deterministic IO coverage for causal coupling was not satisfied.

## Why These Models Belong Together
The combination was selected from a shared domain/theme bucket with deterministic compatibility checks.
- `neuroscience-other-112359-112359-model`: Neuroscience: Model112359112359Model
- `neuroscience-other-112968-112968-model`: Neuroscience: Model112968112968Model
- `neuroscience-other-114639-114639-model`: Neuroscience: Model114639114639Model
- `neuroscience-other-116867-116867-model`: Neuroscience: Model116867116867Model

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
- neuroscience-other-112359-112359-model :: opensourcebrain:112359 :: https://github.com/OpenSourceBrain/112359
- neuroscience-other-112968-112968-model :: opensourcebrain:112968 :: https://github.com/OpenSourceBrain/112968
- neuroscience-other-114639-114639-model :: opensourcebrain:114639 :: https://github.com/OpenSourceBrain/114639
- neuroscience-other-116867-116867-model :: opensourcebrain:116867 :: https://github.com/OpenSourceBrain/116867

## How to Run
```bash
python run_local.py --duration auto --tick-dt auto
```

## How to Interpret Outputs
Use output trajectories and summary metrics to compare mechanistic consistency across constituent models.
Interpret comparative spaces as non-causal side-by-side simulation views.
