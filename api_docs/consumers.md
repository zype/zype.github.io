---
layout: api
title: Zype Developer Portal | Consumers
permalink: /api_docs/consumers/
---

## Consumers Collection
Lists all Consumers.
<hr>
### List all Consumers
<hr>
<pre><code>GET - https://api.zype.com/consumers/?page=page&per_page=per_page
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
page      | The page number of records to return (zero indexed). Example: 0. | Number
per_page  | The number of records to return. Example: 10. | Number
q         | A query string for searching for consumers | String
id        | Query for a consumer by id | String
id!       | Exclude a consumer from the query | String

#### Response
200
Content-Type: application/json


<pre><code>{
  "response": [
    {
      "_id": "54579a634c616e0389000000",
      "_keywords": [
        "com",
        "example",
        "test123"
      ],
      "created_at": "2014-11-03T15:08:19.675Z",
      "deleted_at": null,
      "email": "test123@example.com",
      "site_id": "53e8d7f869702d5b64010000",
      "stripe_id": "cus_54wKapCMCaqd9b",
      "subscription_count": 1,
      "updated_at": "2014-11-03T15:08:19.675Z"
    }
  ],
  "pagination":
    {
      "current": 1,
      "previous": null,
      "next": 2,
      "per_page": 1,
      "pages": 10
    }
}
</code></pre>

<hr>
### Create a Consumer
<hr>
<pre><code>POST - https://api.zype.com/consumers/{consumer}
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
consumer | A set of key value pairs that describe the Consumer. Needs to include email. | Hash
email | The consumer's email address (must be unique) | string

#### Response
201
Content-Type: application/json

<pre><code> {
  "response": {
    "_id": "54579a634c616e0389000000",
    "_keywords": [
      "com",
      "example",
      "test123"
    ],
    "created_at": "2014-11-03T15:08:19.675Z",
    "email": "test123@example.com",
    "site_id": "53e8d7f869702d5b64010000",
    "stripe_id": "cus_54wKapCMCaqd9b1235",
    "subscription_count": 1,
    "updated_at": "2014-11-03T15:08:19.675Z"
  }
}
</code></pre>

## Consumer
Lists descriptive information about a Consumer
<hr>
### Retrieve a Consumer
<hr>
<pre><code>GET - https://api.zype.com/consumer/{id}
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id        | String id of the Consumer to retrieve. Example: 5389352e69702d401b000000. | String

#### Request
Content-Type: application/json

#### Response
200
Content-Type: application/json

<pre><code> {
  "response": {
    "_id": "54579a634c616e0389000000",
    "_keywords": [
      "com",
      "example",
      "test123"
    ],
    "created_at": "2014-11-03T15:08:19.675Z",
    "deleted_at": null,
    "email": "test123@example.com",
    "site_id": "53e8d7f869702d5b64010000",
    "stripe_id": "cus_54wKapCMCaqd9b1235",
    "subscription_count": 1,
    "updated_at": "2014-11-03T15:08:19.675Z"
  }
}
</code></pre>
