---
title: /api/v1/forms/templates/{uuid}/
excerpt: >

  Updates the template with the given UUID.


  Permissions:

  - Non-admin users cannot update templates.

  - Service level users can update any template under their application.

  - Agency level admin users can only update templates that are owned by their
  agency.

  - Service level users can update the agency owner of the template.

  - Agency level admin users cannot update the owner of the template.


  If a field is not provided in the request body, it will not be updated.


  If availableAt is set, no updates can be made to the template after it is
  available.


  Defaults keys can be either a field GUID or parent attribute GUID. Values will
  be validated

  according to data type and options.
api:
  file: Identification Network (api).yaml
  operationId: forms_templates_partial_update
hidden: false
---