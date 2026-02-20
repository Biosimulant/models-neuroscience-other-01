# COMBO_0073 - Neuroscience General

## Scientific Question
How do general mechanisms compare across these models?

## Biological Context
Neuronal dynamics, network signaling, and emergent circuit behavior.

## Mechanistic Assumptions
- Model implementations are used as published in their curated manifests without biological reinterpretation.
- Time integration uses a shared global tick compatible with model min_dt constraints.
- Comparative (non-causal) mode is used because full deterministic IO coverage for causal coupling was not satisfied.

## Why These Models Belong Together
The combination was selected from a shared domain/theme bucket with deterministic compatibility checks.
- `neuroscience-other-117810-117810-model`: Neuroscience: Model117810117810Model
- `neuroscience-other-117966-117966-model`: Neuroscience: Model117966117966Model
- `neuroscience-other-118020-118020-model`: Neuroscience: Model118020118020Model
- `neuroscience-other-118092-118092-model`: Neuroscience: Model118092118092Model

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
- neuroscience-other-117810-117810-model :: opensourcebrain:117810 :: https://github.com/OpenSourceBrain/117810
- neuroscience-other-117966-117966-model :: opensourcebrain:117966 :: https://github.com/OpenSourceBrain/117966
- neuroscience-other-118020-118020-model :: opensourcebrain:118020 :: https://github.com/OpenSourceBrain/118020
- neuroscience-other-118092-118092-model :: opensourcebrain:118092 :: https://github.com/OpenSourceBrain/118092

## How to Run
```bash
python run_local.py --duration auto --tick-dt auto
```

## How to Interpret Outputs
Use output trajectories and summary metrics to compare mechanistic consistency across constituent models.
Interpret comparative spaces as non-causal side-by-side simulation views.
