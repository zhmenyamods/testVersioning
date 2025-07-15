---
title: /api/v1/addresses/import/
excerpt: |2-

      Imports addresses from csv file
      - creates new addresses
      - skips if addresses already exist with the same address_1, city, state, zip code, and address_type

      - User must have specific permission to import addresses.
      - Expected CSV headers: address_1, address_2, city, state, zip_code, phone_1, phone_2,
      address_type, carrier_id, ico_id, broker_id
      - Values are required for headers: address_1, address_type
      
api:
  file: Identification Network (api).yaml
  operationId: addresses_import_create
hidden: false
---