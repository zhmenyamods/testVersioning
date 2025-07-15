---
title: /api/v1/market-contract-codes/bulk-delete/
excerpt: >

  Deletes multiple existing contract codes.


  Access restrictions:


  - If the request user is an admin, all contract codes under the user's
  database scope will be available to delete.

  - If the request user is not an admin, the user can only delete codes where
  the user is the owner of the contract code.

  - Every code must be accessible to the user for the bulk delete to complete.
api:
  file: Identification Network (api).yaml
  operationId: market_contract_codes_bulk_delete_create
hidden: false
---