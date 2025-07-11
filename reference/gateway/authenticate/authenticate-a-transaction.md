---
title: Authenticate a transaction
excerpt: >-
  This API is used to authenticate a transaction. The first step is to call this
  API with sca.type = "enrollment" to check whether the transaction is
  frictionless or needs further challenge. After a successful challenge, this
  API should be called with sca.type = "validation" which will return 3DS2/SCA
  fields.
api:
  file: gateway.json
  operationId: authenticate-a-transaction
hidden: false
---