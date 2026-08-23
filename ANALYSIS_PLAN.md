# Analysis Plan

## Status

Preliminary. Keep the first implementation minimal.

## Unit of analysis

0.05° grid cell.

## Temporal window

Working choice: 2000–2020.

## Exposure

Cropland fraction change:

`ΔCF = CF_2020 - CF_2000`

Initial working classes:

- cropland gain;
- cropland loss;
- stable/control.

Thresholds are not yet fixed.

## Candidate land-cover data

1. GLC_FCS30D, 30 m — proposed main product.
2. GLCLU, 30 m — proposed independent robustness product.

Do not merge the two products before analysis.

## Outcome

Ecosystem resilience derived from vegetation time series using a TAC-based framework. Exact preprocessing remains to be fixed.

## Main design

1. Aggregate high-resolution cropland classes to cropland fraction at 0.05°.
2. Identify gain, loss, and stable cells.
3. Estimate resilience change relative to nearby stable controls.
4. Estimate gain and loss sensitivities separately.
5. Compare symmetric cropland transitions, for example 20%→40% versus 40%→20%.

## First milestone

Produce and validate:

- `CF_2000`;
- `CF_2020`;
- `ΔCF`;
- gain/loss/stable masks;
- basic maps and summary statistics.

Do not implement the full resilience pipeline until this milestone is checked.

## Later robustness

- alternative land-cover product;
- alternative gain/loss thresholds;
- alternative spatial matching windows;
- conversion-source/destination classes;
- alternative resilience indicators.
