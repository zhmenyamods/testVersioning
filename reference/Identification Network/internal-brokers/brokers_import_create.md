---
title: /api/v1/brokers/import/
excerpt: |2-

      Imports brokers from csv file
      - creates new brokers
      - creates new markets for the new brokers
      - skips existing brokers with the same key

      - User must have specific permission to import brokers.
      - Expected CSV headers: name
      
api:
  file: Identification Network (api).yaml
  operationId: brokers_import_create
hidden: false
---