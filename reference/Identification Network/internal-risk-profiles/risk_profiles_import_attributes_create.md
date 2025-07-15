---
title: /api/v1/risk-profiles/{uuid}/import-attributes/
excerpt: |2

      Imports CSV file to create new attributes and RPAs for a given risk profile.

      Internal IDNET endpoint.

      Expected CSV headers: name | data_type | ivans_id | form_group | ido_mapping

      Authentication: user requires special permission to import.
api:
  file: Identification Network (api).yaml
  operationId: risk_profiles_import_attributes_create
hidden: false
---