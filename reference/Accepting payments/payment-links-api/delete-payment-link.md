---
title: Delete payment link
excerpt: >-
  Payment links which have not been opened and no payments have been made yet
  can be deleted entirely. This can be useful for removing payment links that
  have been incorrectly configured or that are no longer relevant.


  Once deleted, the payment link will no longer show up in the API or Mollie
  dashboard.


  To simply disable a payment link without fully deleting it, you can use the
  `archived` parameter on the [Update payment link](update-payment-link)
  endpoint instead.


  > 🔑 Access with

  >

  > [API key](/reference/authentication)

  >

  > [Access token with **payment-links.write**](/reference/authentication)
api:
  file: accepting-payments.json
  operationId: delete-payment-link
hidden: false
---