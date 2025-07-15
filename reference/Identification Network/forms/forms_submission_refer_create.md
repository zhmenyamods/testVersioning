---
title: /api/v1/forms/submission/refer/
excerpt: |2

      Endpoint to refer quotes through IDP.

      Metadata:
          - clientId: integrator's account ID, required
          - quoteId: integrator's quote ID, required
          - callbackUrl: integrator's callback URL, required

      Market metadata:
          - riskProfile: risk profile UUID, required
          - marketQuoteId: carrier's quote ID, optional and can be null
          - marketAccountId: carrier's account ID, optional and can be null
          - contractCodeId: user's market contract code UUID, optional or required, depending on user configuration
          - credentialId: user's market credential UUID, optional and can be null
          - referenceIds: carrier's quote IDs for referral, optional and can be null
api:
  file: Identification Network (api).yaml
  operationId: forms_submission_refer_create
hidden: false
---