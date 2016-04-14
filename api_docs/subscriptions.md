---
layout: api
title: Zype Developer Portal | Subscriptions
permalink: /api_docs/subscriptions/
---

## Subscriptions Collection
Lists all Subscriptions.
<hr>
### List all Subscriptions
<hr>
<pre><code>GET - https://api.zype.com/subscriptions/?page=page&per_page=per_page
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
page      | The page number of records to return (zero indexed). Example: 0. | Number
per_page  | The number of records to return. Example: 10. | Number
q         | A query string for searching for subscriptions | String
id        | Query for a subscription by id | String
id!       | Exclude a subscription from the query | String

#### Response
200
Content-Type: application/json


<pre><code>{
  "response": [
    {
      "_id": "54579a714c616e0389010000",
      "_keywords": [
        "com",
        "example",
        "subscription",
        "test123"
      ],
      "amount": "29.29",
      "cancel_at_period_end": false,
      "cancelled_at": null,
      "consumer_id": "54579a634c616e0389000000",
      "coupon_code": null,
      "created_at": "2015-04-30T21:35:25.718-04:00",
      "currency": "USD",
      "current_period_end_at": null,
      "current_period_start_at": null,
      "deleted_at": null,
      "discount_amount": null,
      "discount_duration": null,
      "discount_duration_months": null,
      "discount_percent": null,
      "interval": "month",
      "interval_count": 1,
      "mrr": null,
      "plan_id": "554251d784502d0714ea1300",
      "site_id": "54h76h4069702d523c000000",
      "start_at": null,
      "status": "active",
      "stripe_card_token": null,
      "stripe_id": "sub_5e7ddfHfsXs6",
      "trial_period_days": 0,
      "updated_at": "2015-04-30T21:35:25.718-04:00",
      "plan_name": "6 Month Subscription"
    }
  ],
  "pagination": {
    current: 2,
    previous: 1,
    next: 3,
    per_page: 10,
    pages: 1
  }
}
</code></pre>

<hr>
### Create a Subscription
<hr>
<pre><code>POST - https://api.zype.com/subscriptions/{subscription}
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
subscription | A set of key value pairs that describe the Subscription. Needs to include consumer_id and plan_id. | Hash
consumer_id | The id of the consumer to be subscribed | String
plan_id | The id of the plan the consumer is subscribing to | String
coupon_code | The code of the coupon, if used. This parameter is optional. | String


#### Response
201
Content-Type: application/json

<pre><code>{
  "response": {
    {
      "_id": "54579a714c616e0389010000",
      "_keywords": [
        "com",
        "example",
        "subscription",
        "test123"
      ],
      "amount": "29.29",
      "cancel_at_period_end": false,
      "cancelled_at": null,
      "consumer_id": "54579a634c616e0389000000",
      "coupon_code": null,
      "created_at": "2015-04-30T21:35:25.718-04:00",
      "currency": "USD",
      "current_period_end_at": null,
      "current_period_start_at": null,
      "deleted_at": null,
      "discount_amount": null,
      "discount_duration": null,
      "discount_duration_months": null,
      "discount_percent": null,
      "interval": "month",
      "interval_count": 1,
      "mrr": null,
      "plan_id": "554251d784502d0714ea1300",
      "site_id": "54h76h4069702d523c000000",
      "start_at": null,
      "status": "active",
      "stripe_card_token": null,
      "stripe_id": "sub_5e7ddfHfsXs6",
      "trial_period_days": 0,
      "updated_at": "2015-04-30T21:35:25.718-04:00",
      "plan_name": "6 Month Subscription"
    }
  }
}
</code></pre>

## Subscription
Lists descriptive information about a Subscription
<hr>
###Retrieve a Subscription
<hr>
<pre><code>GET - https://api.zype.com/subscriptions/{id}
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id        | ID of the Subscription to retrieve. Example: 5389352e69702d401b000000. | String

#### Request
Content-Type: application/json

#### Response
200
Content-Type: application/json

<pre><code>{
  "response": {
    {
      "_id": "54579a714c616e0389010000",
      "_keywords": [
        "com",
        "example",
        "subscription",
        "test123"
      ],
      "amount": "29.29",
      "cancel_at_period_end": false,
      "cancelled_at": null,
      "consumer_id": "54579a634c616e0389000000",
      "coupon_code": null,
      "created_at": "2015-04-30T21:35:25.718-04:00",
      "currency": "USD",
      "current_period_end_at": null,
      "current_period_start_at": null,
      "deleted_at": null,
      "discount_amount": null,
      "discount_duration": null,
      "discount_duration_months": null,
      "discount_percent": null,
      "interval": "month",
      "interval_count": 1,
      "mrr": null,
      "plan_id": "554251d784502d0714ea1300",
      "site_id": "54h76h4069702d523c000000",
      "start_at": null,
      "status": "active",
      "stripe_card_token": null,
      "stripe_id": "sub_5e7ddfHfsXs6",
      "trial_period_days": 0,
      "updated_at": "2015-04-30T21:35:25.718-04:00",
      "plan_name": "6 Month Subscription"
    }
  }
}
</code></pre>

<hr>
### Update a Subscription
<hr>
<pre><code>PUT - https://api.zype.com/subscriptions/{id}
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
Subscription     | A set of key value pairs that describe the subscription. | Hash
consumer_id | The id of the consumer | String
plan_id | The id of the plan | String


#### Request

Content-Type: application/json

#### Response
201
Content-Type: application/json

<pre><code>{
  "response": {
    {
      "_id": "54579a714c616e0389010000",
      "_keywords": [
        "com",
        "example",
        "subscription",
        "test123"
      ],
      "amount": "29.29",
      "cancel_at_period_end": false,
      "cancelled_at": null,
      "consumer_id": "54579a634c616e0389000000",
      "coupon_code": null,
      "created_at": "2015-04-30T21:35:25.718-04:00",
      "currency": "USD",
      "current_period_end_at": null,
      "current_period_start_at": null,
      "deleted_at": null,
      "discount_amount": null,
      "discount_duration": null,
      "discount_duration_months": null,
      "discount_percent": null,
      "interval": "month",
      "interval_count": 1,
      "mrr": null,
      "plan_id": "554251d784502d0714ea1300",
      "site_id": "54h76h4069702d523c000000",
      "start_at": null,
      "status": "active",
      "stripe_card_token": null,
      "stripe_id": "sub_5e7ddfHfsXs6",
      "trial_period_days": 0,
      "updated_at": "2015-04-30T21:35:25.718-04:00",
      "plan_name": "6 Month Subscription"
    }
  }
}
</code></pre>

<hr>
### Remove a Subscription
<hr>
<pre><code>DELETE - https://api.zype.com/subscriptions/{id}
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id        | ID of the Subscription to remove. Example: 5389352e69702d401b000000. | String

#### Request
Content-Type: application/json

#### Response
204

