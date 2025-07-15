---
title: /api/v1/forms/is-eligible/
excerpt: |2

      Returns eligibility results for the requested risk profiles, based on the provided form answers.
      Request body is comprised of form answers, and must include answers for classification (NAICS)
      and primary state fields.
      Results will only be returned for risk profiles that are allowed for the user.
api:
  file: Identification Network (api).yaml
  operationId: forms_is_eligible_create
hidden: false
---