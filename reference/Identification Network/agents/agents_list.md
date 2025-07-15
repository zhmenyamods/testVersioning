---
title: /api/v1/agents/
excerpt: >

  Returns agents that are accessible to the user.


  Access restrictions:


  - Service level users can retrieve any agent and license under their
  integrated application.

  - Admin users can retrieve any agent or license under the admin's agency.

  - Non-admin users can retrieve their own active agent, and active licenses
  where

  they or their agency are the licensee, or where they are granted access.
api:
  file: Identification Network (api).yaml
  operationId: agents_list
hidden: false
---