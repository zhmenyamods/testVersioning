---
title: /api/v1/forms/templates/{uuid}/
excerpt: >

  Deletes the template with the given UUID.


  Permissions:

  - Non-admin users cannot delete templates.

  - Service level users can delete any template under their application.

  - Agency level admin users can only delete templates that are owned by the
  agency.
api:
  file: Identification Network (api).yaml
  operationId: forms_templates_destroy
hidden: false
---