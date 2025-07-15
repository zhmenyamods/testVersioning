---
title: /api/v1/basic-appetite/
excerpt: |2

      Returns basic appetite result and optional form.

      Basic appetite result contains status for each combination of the requested markets, lobs, and states.
      - If no markets are requested, appetite status is returned for all allowed markets.
      - If no states are requested, appetite status is returned for all US states.

      Optional form contains:
      - basic appetite fields
      - enhanced appetite fields for risk profiles in appetite
      - list of risk profiles that passed basic appetite
api:
  file: Identification Network (api).yaml
  operationId: basic_appetite_create
hidden: false
---