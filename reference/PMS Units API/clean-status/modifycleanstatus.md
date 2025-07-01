---
title: Modify Clean Status
excerpt: >-
  Submit a new PUT request to change the clean status of the unit.


  After updating the clean status of a unit, the action will be logged to the
  housekeeping audit log. This log can be viewed on TRACK at
  {{environment_endpoint}}/reports/housekeeping-audit-log/ (NOTE: not an API
  endpoint.)


  This endpoint for modifying the clean status is the same for POST, PUT and
  PATCH methods.


  REQUIRES SERVER KEYS.
api:
  file: pms-units-api.json
  operationId: modifyCleanStatus
hidden: false
---