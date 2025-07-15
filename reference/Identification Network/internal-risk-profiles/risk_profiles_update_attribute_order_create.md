---
title: /api/v1/risk-profiles/update-attribute-order/
excerpt: |-
  Imports csv with attribute id and order and updates order

  Parameters: attributeOrderFile

  csv file should have two headers:

  id - the attribute primary key

  order - the order of the attribute

  Authentication: user requires special permission to import.
api:
  file: Identification Network (api).yaml
  operationId: risk_profiles_update_attribute_order_create
hidden: false
---