---
title: /api/v1/registered-company-codes/bulk-update/
excerpt: |2

      Update multiple existing contract codes, matching based on UUID
      - Required fields: uuid
      - Supported fields for update: active (boolean), market (UUID), icos (list of UUIDs)
      - creates MarketConfiguration records for the specified market and user's tenant if they don't exist

      - User must have specific permission to update a contract code and registered company code.
api:
  file: Identification Network (api).yaml
  operationId: registered_company_codes_bulk_update_partial_update
hidden: false
---