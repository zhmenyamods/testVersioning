---
title: /api/v1/agencies/
excerpt: >

  Returns agencies that are accessible to the user.


  Access restrictions:


  - Service level users can retrieve any agency, agent, and license under their
  integrated application.

  - Admin users can retrieve their own agency, and any agent or license under
  their agency.

  - Non-admin users can retrieve their own active agency, their own active
  agent, and active licenses where

  they or their agency are the licensee, or where they are granted access.
api:
  file: Identification Network (api).yaml
  operationId: agencies_list
hidden: false
---