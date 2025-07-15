---
title: /api/v1/licenses/
excerpt: >

  Creates a new insurance license.


  Access restrictions:


  - Service level users can create licenses under any of their allowed agencies,
  for any allowed licensee,

  and assigned to any allowed agents.

  - Admin users can create licenses under their own agency, for any allowed
  licensee,

  and assigned to any allowed agents.

  - Non-admin users can create licenses where they are the licensee, under their
  own agency.

  They cannot grant other users access to a license.
api:
  file: Identification Network (api).yaml
  operationId: licenses_create
hidden: false
---