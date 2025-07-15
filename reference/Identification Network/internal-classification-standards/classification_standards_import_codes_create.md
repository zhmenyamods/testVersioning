---
title: /api/v1/classification-standards/{external_id}/import-codes/
excerpt: >-
  Parses the class codes csv import for a specified class standard.


  User must have special permission to import.


  Columns for the csv are:

  - CODE

  - DESCRIPTION

  - INDEX CODE

  - INDEX DESCRIPTION

  - STATE(S)

  - RELATED CODES

  - RELATED CODES+DESCRIPTIONS


  To Import:

  - set externalId to an unused classification standard with no associated codes

  - import a csv with codes; these can be used as related codes.


  To use previous imported standard as related codes:

  - set externalId to another unused classification standard

  - set relatedCodeStandard to the externalId of a previous import that contains
  related codes.

  - if relatedCodeStandard is not set, RELATED CODES WILL BE IGNORED.

  - Related codes MUST ALL COME FROM THE SAME STANDARD.

  - import another csv for codes that will use the previously uploaded codes as
  related codes.


  There are two columns used to designate related codes:

  - enter related codes in the RELATED CODES column if all the related codes are
  unique for the standard

  - otherwise, use the code|description format in RELATED CODES+DESCRIPTIONS
  column.

  If any codes are entered in the RELATED CODES, parser will ignore RELATED
  CODES+DESCRIPTION.
api:
  file: Identification Network (api).yaml
  operationId: classification_standards_import_codes_create
hidden: false
---