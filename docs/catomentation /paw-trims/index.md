---
title: 'Paw '
excerpt: How to trim Loki's paws
deprecated: false
hidden: false
metadata:
  robots: index
---
## Attribute keys

* All attribute keys should be lowercase snake case. Example: `order_id`
* All attribute keys on a resource are ordered according to the following standards:
  * The primary key (id) appears first in the object body.
  * Secondary keys relating an object to other resources appear next, in alphabetical order.
  * All other attributes of an object appear next, in alphabetical order.

***

## Formats

* All date and date-time values are formatted in the ISO 8601 standard and in UTC.
* All records of a list response will be sorted by id descending unless otherwise specified using a `sort_by` parameter in the request.
* The list of attributes in any resource doesn’t change based on the ecommerce platform. For example, references to external IDs such as the product ID or customer ID in the e-commerce platform are contained within a standard field name prefixed by the term external. For example, `external_product_id` instead of `shopify_product_id`. This ensures that you don’t have to adjust your integration code based on the underlying e-commerce platform.
* All external IDs are formatted as strings.
* All amounts, such as product prices, are formatted as strings.
* Any rate value inside a tax\_lines object is displayed to four decimal places to accurately reflect tax rates. For example, a 12.5% tax rate is reflected as 0.1250.
* All dollar amounts, such as product prices, are formatted as strings.

***

## Errors

From `2021-11`, onward we use the following grid of errors codes:<br /><br />

<HTMLBlock>{`
<div>
    <ul>
          <li><code>200</code> : the request was successful, made no modifications, and the resource requested is in the body.</li>
          <li><code>201</code> : the request was successful, created a new resource, and resource created is in the body.</li>
          <li><code>202</code> : the request has been accepted and is in processing.</li>
          <li><code>204</code> : the request has been processed successfully. There is no response body.</li>
          <li><code>400</code> : the request was not understood.</li>
          <li><code>401</code> : the request was not able to be authenticated.</li>     
          <li><code>403</code> : the request was authenticated but not authorized for the requested resource (permission scope error).</li>
          <li><code>404</code> : the requested resource or record was not found.</li>
          <li><code>406</code> : the request was unacceptable, or requesting a data source which is not allowed although permissions permit the request.</li>
          <li><code>409</code> : the request is in conflict, or would create a conflict with an existing request or resource (the route is locked).</li>
          <li><code>415</code> : the request body was not a JSON object.</li>
          <li><code>422</code> : the request was understood but cannot be processed due to invalid or missing supplemental information.</li>
          <li><code>426</code> : the request was made using an invalid API version.</li>
          <li><code>429</code> : the request has been rate limited.</li>
          <li><code>500</code> : internal server error.</li>
          <li><code>501</code> : the resource requested has not been implemented in the current version but may be implemented in the future.</li>
          <li><code>503</code> : A 3rd party service on which the response depends has timed out.</li>
        </ul>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<h3 style="text-align: center;">Need Help? <a href="https://support.rechargepayments.com/hc/en-us/requests/new?ticket_form_id=360000121553"
   onclick="getOutboundLink('https://support.rechargepayments.com/hc/en-us/requests/new?ticket_form_id=360000121553'); return false;">Contact Us</a></h3>
`}</HTMLBlock>