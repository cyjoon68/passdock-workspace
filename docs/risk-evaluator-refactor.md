# Risk Evaluator Refactor

## Before

`RiskService.ingest` used one hard-coded if-chain for changed-device failures.

## After

`RiskService.ingest` checks enabled `RiskRule` entries through a rule-name strategy map.

## Why

Adding a rule now adds one evaluator entry instead of extending one growing branch.
