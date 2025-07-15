---
title: /api/v1/attributes/import/
excerpt: >

  Imports from a .csv file to create Attributes in IDNET, intended for internal
  use


  Requires a specific attribute import permission to use


  One field is required using an exact name:


  integrated_app_external_id: An external ID for referring to the attribute
  within an integrated application


  Minimum required Attribute fields (supported via mapping from column header to
  field):

  name, external_id (IVANS generated), form_group_id, data_type, order, ivans_id
  and ido_mapping

  Other Attribute fields can be optionally included in the file and the mapping
  as well:

  Ex. default_value, minimum, maximum, suggest_type, suggest_format, etc.
api:
  file: Identification Network (api).yaml
  operationId: attributes_import_create
hidden: false
---