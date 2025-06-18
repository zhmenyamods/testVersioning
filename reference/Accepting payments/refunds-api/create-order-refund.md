---
title: Create order refund
excerpt: >-
  When using the Orders API, refunds should be made for a specific order.


  If you want to refund arbitrary amounts, however, you can also use the [Create
  payment refund endpoint](create-refund) by creating a refund on the payment
  itself.


  If an order line is still in the `authorized` state, it cannot be refunded.
  You should cancel it instead. Order lines that are `paid`, `shipping` or
  `completed` can be refunded.


  > 🔑 Access with

  >

  > [API key](/reference/authentication)

  >

  > [Access token with **refunds.write**](/reference/authentication)
api:
  file: accepting-payments.json
  operationId: create-order-refund
hidden: false
---