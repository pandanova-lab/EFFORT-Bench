# EFFORT-Bench

**Beyond Task Completion: Measuring AI's Ability to Anticipate Human Work**

## Abstract

Large language models are increasingly used to plan, delegate and monitor professional work. Doing that well requires anticipating how much human effort a task will need, not just completing it. **EFFORT-Bench** tests whether AI systems can forecast the *future recorded person-hours* of real professional work, using only the information available at the time of the forecast. It is built from de-identified legal matter records. A cross-domain extension using public software issue-tracking data is planned. The benchmark measures five capabilities: effort-scale knowledge, task-specific discrimination, evidence integration, probabilistic forecasting and reliability awareness. Every LLM is compared with strong non-LLM baselines under a leakage-controlled protocol.

## Benchmark Overview

- **Task.** Given a snapshot of a task at a forecast origin, predict the distribution (p10 / p50 / p90) of future recorded team hours over a fixed horizon. Zero future effort is a valid outcome.
- **Domains.**
  - *Legal:* matters from an anonymized law firm ("Firm A").
  - *Software:* issues from public Jira worklogs (JOSSE), as a cross-domain extension subject to validation.
- **Information states.** Forecasts are made from progressively richer information about the same task. This separates prior knowledge of effort scale from evidence-based updating.
- **Baselines.** Commercial and open-weight LLMs (zero-shot and retrieval-augmented) alongside historical, retrieval and supervised (e.g., LightGBM) baselines.
- **Evaluation.** The primary metric is quantile (pinball) loss. Secondary metrics cover log-ratio error, rank correlation, interval coverage and calibration. Confidence intervals come from a client-clustered bootstrap.
- **Leakage control.** Chronological and client-disjoint splits. Retrieval pools contain only records from before the forecast origin.

## Directory Structure

```
EFFORT-Bench/
├── data/      # Benchmark data (coming soon)
├── code/      # Evaluation and baseline code (coming soon)
├── figures/   # Figures (coming soon)
└── README.md
```

## Dataset

🚧 **Coming soon.** Dataset availability is subject to data-use permissions and privacy review.

## Code

🚧 **Coming soon.**

## Citation

🚧 **Coming soon.**
