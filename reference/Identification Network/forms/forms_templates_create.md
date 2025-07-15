---
title: /api/v1/forms/templates/
excerpt: >

  Creates a new template.


  Permissions:

  - Non-admin users cannot create templates.

  - By default, a template is scoped to the user's application, and is
  accessible to all agencies

  under the application.

  - Service level users can specify the agency owner of the template, which
  restricts access to users

  under that agency.

  - Agency level admin users cannot specify the owner of the template - any
  template they create will

  automatically set the agency owner to their agency.


  If availableAt is set, no updates can be made to the template after it is
  available.


  Defaults keys can be either a field GUID or parent attribute GUID. Values will
  be validated

  according to data type and options.
api:
  file: Identification Network (api).yaml
  operationId: forms_templates_create
hidden: false
---