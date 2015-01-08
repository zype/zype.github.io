---
layout: api
title: Zype Developer Portal | Plans
permalink: /api_docs/plans/
---

## Plans Collection
Lists all plans.
<hr>
### List all Plans
<hr>
<pre><code>GET - https://api.zype.com/plans/?page=page&per_page=per_page
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
page      | The page number of records to return (zero indexed). Example: 0. | Number
per_page  | The number of records to return. Example: 10. | Number

#### Response
200
Content-Type: application/json


<pre><code>{
  "response": [
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
  ],
  "pagination": {
    "current": 1,
    "previous": null,
    "next": null,
    "per_page": 1,
    "pages": 1
  }
}
</code></pre>

<hr>

## Plan
Lists descriptive information about a plan
<hr>
###Retrieve a Plan
<hr>
<pre><code>GET - https://api.zype.com/plan/{id}
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id        | String id of the Plan to retrieve. Example: 5389352e69702d401b000000. | String

#### Request
Content-Type: application/json

#### Response
200
Content-Type: application/json

<pre><code>{
  "response": {
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
      "stripe_public_key": "abcde12345",
      "trial_period_days": 0,
      "updated_at": "2014-10-23T13:02:20.075Z"
    }
  }
}
</code></pre>
