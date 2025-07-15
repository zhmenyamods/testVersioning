---
title: /api/v1/value-lists/import/
excerpt: |2

      Imports from a user cloud file (CSV) to create value lists and value list options in IDNET.

      Intended for internal use to speed up value list creation for carrier implementations.

      Requires specific value list import permission to use.

      Value list fields that are supported via mapping from header column to field:
      name, description, data_type

      Value list option fields that are supported via mapping from header column to field:
      name, order, int_value, str_value

      Value list option fields that are automatically set: value_list_id (matched on value list name)
api:
  file: Identification Network (api).yaml
  operationId: value_lists_import_create
hidden: false
---