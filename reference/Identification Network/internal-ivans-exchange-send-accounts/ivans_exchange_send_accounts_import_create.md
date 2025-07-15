---
title: /api/v1/ivans-exchange-send-accounts/import/
excerpt: >

  Imports Ivans Exchange send accounts from the given format and import file.

  Upserts records based on account_id.

  - User must have specific permission to import send accounts.

  - Expected CSV headers: account_id, carrier_id, account_id_alternate,
  broker_id
api:
  file: Identification Network (api).yaml
  operationId: ivans_exchange_send_accounts_import_create
hidden: false
---