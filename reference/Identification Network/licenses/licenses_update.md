---
title: /api/v1/licenses/{uuid}/
excerpt: >

  Updates an insurance license if it is accessible to the user.


  Access restrictions:


  - Service level users can update any license under their integrated
  application.

  - Admin users can update any license under the admin's agency.

  - Non-admin users can update active licenses where they are the licensee.

  They cannot grant other users access to a license.
api:
  file: Identification Network (api).yaml
  operationId: licenses_update
hidden: false
---