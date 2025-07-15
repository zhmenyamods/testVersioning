---
title: /api/v1/agents/{id}/
excerpt: >

  Returns an agent if it is accessible to the user.


  Access restrictions:


  - Service level users can retrieve any agent and license under their
  integrated application.

  - Admin users can retrieve any agent or license under their agency.

  - Non-admin users can retrieve their own active agent, and active licenses
  where

  they or their agency are the licensee, or where they are granted access.
api:
  file: Identification Network (api).yaml
  operationId: agents_retrieve
hidden: false
---