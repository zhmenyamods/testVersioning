---
title: /api/v1/forms/templates/{uuid}/
excerpt: >

  Returns individual template and its default field values.


  Permissions:

  - All users can access templates owned by Ivans.

  - Service level users can access templates that are owned by their application
  or any agency under the application.

  - Agency level admin users can access templates owned by their application or
  their own agency.

  - Agency level non-admin users can access templates that are set to available,
  and are owned by their application

  or their own agency.
api:
  file: Identification Network (api).yaml
  operationId: forms_templates_retrieve
hidden: false
---