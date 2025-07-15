---
title: /api/v1/market-bound-status/
excerpt: |2

      •  After the quote is sold, market_bound_status will be set to mark as sold. based on the
      QuoteId, QuoteSessionId and Market
      •  Request body;
          - quoteSessionId:
              UUID (populated during the submission part)
          - quoteId
              id (populated during the submission part)
          - market
              UUID
api:
  file: Identification Network (api).yaml
  operationId: market_bound_status_create
hidden: false
---