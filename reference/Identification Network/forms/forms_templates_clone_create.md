---
title: /api/v1/forms/templates/{uuid}/clone/
excerpt: >

  Creates a copy of the template with the given UUID.


  Permissions:

  - Non-admin users cannot clone templates.


  The new template will be scoped to the user's application, regardless of the
  source template's application.


  If the template is cloned by an agency level admin user, the template's agency
  owner will be set to their agency.
api:
  file: Identification Network (api).yaml
  operationId: forms_templates_clone_create
hidden: false
---