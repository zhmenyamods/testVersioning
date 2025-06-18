---
title: Cancel payment refund
excerpt: >-
  Refunds will be executed with a delay of two hours. Until that time, refunds
  may be canceled manually via the Mollie Dashboard, or by using this endpoint.


  A refund can only be canceled while its `status` field is either `queued` or
  `pending`. See the [Get refund endpoint](get-refund) for more information.


  > 🔑 Access with

  >

  > [API key](/reference/authentication)

  >

  > [Access token with **refunds.write**](/reference/authentication)
api:
  file: accepting-payments.json
  operationId: cancel-refund
hidden: false
---