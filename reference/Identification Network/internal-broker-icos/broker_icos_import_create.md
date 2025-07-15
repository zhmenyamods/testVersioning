---
title: /api/v1/broker-icos/import/
excerpt: |2-

      Imports broker ICOs from csv file
      - skips existing broker ICOs with the same key

      - User must have specific permission to import broker ICOs.
      - Expected CSV headers: broker_name, ico_naic_code, download_indicator
      
api:
  file: Identification Network (api).yaml
  operationId: broker_icos_import_create
hidden: false
---