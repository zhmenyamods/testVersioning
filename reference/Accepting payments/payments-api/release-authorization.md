---
title: Release payment authorization
excerpt: >-
  Releases the full remaining authorized amount. Call this endpoint when you
  will not be making any additional captures. Payment authorizations may also be
  released manually from the Mollie Dashboard.


  Mollie will do its best to process release requests, but it is not guaranteed
  that it will succeed. It is up to the issuing bank if and when the hold will
  be released.


  If the request does succeed, the payment status will change to `canceled` for
  payments without captures. If there is a successful capture, the payment will
  transition to `paid`.


  > 🔑 Access with

  >

  > [API key](/reference/authentication)

  >

  > [Access token with **payments.write**](/reference/authentication)
api:
  file: accepting-payments.json
  operationId: release-authorization
hidden: false
---