---
title: Merge Contacts
excerpt: >
  This endpoint will merge all secondary contacts provided in the request with
  primary contact.


  Important: The primary contact, the contact that will remain after merge, is
  the contact id in the end point.

  Important: An owner contact cannot be merged into another contact, however a
  regular contact can be merged into an owner contact.


  The following are the fields of a contact and what will happen in the event of
  merge:


  Name: Retain primary.

  Company: Secondary added to primary.

  VIP Customer: If true on primary or secondary remain true.

  Birth Date: Retain primary, retain secondary if primary is NULL.

  Do Not Rent: If true on primary or secondary remain true.

  Anniversary Date: Retain primary, retain secondary if primary is NULL.

  PHONE FIELDS (Mobile Phone, Home Phone, Other Phone): Retain primary, retain
  secondary if primary is NULL.

  Work Phone: Retain primary, retain secondary if primary is NULL.

  Primary Email / Alternate email: Retain primary, retain secondary if primary
  is NULL.

  Fax Number: Retain primary, retain secondary if primary is NULL.

  Country: Retain primary, retain secondary if primary is NULL.

  Address 1: Retain primary, retain secondary if primary is NULL.

  Address 2: Retain primary, retain secondary if primary is NULL on Address 1.

  City: Retain primary, retain secondary if primary is NULL on Address 1.

  State: Retain primary, retain secondary if primary is NULL on Address 1.

  Zip: Retain primary, retain secondary if primary is NULL on Address 1.

  Payment type: Will not overwrite or import.

  Tax ID: Will not overwrite or import.

  Custom Fields: Will not overwrite or import.
api:
  file: crm-api.json
  operationId: contactMerge
hidden: false
---