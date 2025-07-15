---
title: Activate a resthook subscription
excerpt: >-
  After creating a subscription, we'll send a POST request to your target URL
  with a `X-Hook-Secret` header. <br />

  You should response to this with a 200 status code, and use the value of the
  `X-Hook-Secret` header that you received to activate the subscription using
  this endpoint.
api:
  file: 640aaa7fc2fecc0027ed0fcc.json
  operationId: activateResthookSubscription
hidden: false
---