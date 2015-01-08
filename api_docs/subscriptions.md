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
    {
      "_id": "54579a714c616e0389010000",
      "_keywords": [
        "com",
        "example",
        "subscription",
        "test123"
      ],
      "amount": "5.99",
      "consumer_id": "54579a634c616e0389000000",
      "created_at": "2014-11-03T15:08:33.668Z",
      "currency": "USD",
      "deleted_at": null,
      "interval": "month",
      "plan_id": "544813e74c616e0dc0000000",
      "site_id": "53e8d7f869702d5b64010000",
      "stripe_card_token": "tok_14umRWBZRS312G8xjfXD1zHQvP3",
      "stripe_id": "sub_54wKXHYIaIj8812YgK",
      "trial_period_days": 14,
      "updated_at": "2014-11-03T15:08:33.668Z"
    }
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
      "amount": "5.99",
      "consumer_id": "54579a634c616e0389000000",
      "created_at": "2014-11-03T15:08:33.668Z",
      "currency": "USD",
      "deleted_at": null,
      "interval": "month",
      "plan_id": "544813e74c616e0dc0000000",
      "site_id": "53e8d7f869702d5b64010000",
      "stripe_card_token": "tok_14umRWBZRS312G8xjfXD1zHQvP3",
      "stripe_id": "sub_54wKXHYIaIj8812YgK",
      "trial_period_days": 14,
      "updated_at": "2014-11-03T15:08:33.668Z"
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
id        | String id of the Subscription to retrieve. Example: 5389352e69702d401b000000. | String

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
      "amount": "5.99",
      "consumer_id": "54579a634c616e0389000000",
      "created_at": "2014-11-03T15:08:33.668Z",
      "currency": "USD",
      "deleted": false,
      "interval": "month",
      "plan_id": "544813e74c616e0dc0000000",
      "site_id": "53e8d7f869702d5b64010000",
      "stripe_card_token": "tok_14umRWBZRS312G8xjfXD1zHQvP3",
      "stripe_id": "sub_54wKXHYIaIj8812YgK",
      "trial_period_days": 14,
      "updated_at": "2014-11-03T15:08:33.668Z"
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
      "amount": "5.99",
      "consumer_id": "54579a634c616e0389000000",
      "created_at": "2014-11-03T15:08:33.668Z",
      "currency": "USD",
      "deleted": false,
      "interval": "month",
      "plan_id": "544813e74c616e0dc0000000",
      "site_id": "53e8d7f869702d5b64010000",
      "stripe_card_token": "tok_14umRWBZRS312G8xjfXD1zHQvP3",
      "stripe_id": "sub_54wKXHYIaIj8812YgK",
      "trial_period_days": 14,
      "updated_at": "2014-11-03T15:08:33.668Z"
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
id        | String id of the Subscription to remove. Example: 5389352e69702d401b000000. | String

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
      "amount": "5.99",
      "consumer_id": "54579a634c616e0389000000",
      "created_at": "2014-11-03T15:08:33.668Z",
      "currency": "USD",
      "deleted": false,
      "interval": "month",
      "plan_id": "544813e74c616e0dc0000000",
      "site_id": "53e8d7f869702d5b64010000",
      "stripe_card_token": "tok_14umRWBZRS312G8xjfXD1zHQvP3",
      "stripe_id": "sub_54wKXHYIaIj8812YgK",
      "trial_period_days": 14,
      "updated_at": "2014-11-03T15:08:33.668Z"
    }
  }
}
</code></pre>
