---
title: /api/v1/carrier-ico/import/
excerpt: |2

      • IDNET internal purpose of importing LIFE, HEALTH, PROPERTY & CASUALTY, and GPAL spreadsheets
      • GPAL creates carriers and markets; all carriers have a unique group code
      • PROPERTY & CASUALTY, LIFE, HEALTH files create ICOs that work under the carrier
      • Address information and Carriers (Markets).
      • First, GPAL should be imported because other spreadsheets ICOs depend on the carriers
          with unique group codes.
      • File formats are different for GPAL and LIFE, HEALTH, PROPERTY & CASUALTY,
          but in case the UUID column is added to the end of the row,
          Market uuids will be updated accordingly
      • Request params:
          - type:
              choices (Property & Casualty, HEALTH, LIFE, GPAL)
          - ico_file:
              csv(utf-8) or csv(cp1252)
          - dry_run:
              set to true for a preview of records that will be created/updated/deleted
              without actually performing the operations
      • Authentication, user must have special auth to import.
api:
  file: Identification Network (api).yaml
  operationId: carrier_ico_import_create
hidden: false
---