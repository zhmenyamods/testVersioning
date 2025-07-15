---
title: /api/v1/licenses/{uuid}/
excerpt: >

  Returns an insurance license if it is accessible to the user.


  Access restrictions:


  - Service level users can retrieve any license under their integrated
  application.

  - Admin users can retrieve any license under the admin's agency.

  - Non-admin users can retrieve active licenses where

  they or their agency are the licensee, or where they are granted access.
api:
  file: Identification Network (api).yaml
  operationId: licenses_retrieve
hidden: false
---