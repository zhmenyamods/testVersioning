---
title: /api/v1/enhanced-appetite/
excerpt: |2

      Returns enhanced appetite result and optional form.

      Enhanced appetite result has status for each requested combination of markets, lobs, and states.
      - If no markets are requested, appetite status is returned for all allowed markets.
      - If no states are requested, appetite status is returned for all US states.

      Optional form contains:
      - basic appetite fields
      - enhanced appetite fields for risk profiles in basic appetite
      - risk information fields for risk profiles in enhanced appetite
      - available risk profiles: list of risk profiles that passed basic and enhanced appetite,
      and that have the highest priority route for their respective product
api:
  file: Identification Network (api).yaml
  operationId: enhanced_appetite_create
hidden: false
---