---
title: /api/v1/basic-appetite-capture/
excerpt: |2

      Returns basic appetite result, form, and possible routes.

      Second endpoint of the IDP appetite flow.

      Basic appetite result has status for each requested combination of markets, lobs, and states.

      Form contains:
      - basic appetite fields
      - enhanced appetite fields for risk profiles in appetite
      - available risk profiles: list of risk profiles that passed basic appetite

      Possible routes contains possible route types for each requested combination of market and lob.
api:
  file: Identification Network (api).yaml
  operationId: basic_appetite_capture_create
hidden: false
---