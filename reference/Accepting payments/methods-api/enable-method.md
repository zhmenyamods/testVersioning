---
title: Enable payment method
excerpt: >-
  Enable a payment method on a specific profile.


  When using a profile-specific API credential, the alias `me` can be used
  instead of the profile ID to refer to the current profile.


  Some payment methods require extra steps in order to be activated. In cases
  where a step at the payment method provider needs to be completed first, the
  status will be set to `pending-external` and the response will contain a link
  to complete the activation at the provider.


  To enable voucher or gift card issuers, refer to the [Enable payment method
  issuer](enable-method-issuer) endpoint.


  > 🔑 Access with

  >

  > [API key](/reference/authentication)

  >

  > [Access token with **profiles.write**](/reference/authentication)
api:
  file: accepting-payments.json
  operationId: enable-method
hidden: false
---