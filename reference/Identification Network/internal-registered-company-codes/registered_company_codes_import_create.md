---
title: /api/v1/registered-company-codes/import/
excerpt: |2-

      Imports market contract codes from csv file
      - creates new contract codes
      - skips existing codes
      - creates MarketConfigurations, MarketContractCodeICOs, and MarketContractSegments

      - User must have specific permission to import contract codes.
      - Expected CSV headers: carrier_id, broker_id, nickname, code, y_account_id, segments,
      icos, location, active, new_business, binding_authority, service_center, notes,
      last_modified_by_external_id
      - batchSize parameter in request body can be used to customize how many records are created per batch.
      
api:
  file: Identification Network (api).yaml
  operationId: registered_company_codes_import_create
hidden: false
---