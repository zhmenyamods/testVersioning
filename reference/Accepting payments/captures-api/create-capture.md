---
title: Create capture
excerpt: >-
  **This feature is currently in open beta. The final specification may still
  change.**


  Capture an *authorized* payment.


  Some payment methods allow you to first collect a customer's authorization,
  and capture the amount at a later point.


  By default, Mollie captures payments automatically. If however you configured
  your payment with `captureMode: manual`, you can capture the payment using
  this endpoint after having collected the customer's authorization.


  > 🔑 Access with

  >

  > [API key](/reference/authentication)

  >

  > [Access token with **payments.write**](/reference/authentication)
api:
  file: accepting-payments.json
  operationId: create-capture
hidden: false
---