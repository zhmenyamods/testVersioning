---
title: /api/v1/market-contract-codes/
excerpt: >

  Creates a market contract code.


  Attributes that control access:


  - User - single user that represents the owner of the contract code. The owner
  of a contract code

  can view, update, and delete the contract code.

  - Users - array of users that represent users that have been assigned view
  access to the contract code.

  - Access structures - array of structures that represent the structures that a
  user must belong to,

  in order to view the contract code.

  - If user, users, and access structures are all null or empty, the contract
  code has no access restrictions.


  Permissions:


  - An admin user can set any attributes on a contract code.

  - A non-admin user cannot set access structures or specific users on a
  contract code.

  - A non-admin user can set the owner on a contract code, but the owner must be
  its own user.
api:
  file: Identification Network (api).yaml
  operationId: market_contract_codes_create
hidden: false
---