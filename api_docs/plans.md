---
layout: api
title: Zype Developer Portal | Plans
permalink: /api_docs/plans/
---

## Plans Collection
<hr>
### List Plans
<pre><b>GET</b> https://api.zype.com/plans</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
page      | The page number of records to return (Example: 1) | Integer
per_page  | The number of records to return (Example: 10) | Integer
q         | Filter records by keyword | String
id        | Filter records by ID | String
id!       | Exclude records by ID | String

### Retrieve a Plan
<pre><b>GET</b> https://api.zype.com/plans/[id]</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id        | ID of the record to retrieve (Example: 5389352e69702d401b000000) | String

### Plan Object
<pre>
{
  "_id": "544813e74c616e0dc0000000",
  "_keywords": [],
  "active": true,
  "amount": "7.99",
  "created_at": "2014-10-22T20:30:31.792Z",
  "currency": "USD",
  "description": 'Description for the plan',
  "interval": "month",
  "name": "Zype Monthly Subscription",
  "stripe_id": "zype-monthly",
  "stripe_public_key": "pk_test_123456",
  "trial_period_days": 0,
  "updated_at": "2014-10-23T13:02:20.075Z"
}
</pre>