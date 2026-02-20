# COMBO_0072 - Neuroscience Synaptic Plasticity

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
- `neuroscience-other-19591-19591-model`: Neuroscience: Model1959119591Model
- `neuroscience-other-19747-19747-model`: Neuroscience: Model1974719747Model
- `neuroscience-other-34168-34168-model`: Neuroscience: Model3416834168Model
- `neuroscience-other-35781-35781-model`: Neuroscience: Model3578135781Model

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
- neuroscience-other-19591-19591-model :: opensourcebrain:19591 :: https://github.com/OpenSourceBrain/19591
- neuroscience-other-19747-19747-model :: opensourcebrain:19747 :: https://github.com/OpenSourceBrain/19747
- neuroscience-other-34168-34168-model :: opensourcebrain:34168 :: https://github.com/OpenSourceBrain/34168
- neuroscience-other-35781-35781-model :: opensourcebrain:35781 :: https://github.com/OpenSourceBrain/35781

## How to Run
```bash
python run_local.py --duration auto --tick-dt auto
```

## How to Interpret Outputs
Use output trajectories and summary metrics to compare mechanistic consistency across constituent models.
Interpret comparative spaces as non-causal side-by-side simulation views.
