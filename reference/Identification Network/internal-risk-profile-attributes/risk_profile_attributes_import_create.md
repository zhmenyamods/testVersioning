---
title: /api/v1/risk-profile-attributes/import/
excerpt: |2

      Imports from a user cloud file (CSV) to create Risk Profile Attributes in IDNET.

      Intended for internal use to speed up RPA creation for carrier implementations.

      Requires specific RPA import permission to use.

      Most RPA fields are supported via mapping from header column to field.
      Required fields:
      attribute_id, data_class, requirement_level, underwriting_category
      Fields that have default value:
      data_class, requirement_level, underwriting_category
      Optional RPA fields:
      name, context, description, order, required, value_list_id, effective_date, expiration_date,
      classification_standard_id, classification_codes_str_value,
      classification_codes_standard_id, classification_codes_exclude

      RPA fields that are automatically set: product_id, risk_profiles

      To set related NAICS indexes on RPAs, include a column where the header is "naics_indexes"
      and the values are comma-separated UUIDs of NAICS indexes.

      RPA fields that are not supported: condition_set, class_code_filter_rpas, prefill_source_rpa,
      countries, subdivisions
api:
  file: Identification Network (api).yaml
  operationId: risk_profile_attributes_import_create
hidden: false
---