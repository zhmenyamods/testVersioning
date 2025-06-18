---
title: New Endpoint
api:
  file: test-api.json
  operationId: get_new-endpoint
hidden: false
---
responses:
  '200':
    description: OK
    content:
      application/json:
        schema:
          type: object
          properties:
            name:
              type: string
              description: The name of the pet
            petType:
              type: string
              description: The type of pet
            color:
              type: string
              description: The color of the pet
            gender:
              type: string
              description: The gender of the pet
            breed:
              type: string
              description: The breed of the pet