---
title: Create payment
excerpt: >-
  Payment creation is elemental to the Mollie API: this is where most payment
  implementations start off.


  Once you have created a payment, you should redirect your customer to the URL
  in the `_links.checkout` property from the response.


  To wrap your head around the payment process, an explanation and flow charts
  can be found in the 'Accepting payments' guide.


  If you specify the `method` parameter when creating a payment, optional
  additional parameters may be available for the payment method that are not
  listed below. Please refer to the guide on [method-specific
  parameters](extra-payment-parameters).


  > 🔑 Access with

  >

  > [API key](/reference/authentication)

  >

  > [Access token with **payments.write**](/reference/authentication)
api:
  file: accepting-payments.json
  operationId: create-payment
hidden: false
---