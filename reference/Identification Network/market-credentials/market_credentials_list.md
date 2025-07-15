---
title: /api/v1/market-credentials/
excerpt: >

  Returns all of the market credentials that user has access to.

  - If a user is an admin, all credentials with the market configuration will be
  available to view.

  - If the user is not an admin, the access structure will be filtered based on
  the user's permission.
api:
  file: Identification Network (api).yaml
  operationId: market_credentials_list
hidden: false
---