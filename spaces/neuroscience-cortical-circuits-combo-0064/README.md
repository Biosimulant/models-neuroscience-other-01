# COMBO_0064 - Neuroscience Cortical Circuits

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
- `neuroscience-other-29942-29942-model`: Neuroscience: Model2994229942Model
- `neuroscience-other-2d-model-of-olfactory-bulb-gamma-oscillations-li-232097-model`: Neuroscience: Model2dModelOfOlfactoryBulbGammaOscillationsLi232097Model
- `neuroscience-other-2d-olfactory-bulb-gamma-oscillations-osb232097-model`: Neuroscience: Model232097232097Model
- `neuroscience-other-3264-3264-model`: Neuroscience: Model32643264Model

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
- neuroscience-other-29942-29942-model :: opensourcebrain:29942 :: https://github.com/OpenSourceBrain/29942
- neuroscience-other-2d-model-of-olfactory-bulb-gamma-oscillations-li-232097-model :: modeldb:232097 :: https://modeldb.science/232097
- neuroscience-other-2d-olfactory-bulb-gamma-oscillations-osb232097-model :: opensourcebrain:232097 :: https://github.com/OpenSourceBrain/232097
- neuroscience-other-3264-3264-model :: opensourcebrain:3264 :: https://github.com/OpenSourceBrain/3264

## How to Run
```bash
python run_local.py --duration auto --tick-dt auto
```

## How to Interpret Outputs
Use output trajectories and summary metrics to compare mechanistic consistency across constituent models.
Interpret comparative spaces as non-causal side-by-side simulation views.
