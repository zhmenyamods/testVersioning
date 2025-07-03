---
title: Paw  (COPY)
excerpt: How to trim Loki's paws
deprecated: false
hidden: false
link:
  new_tab: false
metadata:
  title: Paw
  image: >-
    https://files.readme.io/fde0a6270c2e8a3bd93e5bd0704bd23a7ad39ec1304cbb2ff0d9c601a0de6b4e-pngimg.com_-_cat_PNG50533.png
  robots: index
---
当合作方通过智能合约查询到某用户的 KYC 状态为"待验证"时，提示用户点击合作方 APP 中的 KYC 按钮，并通过手机浏览器跳转至 CuteID KYC H5 页面完成 KYC 认证。

CuteID KYC 页面是私有的，访问该页面需要认证。请按照我们预先定义的规则，提供所有参数，并生成base64编码的RSA签名，随后将其作为查询字符串拼接到前端的 base URL 中。

示例：`https://sandbox-web.cuteid.ai?app_uuid={app_uuid}&external_id={external_id}&rand={rand}&timestamp={timestamp}&sign={sign}`
