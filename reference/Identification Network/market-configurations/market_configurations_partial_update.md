---
title: /api/v1/market-configurations/{uuid}/
excerpt: |

  Updates a market configuration.

  Only service level users can update the agency.

  Fields that can be updated:
  - lineOfBusiness: uuid
  - accessStructures: (multiple accepted)
      - agency: uuid (required)
      - branch: uuid (not required)
      - department: uuid (not required)
      - businessUnit: uuid (not required)
  - appointed: true or false
  - preferred: true or false
  - notes: text
  - agency: uuid
api:
  file: Identification Network (api).yaml
  operationId: market_configurations_partial_update
hidden: false
---