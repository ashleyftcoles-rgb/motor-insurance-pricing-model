# Motor Insurance Pricing & Risk Simulation

An Excel project exploring motor insurance pricing and portfolio risk using synthetic policy and claims data.

The workbook combines a frequency–severity pricing model, an individual quotation tool, a component-based claims calculator and Monte Carlo simulation.

## Project objectives

- Generate a synthetic motor insurance portfolio.
- Explore how driver and vehicle characteristics affect insurance prices.
- Calculate expected claim costs and premiums.
- Analyse portfolio performance and simulated underwriting profit.

## Workbook features

| Feature | Purpose |
|---|---|
| Assumptions | Defines portfolio characteristics, risk factors and pricing loadings |
| Policy and claims data | Provides synthetic records for modelling and analysis |
| Pricing engine | Calculates policy-level expected claim costs and premiums |
| Quote Generator | Produces an illustrative quote from user inputs |
| Claims Calculator | Estimates claim components under selected assumptions |
| Monte Carlo Simulation | Generates scenarios for aggregate claims and underwriting profit |
| Dashboard | Summarises portfolio, pricing and simulation results |

## Methodology

### Pricing

Expected claim cost is calculated as:

**Expected claim frequency × Expected claim severity**

Assumed risk factors adjust frequency and severity for characteristics such as driver age, no-claims bonus and vehicle group.

Premiums incorporate expense, commission and target profit loadings. Insurance Premium Tax is added separately to calculate the customer premium.

### Claims modelling

Claim costs are separated into own-vehicle repair, injury and third-party damage components. Their values depend on the selected claim characteristics and modelling assumptions.

### Monte Carlo simulation

The simulation uses binomial claim counts and a lognormal approximation to average claim severity, conditional on the claim count.

Simulated underwriting profit deducts claims, expenses and commission from premium income excluding Insurance Premium Tax.

## How to use

1. Download `motor_insurance_pricing_model.xlsx`.
2. Open it in a recent desktop version of Microsoft Excel supporting `XLOOKUP`, `FILTER` and `LET`.
3. Read the workbook’s README and review the Assumptions sheet.
4. Explore the Quote Generator and Claims Calculator.
5. Review the Dashboard and Monte Carlo results.

**Recalculation changes random values.** The workbook uses Excel random-number functions, so recalculation can regenerate synthetic data and simulation results. PivotTables may require a separate refresh.

## Assumptions and limitations

- All policy and claims data are synthetic.
- Risk factors are illustrative assumptions rather than estimates fitted to real insurance experience.
- The claims-generation model allows at most one claim per policy.
- Vehicle groups are limited to those represented in the workbook.
- The simulation simplifies policy differences and assumes independent claim amounts.
- Common shocks, catastrophe dependence and uncertainty in model parameters are not explicitly modelled.
- Simulation results depend on the selected assumptions and generated dataset.
- Zero observed losses in a simulation does not imply that losses are impossible.

This project is an educational demonstration of insurance modelling in Excel, not a production pricing tool or an insurance quotation service.

## Skills demonstrated

- Excel formulas and structured table references
- Lookup functions and data validation
- Frequency–severity pricing
- Component-based claims modelling
- Monte Carlo simulation
- PivotTables, charts and portfolio reporting

## Future improvements

- Reproducible data generation and fixed demonstration inputs
- Additional reconciliation and validation checks
- Policy-level simulation and sensitivity analysis
- Calibration against an appropriately licensed external dataset
