---
title: Get payment method
excerpt: >-
  Retrieve a single payment method by its ID.


  If a method is not available on this profile, a `404 Not Found` response is
  returned. If the method is available but not enabled yet, a status `403
  Forbidden` is returned. You can enable payments methods via the [Enable
  payment method endpoint](enable-method) of the Profiles API, or via the Mollie
  Dashboard.


  If you do not know the method's ID, you can use the [methods list
  endpoint](list-methods) to retrieve all payment methods that are available.


  Additionally, it is possible to check if wallet methods such as Apple Pay are
  enabled by passing the wallet ID (`applepay`) as the method ID.


  > 🔑 Access with

  >

  > [API key](/reference/authentication)

  >

  > [Access token with **payments.read**](/reference/authentication)
api:
  file: accepting-payments.json
  operationId: get-method
hidden: false
---