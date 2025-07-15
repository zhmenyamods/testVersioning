---
title: /api/v1/basic-appetite/import/
excerpt: |2-

      Imports from csv to create basic appetite condition sets and conditions for a risk profile.

      Internal IDNET endpoint.

      Spreadsheet requires the following headers:
      State(s) | NAICS Code(s) | NAICS Index Description | NAICS AK Hash

      Authentication: user must have special permission to import.
      
api:
  file: Identification Network (api).yaml
  operationId: basic_appetite_import_create
hidden: false
---