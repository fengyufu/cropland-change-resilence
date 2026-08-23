# Cropland Change & Ecosystem Resilience

A lightweight research repository for studying whether cropland gain and cropland loss have asymmetric effects on ecosystem resilience.

The workflow is adapted from `geo-research-os`, but intentionally starts small: keep the research question, analysis plan, decisions, and project state explicit before building a large codebase.

## Current idea

- Exposure: cropland fraction change, initially 2000–2020.
- Main land-cover candidate: GLC_FCS30D (30 m).
- Robustness land-cover candidate: GLCLU (30 m), analysed independently rather than merged.
- Analysis grid: initially 0.05°.
- Outcome: ecosystem resilience derived from vegetation time series (TAC framework).
- Main comparison: cropland gain vs loss, including symmetric transitions such as 20%→40% vs 40%→20%.

These choices are provisional until documented in `DECISIONS.md`.

## Start here

Read in this order:

1. `START_HERE.md`
2. `PROJECT_STATE.json`
3. `QUESTION.md`
4. `ANALYSIS_PLAN.md`
5. `DECISIONS.md`
6. `WORKLOG.md`

## Repository rule

Do not commit raw remote-sensing data. Keep raw and generated data outside Git; record data sources and processing steps instead.

## Immediate next task

Confirm the cropland data products and build the first 2000/2020 cropland-fraction preprocessing workflow before implementing the resilience analysis.
