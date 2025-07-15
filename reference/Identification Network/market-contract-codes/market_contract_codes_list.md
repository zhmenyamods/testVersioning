---
title: /api/v1/market-contract-codes/
excerpt: >

  Returns all market contract codes that the user has access to.


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


  Access restrictions:


  - If the request user is an admin, all contract codes under the user's
  database scope will be available to view.

  - If the request user is not an admin, the user can only view codes where the
  user is the owner of the contract code,

  the user is part of code's specific users or access structures, or the code
  has no access restrictions.
api:
  file: Identification Network (api).yaml
  operationId: market_contract_codes_list
hidden: false
---