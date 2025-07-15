---
title: /api/v1/enhanced-appetite-capture/
excerpt: |2

      Returns enhanced appetite result, form, and routes.

      Third endpoint in IDP appetite flow.

      Enhanced appetite result has status for each requested combination of markets, lobs, and states.

      Form contains:
      - basic appetite fields
      - enhanced appetite fields for risk profiles in basic appetite
      - risk information fields for risk profiles in enhanced appetite
      - available risk profiles: list of risk profiles that passed basic and enhanced appetite,
      and that have the highest priority route for their respective product

      Routes contains best available route type for each requested combination of market and lob.
api:
  file: Identification Network (api).yaml
  operationId: enhanced_appetite_capture_create
hidden: false
---