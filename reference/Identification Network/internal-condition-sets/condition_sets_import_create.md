---
title: /api/v1/condition-sets/import/
excerpt: >

  Imports from a user cloud file (CSV) to create Condition Sets and Conditions
  in IDNET.


  Intended for internal use to speed up Condition Set creation for carrier
  implementations.


  Requires specific Condition Set import permission to use.


  Minimum required Condition Set fields (supported via mapping from column
  header to field):

  name, operator


  Other Condition Set fields can be optionally included in the file and the
  mapping as well:

  Ex. riskProfileAttributeId, conditionSetId (for a parent condition set),
  message, appetite_type, etc.


  Minimum required condition fields (supported via mapping from column header to
  field):

  operator, source_attribute_id, str_value, num_value


  Other Condition fields can be optionally included in the file and the mapping
  as well:

  Ex. source_value_modifier, child_groups_only, etc.


  Condition fields that are automatically set: conditionSetId (matched on
  Condition Set name)
api:
  file: Identification Network (api).yaml
  operationId: condition_sets_import_create
hidden: false
---