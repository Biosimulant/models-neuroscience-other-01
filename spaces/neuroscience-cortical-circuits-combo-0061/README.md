# COMBO_0061 - Neuroscience Cortical Circuits

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
- `neuroscience-other-2-distinct-classes-of-l2-and-l3-pyramidal-neuron-236429-model`: Neuroscience: Model2DistinctClassesOfL2AndL3PyramidalNeuron236429Model
- `neuroscience-other-20014-20014-model`: Neuroscience: Model2001420014Model
- `neuroscience-other-20756-20756-model`: Neuroscience: Model2075620756Model
- `neuroscience-other-21984-21984-model`: Neuroscience: Model2198421984Model

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
- neuroscience-other-2-distinct-classes-of-l2-and-l3-pyramidal-neuron-236429-model :: modeldb:236429 :: https://modeldb.science/236429
- neuroscience-other-20014-20014-model :: opensourcebrain:20014 :: https://github.com/OpenSourceBrain/20014
- neuroscience-other-20756-20756-model :: opensourcebrain:20756 :: https://github.com/OpenSourceBrain/20756
- neuroscience-other-21984-21984-model :: opensourcebrain:21984 :: https://github.com/OpenSourceBrain/21984

## How to Run
```bash
python run_local.py --duration auto --tick-dt auto
```

## How to Interpret Outputs
Use output trajectories and summary metrics to compare mechanistic consistency across constituent models.
Interpret comparative spaces as non-causal side-by-side simulation views.
