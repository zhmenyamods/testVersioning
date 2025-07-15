---
title: Create a resthook subscription
excerpt: >-
  After a subscription is successfully created, we'll send a POST request to
  your target URL with a `X-Hook-Secret` header. <br />

  You need to response to this request with a 200 status code to confirm your
  subscribe intention. <br />

  Then, you need to use the `X-Hook-Secret` to activate the subscription using
  the
  [/resthook_subscriptions/activate](#post-/v3/resthook_subscriptions/activate)
  endpoint. <br />

  For more information and detailed instructions, [see our webhooks
  documentation here.](https://docs.affinda.com/docs/webhooks)
api:
  file: 640aaa7fc2fecc0027ed0fcc.json
  operationId: createResthookSubscription
hidden: false
---