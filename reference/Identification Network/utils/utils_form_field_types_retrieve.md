---
title: /api/v1/utils/form-field-types/
excerpt: >

  Returns information, including JSON data type, API route, and object
  properties, for all form field types.


  jsonDataType - the JSON data type of the answer that an integrator should
  submit for a field type. A list

  of JSON data types is provided if the answer can be one of multiple data
  types.


  optionsApiRoute - IDNET API route that an integrator should call to retrieve
  the options for a dropdown-like

  field


  optionPropertiesToDisplay - if the options retrieved via API are objects, this
  specifies which object

  properties an integrator should display on the front-end as answer choices


  optionPropertiesToSubmit - if the options retrieved via API are objects, this
  specifies which object

  properties an integrator should submit as the answer
api:
  file: Identification Network (api).yaml
  operationId: utils_form_field_types_retrieve
hidden: false
---