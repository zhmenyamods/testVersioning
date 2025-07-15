---
title: /api/v1/agencies/{id}/
excerpt: >

  Updates an agency if it is accessible to the user.


  Access restrictions:


  - Only service level and admin users can update an agency.

  - Service level users can update any agency under their integrated
  application.

  - Admin users can update their own agency.

  - Only service level users can set the test mode on an agency.
api:
  file: Identification Network (api).yaml
  operationId: agencies_update
hidden: false
---