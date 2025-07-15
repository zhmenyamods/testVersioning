---
title: /api/v1/forms/templates/
excerpt: >

  Returns list of templates and their default field values that are accessible
  to the user.


  Permissions:

  - All users can access templates owned by Ivans.

  - Service level users can access templates that are owned by their application
  or any agency under the application.

  - Agency level admin users can access templates owned by their application or
  their own agency.

  - Agency level non-admin users can access templates that are set to available,
  and are owned by their application

  or their own agency.


  Templates can be filtered with the given Lines of Business and Markets.

  If no filters are provided, all permitted templates will be returned.

  If exclude_defaults is true, default field values will not be returned for
  each template.
api:
  file: Identification Network (api).yaml
  operationId: forms_templates_list
hidden: false
---