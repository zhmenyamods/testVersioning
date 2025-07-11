---
title: 'Paw '
excerpt: How to trim Loki's paws
deprecated: false
hidden: false
metadata:
  title: Paw
  image: >-
    https://files.readme.io/fde0a6270c2e8a3bd93e5bd0704bd23a7ad39ec1304cbb2ff0d9c601a0de6b4e-pngimg.com_-_cat_PNG50533.png
  robots: index
---
<span style={{ color: "red", fontSize: "24px", fontWeight: "bold" }}># Required Account Level: Standard Edition and Above</span>

# Real-Time Futures Trade Orders Push

## Channel: `futures_trades@``{exchange}`\_`{symbol}`@`{minVol}`

To subscribe to the `futures_trades` channel, send the following message:

```json
{
    "method": "subscribe",
    "channels": ["futures_trades@Binance_BTCUSDT@10000"]
}
```

### Response Example

Upon receiving data, the response will look like this:

```json
{
    "channel": "futures_trades@Binance_BTCUSDT@10000",
    "data": [
        {
            "baseAsset": "BTC",
            "exName": "Binance",
            "price": 56738.00,
            "side": 2,//side=1  sell.   side=2   buy   
            "symbol": "BTCUSDT",
            "time": 1725416318379,
            "volUsd": 3858.18400
        }
    ]
}
```